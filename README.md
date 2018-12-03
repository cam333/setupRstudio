# setupRstudio
how to set up rstudio on gcp

update source list
1. sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
2. echo "deb http://cran.rstudio.com/bin/linux/debian stretch-cran34/" | sudo tee -a /etc/apt/sources.list

Latest version of R on Debian
(https://www.linode.com/docs/development/r/how-to-install-r-on-ubuntu-and-debian/)

1. sudo apt install dirmngr
2. sudo apt-key adv --keyserver keys.gnupg.net --recv-key 'E19F5F87128899B192B1A2C2AD5F960A256A04AF'
3. sudo apt update
4. sudo apt install r-base


## Rstudio Server (https://www.rstudio.com/products/rstudio/download-server/)

1. sudo apt-get install gdebi-core
2. wget https://download2.rstudio.org/rstudio-server-stretch-1.1.463-amd64.deb
3. sudo gdebi rstudio-server-stretch-1.1.463-amd64.deb
