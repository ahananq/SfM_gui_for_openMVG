## Ubuntu 15.10 building
```
#Prepare and empty machine for building:
sudo apt-get update -qq && sudo apt-get install -qq
sudo apt-get -y install git subversion cmake libpng-dev libjpeg-dev libtiff-dev libglu1-mesa-dev libeigen3-dev libboost-iostreams-dev libboost-program-options-dev libboost-system-dev libboost-serialization-dev libopencv-dev libcgal-dev libatlas-base-dev libsuitesparse-dev qt5-default libpcl-dev libxxf86vm1 libxxf86vm-dev libxi-dev libxrandr-dev graphviz
main_path=`pwd`

#VCGLib (Required)
svn checkout svn://svn.code.sf.net/p/vcg/code/trunk/vcglib vcglib

#Ceres (Required)
git clone https://ceres-solver.googlesource.com/ceres-solver ceres-solver
mkdir ceres_build && cd ceres_build/
cmake . ../ceres-solver/ -DMINIGLOG=ON -DBUILD_TESTING=OFF -DBUILD_EXAMPLES=OFF
make && sudo make install
cd ..

#CMVS / PMVS (Optional)
git clone https://github.com/open-anatomy/CMVS-PMVS.git
mkdir CMVS-PMVS_build && cd CMVS-PMVS_build
cmake ../CMVS-PMVS/program
make && sudo make install
cd ..

#OpenMVS (Recommended)
git clone https://github.com/open-anatomy/openMVS.git --branch ubuntu_15_10 openMVS
mkdir openMVS_build && cd openMVS_build
cmake . ../openMVS -DCMAKE_BUILD_TYPE=Release -DVCG_DIR="$main_path/vcglib"
make && sudo make install
cd ..

#OpenMVG + GUI (Required)
git clone --recursive https://github.com/open-anatomy/SfM_gui_for_openMVG.git openMVG
mkdir openMVG_build && cd openMVG_build
cmake -DCMAKE_BUILD_TYPE=RELEASE . ../openMVG/src/ -DCMAKE_INSTALL_PREFIX=$main_path/openMVG_build/openMVG_install -DBUILD_SFM_GUI=ON -DOPENMVG_PMVS_PATH=$main_path/CMVS-PMVS_build
make && make install
```
