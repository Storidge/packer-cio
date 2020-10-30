# Packer Templates for Storidge CIO
This repo contains [Packer](https://www.packer.io/) templates for generating AWS AMIs and DigitalOcean snapshot images with the community edition of the [Storidge CIO](http://storidge.com/docs/) software.

## Latest Supported CIO Version

2.0.0-3411

All supported versions can be found at: http://download.storidge.com/pub/ce/

## Templates

aws-c7xl3.json 	- AMI with Storidge CIO on Centos 7

aws-u20.json 		- AMI with Storidge CIO on Ubuntu 20.04

aws-u18.json 		- AMI with Storidge CIO on Ubuntu 18.04

aws-k8s-c7xl3.json - AMI with EKS 1.18 on Centos 7

aws-k8s-u18.json - AMI with EKS 1.18 on Ubuntu 18.04

do-c7xl3.json 	- DO image with Storidge CIO on Centos 7

do-u18.json 	- DO image with Storidge CIO on Ubuntu 18.04

do-u20.json   - DO image with Storidge CIO on Ubuntu 20.04

eks-1.18-cio-c7xl3.json - AMI with EKS 1.18, Storidge CIO on Centos 7

eks-1.18-cio-u18.json - AMI with EKS 1.18, Storidge CIO on Ubuntu 18.04

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
