---
title: "BGP Quagga to Fortinet CLI Equivalent"
excerpt_separator: "<!--more-->"
categories:
  - Commands
tags:
  - BGP
  - Quagga
  - Fortinet
---


Some equivalent commands from BGP Quagga to Fortinet CLI.

The BGP Quagga commands are the first in <font color="#52adc8">blue</font>, the Fortinet CLI commands are in <font color="#62c462">green</font>.

### Show BGP routing table:

sh ip bgp
{: .notice--info}

get router info bgp network
{: .notice--success}


### Show BGP nighbors summary:

sh ip bg summary
{: .notice--info}

get router info bgp summary
{: .notice--success}


### Show Advertised-routes for BGP neighbor IP 172.0.0.1:

sh ip bgp neighbors 172.0.0.1 advertised-routes
{: .notice--info}

get router info bgp neighbors 172.0.0.1 advertised-routes
{: .notice--success}


### Show Received-routes from BGP neighbor IP 172.0.0.1:

sh ip bgp neighbors 172.0.0.1 received-routes
{: .notice--info}

get router info bgp neighbors 172.0.0.1 routes
{: .notice--success}


### Clear routes received / advertised for BGP neighbor IP 172.0.0.1:

clear ip bgp 172.0.0.1 soft out/in
{: .notice--info}

exe router clear bgp ip 172.0.0.1 soft out/in
{: .notice--success}







