# MALOS-eye examples

### Pre-Requisites
```
# Base repository and assoc. packages
echo "deb http://packages.matrix.one/matrix-creator/ ./" | sudo tee --append /etc/apt/sources.list
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install libzmq3-dev xc3sprog malos-eye matrix-creator-malos matrix-creator-openocd wiringpi matrix-creator-init cmake g++ git

# Install npm (doesn't really matter what version, apt-get node is v0.10...)
sudo apt-get install npm nodejs

# n is a node version manager
sudo npm install -g n

# node 6.5 is the latest target node version, also installs new npm
n 6.5


```
### Getting Started with the Examples
```
# Clone repository.
git clone https://github.com/matrix-io/malos-eye.git

# Fetch protocol-buffers repository.
git submodule init
git submodule update

# Setup examples.
cd examples
npm install
```

### Face Detection with Demographics
Demographics example. Detect faces and get age, gender, emotion and pose by querying a remote server.
```
node query_demographics.js
```

### Gesture Detection
Everloop + Gesture demo. Control the Everloop LEDs with your hand.
```
node gesture_plus_everloop.js
```
