run docker command in jupyter notebook container.

## how to use

### run jupyter container
```
docker run -p 8888:8888 \
  -v /var/run/docker.sock:/var/run/docker.sock \
  syspro86/jupyter_with_docker
```

### run docker command in notebook
run docker command with preceding '!sudo' 

```
!sudo docker ps
```
![docker](https://user-images.githubusercontent.com/31230327/67204020-8a338b80-f447-11e9-8f07-6c65528ca752.png)

