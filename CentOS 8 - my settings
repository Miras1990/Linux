Repozytorium EPEL: https://rpmfusion.org/Configuration
sudo yum install --nogpgcheck https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

Repozytorium RPM Fusion:
sudo yum install --nogpgcheck https://download1.rpmfusion.org/free/el/rpmfusion-free-release-8.noarch.rpm https://download1.rpmfusion.org/nonfree/el/rpmfusion-nonfree-release-8.noarch.rpm

CentOS 8 required additional step:
sudo yum config-manager --enable PowerTools

AppStream metadata
sudo yum groupupdate core

Multimedia post-install
sudo yum groupupdate multimedia --setop="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin
sudo yum groupupdate sound-and-video

Tainted repos (odtwarzanie filmów z DVD)
sudo yum install rpmfusion-free-release-tainted
sudo yum install libdvdcss

Włączyć repozytorium flathub: https://flatpak.org/setup/CentOS/
https://flathub.org/repo/flathub.flatpakrepo
sudo cp flathub.flatpakrepo /etc/yum.repos.d/

Google Chrome:
wget https://dl.google.com/linux/linux_signing_key.pub
sudo rpm --import linux_signing_key.pub
rpm -qi gpg-pubkey-7fac5991-*

ElRepo: http://elrepo.org/tiki/tiki-index.php
rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org
sudo yum install https://www.elrepo.org/elrepo-release-8.1-1.el8.elrepo.noarch.rpm

NVIDIA Cuda Toolkit: https://developer.nvidia.com/cuda-downloads
sudo yum config-manager --add-repo http://developer.download.nvidia.com/compute/cuda/repos/rhel8/x86_64/cuda-rhel8.repo
sudo yum clean all
sudo yum -y module install nvidia-driver:latest-dkms
sudo yum -y install cuda

Kodeki:
sudo yum install gstreamer1-plugins-* ffmpeg

Thermald:
sudo yum install automake gcc gcc-c++ glib2-devel libxml2-devel dbus-glib-devel

TLP:
wget https://download-ib01.fedoraproject.org/pub/epel/7/x86_64/Packages/t/tlp-1.1-1.el7.noarch.rpm https://download-ib01.fedoraproject.org/pub/epel/7/x86_64/Packages/t/tlp-rdw-1.1-1.el7.noarch.rpm
sudo yum install tlp-1.1-1.el7.noarch.rpm tlp-rdw-1.1-1.el7.noarch.rpm
sudo nano /etc/default/tlp
sudo systemctl enable tlp.service
sudo systemctl start tlp.service
