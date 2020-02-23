----
## Windows Subsystem for Linux
#### Installation Guide for Windows 10
* Windows 10 version: >16.07
* Open Control Panel -> Programs and Features -> Turn Windows Feature on or off -> Check Windows Subsystem for Linux
* Reboot
* Microsoft store: Ubuntu 18.04 LTS
----

## R Installation
#### R
```
# Remove outdated R
sudo apt-get --purge remove r-base r-base-core r-base-dev

# updat R source
sudo vim /etc/apt/sources.list
deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/

# R installation
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
sudo apt-get update
sudo apt-get install -y r-base r-base-core r-base-dev
```

#### Essential elements for R
```bash
sudo apt install openjdk-8-jre-headless
sudo apt-get install exfat-utils exfat-fuse
sudo apt-get install libcurl4-openssl-dev
sudo apt-get install libxml2-dev
sudo apt-get -y install libssl-dev subversion scons libfuse-dev gcc
sudo apt-get -y install libmariadb-dev libudunits2-dev
sudo apt-get install libhdf5-dev
```
----

## Bioconda

```bash
## Miniconda
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh

## Add channels
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/menpo/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
conda config --set show_channel_urls yes
```
