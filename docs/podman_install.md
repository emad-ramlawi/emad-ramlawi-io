```
echo "deb https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_${VERSION_ID}/ /" | sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list
curl -L https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_${VERSION_ID}/Release.key | sudo apt-key add -
sudo apt update
sudo apt -y install podman
nano /etc/containers/registries.conf
    [registries.search]
    registries = ['docker.io', 'quay.io', 'registry.access.redhat.com']
nginx installation on podman
podman image pull nginx:latest
podman run --name mynginx -p 8080:80 -d nginx
```
