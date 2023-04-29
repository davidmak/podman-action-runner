dnf -y module enable container-tools:rhel8; dnf -y update; rpm --restore --quiet shadow-utils; dnf -y install crun podman netavark fuse-overlayfs /etc/containers/storage.conf --exclude container-selinux; rm -rf /var/cache /var/log/dnf* /var/log/yum.*
dnf -y install podman-docker

useradd podman; echo podman:10000:5000 > /etc/subuid; echo podman:10000:5000 > /etc/subgid;
mkdir -p /home/podman/.local/share/containers
mkdir -p /home/podman/.config
chown podman:podman -R /home/podman

cd /home/podman/
mkdir actions-runner
cd actions-runner
...
./bin/installdependencies.sh 
mkdir /github
ln -s /home/podman /github/home
