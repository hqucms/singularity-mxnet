BootStrap:docker
From:mxnet/python:gpu

%labels
MAINTAINER Huilin Qu

%runscript
exec echo "The runscript is the containers default runtime command!"

%post
mkdir -p /data
pip install matplotlib numexpr numpy pandas scikit-learn scipy tables
echo "Done!"
