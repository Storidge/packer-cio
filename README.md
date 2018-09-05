# Packer Templates for Storidge CIO
This repo contains [Packer](https://www.packer.io/) templates for generating AWS AMIs and DigitalOcean snapshot images with the community edition of the [Storidge CIO](http://storidge.com/docs/) software. 

## Templates

aws-c7xl3.json - Base install of Centos 7.4 with Storidge CIO for AWS AMI

aws-u14.json - Base install of Ubuntu 14.04 with Storidge CIO for AWS AMI

aws-u16.json - Base install of Ubuntu 16.04 with Storidge CIO for AWS AMI

do-c7xl3.json - Base install of Centos 7.4 with Storidge CIO for DigitalOcean

do-u16.json - Base install of Ubuntu 16.04 with Storidge CIO for DigitalOcean

## Usage
Download templates
```
git clone https://github.com/Storidge/packer-cio.git
cd packer-cio
```
Add your AWS access id and secret key or DigitalOcean api token to the variables.json file, then run: 
```
vi variables.json
packer build -var-file variables.json <provider-os>.json
```

