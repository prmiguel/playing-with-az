# `ACI` - Azure Container Instance

## Examples

### Create a container in a container group with public IP address
```sh
az container create -g $resource --image nginx:1.21 --ip-address public --name nginx
```

### Create a container in a container group with public IP address and port
```sh
az container create -g $resource --image prmiguel/computer-database --ip-address public --ports 9000 --name computer-db
```

### Create a container in a container group that mounts a git repo as volume.
```sh
az container create -g $resource --name fileshare-repo --image filebrowser/filebrowser --gitrepo-url https://github.com/filebrowser/filebrowser --gitrepo-dir ./filebrowser --gitrepo-mount-path /srv --ip-address public
```

### Create a container in a container group with environment variables.
```sh
az container create -g $resource --name color-red --image bedis9/colors --ip-address public --environment-variables COLOR=red --ports 8080
```
