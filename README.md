# RPI_installer_components
Node-Red, Influxdb, grafana installation



## Use git to install installation script
      git clone https://github.com/KressAlex/RPI_installer_components.git ~/Install_script
      cd ~/Install_script
      sudo chmod +x install.sh
      sudo ./install.sh
      
## Installation procedure
      sudo apt update
      sudo apt upgrade -y

## Run script
      sudo ./install.sh

## Install Node-Red -> self created
      sudo apt install build-essential git
      bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered) -y -y
      node-red-pi --max-old-space-size=256 -y 
      sudo systemctl enable nodered.service 

Node-red login admin, pw adminadmin
noderedsetup


## Install Node-Red -> by superhouse.tv
      sudo apt install build-essential git
      bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
      npm install node-red-contrib-influxdb
      sudo systemctl enable nodered.service
      sudo systemctl start nodered.service



## Install InfluxDB -> https://pimylifeup.com/raspberry-pi-influxdb/

      curl https://repos.influxdata.com/influxdata-archive.key | gpg --dearmor | sudo tee /usr/share/keyrings/influxdb-archive-   keyring.gpg >/dev/null
      echo "deb [signed-by=/usr/share/keyrings/influxdb-archive-keyring.gpg] https://repos.influxdata.com/debian stable main" | sudo tee /etc/apt/sources.list.d/influxdb.list
      sudo apt update
      sudo apt install influxdb
      sudo systemctl unmask influxdb
      sudo systemctl enable influxdb
      sudo systemctl start influxdb

      #Setup InfluxDB V1

      influx
      CREATE DATABASE tanklevel
      use tanklevel      #stopped at step 3

      
## Install InfluxDB
      TBD 
      
## Install Grafana
      wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add - 
      echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
      sudo apt update -y
      sudo apt install grafana -y
      sudo systemctl enable grafana-server
      sudo systemctl start grafana-server



      
