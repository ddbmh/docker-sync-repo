## Synchronize images from Docker Hub to local Registry


### Editing image lists
Edit the images.txt of the repos for syncing


### Usage

Sample

need python 2.7
设置目标阿里云仓库地址和namespace(--registry  registry.cn-hangzhou.aliyuncs.com/tzm-hz)
设置要同步的仓库列表文件 --file images.txt
设置从哪里同步 --docker_host=127.0.0.1:5000
python sync_images.py --registry registry.cn-hangzhou.aliyuncs.com/tzm-hz --file images.txt --docker_host=127.0.0.1:5000



Help
 
```sh
python sync_images -h|--help
```


Synchronize images from specific repository 

```sh
python sync_images -n|--name <repo_name> 
```


Synchronize images from the configuraiton files, by default "images.txt"

```sh
python sync_images [-f|--file <config_file>]
```

Other optional arguments


```sh
-d|--docker_host <tcp://server:port>|<'unix:///var/run/docker.sock'>

-r|--registry <host:port>

-i|--insecure_registry
```