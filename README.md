# Packer Templates for Storidge CIO
This repo contains [Packer](https://www.packer.io/) templates for generating AWS AMIs and DigitalOcean snapshot images with [Storidge CIO](http://storidge.com/docs/) software. 

## Templates

aws-c7xl3.json - Base install of Centos 7.4 with Storidge CIO for AWS AMI

aws-u16.json - Base install of Ubuntu 16.04 with Storidge CIO for AWS AMI

do-c7xl3.json - Base install of Centos 7.4 with Storidge CIO for DigitalOcean

do-u16.json - Base install of Ubuntu 16.04 with Storidge CIO for DigitalOcean

## Usage

Add your AWS access id and secret key or DigitalOcean api token to the variables.json file, then run: 

```
git clone https://github.com/Storidge/packer-cio.git
cd packer-cio
packer build -var-file variables.json <provider-os>.json
```

