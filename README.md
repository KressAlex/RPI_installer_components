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

## Install Node-Red
      bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)

## Install InfluxDB
      TBD 
      
## Install Grafana
      wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add - 
      echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
      sudo apt update -y
      sudo apt install grafana -y
      sudo systemctl enable grafana-server
      sudo systemctl start grafana-server



      
