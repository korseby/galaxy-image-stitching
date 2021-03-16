# galaxy-image-stitching

export CFLAGS="-I/opt/include/libomp"; export CCFLAGS=$CFLAGS; export CXXFLAGS=$CFLAGS; export LDFLAGS="-L/opt/lib/libomp -L/opt/lib"
port install libeigen3-dev eigen jpeg
git clone https://github.com/ppwwyyxx/OpenPano
cd OpenPano
vi src/Makefile, change usr and usr/local to opt, add -I/opt/include to OPTFLAGS
cd ..
./OpenPano/src/image-stitching *.jpg
echo use supplied config.cfg
echo Output file is always saved to out.jpg
