BootStrap:docker
From:nvidia/cuda:8.0-cudnn6-devel

%labels
MAINTAINER Huilin Qu

%runscript
exec echo "The runscript is the container default runtime command!"

%post

apt-get update && apt-get -y install wget pip

# download and run NIH HPC NVIDIA driver installer
wget https://raw.githubusercontent.com/NIH-HPC/gpu4singularity/master/gpu4singularity 
chmod u+rwx gpu4singularity
./gpu4singularity --verbose
rm gpu4singularity

pip install matplotlib numexpr numpy pandas scikit-learn scipy tables mxnet-cu80
mkdir -p /data
echo "Done!"
