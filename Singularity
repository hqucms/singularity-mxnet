BootStrap:docker
From:nvidia/cuda:8.0-cudnn6-devel

%labels
MAINTAINER Huilin Qu

%runscript
exec echo "The runscript is the container default runtime command!"

%post

# download and run NIH HPC NVIDIA driver installer
wget gpu4singularity 
chmod u+rwx gpu4singularity
./gpu4singularity --verbose
rm gpu4singularity

pip install matplotlib numexpr numpy pandas scikit-learn scipy tables mxnet-cu80
mkdir -p /data
echo "Done!"
