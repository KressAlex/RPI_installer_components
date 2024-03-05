# RPI_installer_components
Node-Red, Influxdb, grafana installation

$ sudo apt update
$ sudo apt upgrade -y


##	Installation procedure

      $ sudo apt update
      $ sudo apt upgrade -y

## Run script
      $ sudo ./install.sh



## Install Node-Red
      $ bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)

## Install InfluxDB
      $ 
      
## Install Grafana
      $ wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add - 
      echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
      sudo apt update
      sudo apt install grafana
      sudo systemctl enable grafana-server
      sudo systemctl start grafana-server



      
