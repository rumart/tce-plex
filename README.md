This repository contains the files used for getting Plex Media server up and running on a Tanzu Community Edition (TCE) cluster

For more information about the project please visit my [blog post here](https://rudimartinsen.com/2022/01/28/tce-plex)

A brief explanation of the files

## cluster

The management and workload cluster configuration files. For more information about deploying TCE cluster check out this blog

## storage class

The storage class utilizing the vSphere CSI pointing to a vSphere datastore for dynamically creating PVC's

## packages

This includes the config files for the individual Tanzu packages used in the solution. Before deploying those the metallb.yaml file should be applied to deploy the MetalLB load balancer

## plex

These files are explained in the blog post mentioned previously and will deploy a Plex media server mounting media files from an external NFS server, a Plex exporter that Prometheus can scrape metrics from, and a Grafana dashboard for visualizing the metrics