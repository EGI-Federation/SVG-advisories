---
title: Advisory-EGI-SVG-2024-25
permalink: /Advisory-EGI-SVG-2024-25
  
published: false
---

## Advisory-EGI-SVG-2024-25

# perfSONAR configuration change recommendation 

PerfSonar by default enables a public webserver endpoint that proxies the prometheus node_exporter, 
thereby publishing excessive system information.

We do not assign a risk level to this vulnerability at this time, because it would depend on what is 
published exactly, not only today, but also after future updates of components involved.

We consider it bad practice to serve - by default - such extensive system information to the world.

## IDs AND CVSS SCORE      

EGI SVG ID : EGI-SVG-2024-25
    
CVE ID     : N/A

CVSS Score : N/A
    
## AFFECTED SOFTWARE AND VERSIONS
    
All versions of perfSONAR are affected.

## ACTIONS REQUIRED/RECOMMENDED

Sites running perfSonar are recommended to consider carrying out mitigation, 
see MITIGATION below unless this disables functionality required.

If anyone becomes aware of any situation where this information exposure has a significant 
impact on the EGI infrastructure then please inform EGI SVG.

## MITIGATION

Sites can mitigate by disabling the node_exporter service:

```
systemctl stop node_exporter.service
systemctl disable node_exporter.service
```

Alternatively the service can be firewalled to allow only trusted hosts/domains.
    
Lastly Prometheus can be configured to log less information [R 2].

## MORE INFORMATION

The perfsonar-host-metrics package creates a public webserver endpoint at https://<perfsonar host>/node_exporter/metrics (via apache) 
which proxies an instance of prometheus node_exporter. This endpoint provides excessive system information.

    
## STATUS OF THIS ADVISORY
                      
_TLP:CLEAR information - Unlimited distribution_ 

https://advisories.egi.eu/Advisory-EGI-SVG-2024-25

Minor updates may be made without re-distribution to the sites.

## CONTACT AND OTHER INFORMATION ON SVG

-----------------------------
    This advisory is subject to the Creative Commons licence 
    https://creativecommons.org/licenses/by/4.0/ and
    the EGI (https://www.egi.eu/) Software Vulnerability Group 
    must be credited.
-----------------------------

    
Comments or questions should be sent to
	svg-rat at mailman.egi.eu

Vulnerabilities relevant for EGI can be reported at
	report-vulnerability at egi.eu
    
(see [R 99] for further details, and other information on SVG)
    
    
## REFERENCES

- [R 1] <https://docs.perfsonar.net/manage_daemons.html?highlight=exporter>

- [R 2] https://prometheus.io/docs/prometheus/latest/configuration/configuration/

- [R 99] <https://confluence.egi.eu/display/EGIBG/SVG+Advisories>
