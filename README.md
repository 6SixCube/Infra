# Infrastructure

Repository to configure my linux PC. Here i will discribe all scripts and tools i need.


## Icescrum

### Docker Install 

#### Icescrum 
download from repository :

```bash
docker pull icescrum/icescrum
```

launch docker icescrum only :
```bash
docker run --name icescrum -v /home/pierref/icescrum:/root -p 8080:8080 icescrum/icescrum
```  

#### mysql install :

Configure docker network :

```bash
docker network create --driver bridge is_net
docker run --name mysql -v /home/pierref/icescrum/mysql:/var/lib/mysql --net=is_net -e MYSQL_DATABASE=icescrum -e MYSQL_ROOT_PASSWORD=root -d mysql:5.7 --character-set-server=utf8mb4 --collation-server=utf8mb4_unicode_ci
```


**Have Fun**
