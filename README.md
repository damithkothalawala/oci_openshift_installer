# oci_openshift_installer
Install RedHat OpenShift 4.9 on Oracle Cloud Infrastructure

## Simplified Diagram 
![Simplified Diagram](https://github.com/damithkothalawala/oci_openshift_installer/raw/main/images/simplified.png)

## Full Map
Or open https://raw.githubusercontent.com/damithkothalawala/oci_openshift_installer/main/images/diagram.digraph using [GraphvizOnline](https://dreampuf.github.io/GraphvizOnline)

![Full Map](https://github.com/damithkothalawala/oci_openshift_installer/raw/main/images/graphviz.svg)


Please Note that you should use Oracle Cloud Shell to execute this TF script. And make sure to have ssh key pairs on your cloud shell environment or use ssh-keygen command to generate key pairs. Provided *terraform.tfvars* file is an example only. You should fill it with your values and Live ISO image on OpenShift Assisted Installer Wizard. 

This installer is compatible with https://console.redhat.com/openshift assisted cluster installation method. And you would need to terminate and re-create nodes with preserved boot volumes per each node manually.

This release not yet hardened with tight security for public subnet (port 22/80 and 443 is open to the world)

I assume that whoever going to do this on their tenant is having enough privileges to create resources on OCI and you already have a registered DNS to be used with this deployment

K8s api only exposed to internal cluster network and please open it to public internet via public loadbalancer at your own risk. 

This script will create sub compartment inside given compartment (just give tenancy id as compartment if you want it under 1 level down) to have clean installation and to make it easy to clean up whenever you are done.

[![Installation Guide](https://img.youtube.com/vi/9njc_7GJIoc/0.jpg)](https://www.youtube.com/watch?v=9njc_7GJIoc)

You should watch this video https://www.youtube.com/watch?v=9njc_7GJIoc before starting the installation
