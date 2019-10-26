# Packer Templates for Storidge CIO
This repo contains [Packer](https://www.packer.io/) templates for generating AWS AMIs and DigitalOcean snapshot images with the community edition of the [Storidge CIO](http://storidge.com/docs/) software.

## Latest Supported CIO Version

1.0.0-3007

All supported versions can be found at: http://download.storidge.com/pub/ce/

## Templates

aws-c7xl3.json 	- Base install of Centos 7.4 with Storidge CIO for AWS AMI

aws-u16.json 		- Base install of Ubuntu 16.04 with Storidge CIO for AWS AMI

aws-u18.json 		- Base install of Ubuntu 18.04 with Storidge CIO for AWS AMI

do-c7xl3.json 	- Base install of Centos 7.4 with Storidge CIO for DigitalOcean

do-u16.json 		- Base install of Ubuntu 16.04 with Storidge CIO for DigitalOcean

do-u18.json 		- Base install of Ubuntu 18.04 with Storidge CIO for DigitalOcean

## Usage
[Download Packer](https://www.packer.io/downloads.html)

Download templates:
```
git clone https://github.com/Storidge/packer-cio.git
```
Modify `variables.json` file:
```
cd packer-cio
cp variables.json.template variables.json
```
Add your AWS access id and secret key or DigitalOcean api token to `variables.json`.
Make sure to check that the build number is valid then run:
```
packer validate -var-file variables.json <template>
```
If there are no errors, run the following command to build:
```
packer build -var-file variables.json <template>
```
