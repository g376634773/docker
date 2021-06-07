### 搜索镜像版本
curl https://registry.hub.docker.com/v1/repositories/centos/tags\
| tr -d '[\[\]" ]' | tr '}' '\n'\
| awk -F: -v image='centos' '{if(NR!=NF && $3 != ""){printf("%s:%s\n",image,$3)}}'

