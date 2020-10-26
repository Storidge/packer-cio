# Packer Templates for Storidge CIO
This repo contains [Packer](https://www.packer.io/) templates for generating AWS AMIs and DigitalOcean snapshot images with the community edition of the [Storidge CIO](http://storidge.com/docs/) software.

## Latest Supported CIO Version

2.0.0-3411

All supported versions can be found at: http://download.storidge.com/pub/ce/

## Templates

aws-c7xl3.json 	- Base install of Centos 7.4 with Storidge CIO for AWS AMI

aws-u20.json 		- Base install of Ubuntu 20.04 with Storidge CIO for AWS AMI

aws-u16.json 		- Base install of Ubuntu 16.04 with Storidge CIO for AWS AMI

aws-u18.json 		- Base install of Ubuntu 18.04 with Storidge CIO for AWS AMI

aws-u20.json    - Base install of Ubuntu 20.04 with Storidge CIO for AWS AMI

aws-k8s-c7xl3.json - Base install of Centos 7.4 with Kubernetes 1.18 for AWS AMI

aws-k8s-u18.json - Base install of Ubuntu 18.04 with Kubernetes 1.18 for AWS AMI

do-c7xl3.json 	- Base install of Centos 7.4 with Storidge CIO for DigitalOcean

do-u16.json 		- Base install of Ubuntu 16.04 with Storidge CIO for DigitalOcean

do-u18.json 		- Base install of Ubuntu 18.04 with Storidge CIO for DigitalOcean

do-u20.json     - Base install of Ubuntu 20.04 with Storidge CIO for DigitalOcean

eks-1.18-cio-c7xl3.json - Base install of Centos 7.4 with Storidge CIO and Kubernetes 1.18 for AWS EKS AMI

eks-1.18-cio-u18.json - Base install of Ubuntu 18.04 with Storidge CIO and Kubernetes 1.18 for AWS EKS AMI

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
