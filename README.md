# setupRstudio
how to set up rstudio on gcp

update source list

```
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
echo "deb http://cran.rstudio.com/bin/linux/debian stretch-cran34/" | sudo tee -a /etc/apt/sources.list
```
Latest version of R on Debian
(https://www.linode.com/docs/development/r/how-to-install-r-on-ubuntu-and-debian/)

```
sudo apt install dirmngr
sudo apt-key adv --keyserver keys.gnupg.net --recv-key 'E19F5F87128899B192B1A2C2AD5F960A256A04AF'
sudo apt update
sudo apt install r-base
```

## Rstudio Server (https://www.rstudio.com/products/rstudio/download-server/)

```
sudo apt-get install gdebi-core
wget https://download2.rstudio.org/rstudio-server-stretch-1.1.463-amd64.deb
sudo gdebi rstudio-server-stretch-1.1.463-amd64.deb
```

## enable port 8787 on gcp

create a fire wall 0.0.0.0/0 for TCP 8787
apply to all instances or pick a specific instance - which is the name of the instance 

## create a user 
```
sudo adduser "rserver"
passwd rserver 
sudo usermod -aG sudo rserver
```
## give access to the home dir
```
sudo chmod -R 777 /home 
```
