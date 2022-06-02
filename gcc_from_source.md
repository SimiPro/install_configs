##download 
release from: https://github.com/gcc-mirror/gcc/tags 

## download additional sources and libs
- ./gcc_dir/contrib/download_prerequisites
- sudo apt install flex

## configure
./configure -v --build=x86_64-linux-gnu --host=x86_64-linux-gnu --target=x86_64-linux-gnu 
          --prefix=/usr/local/gcc-12.1.0 --enable-checking=release --enable-languages=c,c++,fortran --disable-multilib --program-suffix=-12.1
          
## make
make -j16

## install
sudo make install

## enjoy
/usr/local/gcc-12.1.0/bin/g++-12.1  --version

