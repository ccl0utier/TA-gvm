# Technical Add-on for Greenbone Vulnerability Manager

## Overview

### About the Technical Add-on for Greenbone Vulnerability Manager

|                       |                                                         |
|-----------------------|---------------------------------------------------------|
| Version               | 1.0.0                                                   |
| Vendor Products       | Greenbone Community Edition (GCE). Others are untested. |
| Visible in Splunk Web | No.                                                     |

The **Technical Add-on for Greenbone Vulnerability Manager** collects vulnerability scan and operational log data from Greenbone Vulnerability Manager (GVM). You can install the Add-on on a forwarder to send data from GVM to a Splunk Enterprise indexer or group of indexers. You can also use the add-on to provide data for other apps, such as Splunk Enterprise Security.

The **Technical Add-on for Greenbone Vulnerability Manager** collects the following data using file inputs:

- Vulnerability Scan results sent from GVM to Splunk as scan tasks are completed.
- Changes to various GVM services log files in the `/var/log/gvm` directory and subdirectories.

### Source types for the Technical Add-on for Greenbone Vulnerability Manager

The **Technical Add-on for Greenbone Vulnerability Manager** provides index-time, search-time and CIM normalization for GVM vulnerability scan results, authentication, tasks and operational data in the following formats:

| Source Type                | Description                                             | CIM Data Models    |
|----------------------------|---------------------------------------------------------|--------------------|
| greenbone:gsm:scan         | Vulnerability Scan Results (parsed from XML)            | Vulnerabilities    |
| greenbone:gsad:log         | Greenbone Security Assistant (GSA) logs                 | Authentication     |
| greenbone:gvmd:log         | Greenbone Vulnerability Manager Daemon (GVMD) logs      | n/a                |
| greenbone:openvas:log      | OpenVAS Scanner logs                                    | n/a                |
| greenbone:ospd-openvas:log | OSP Scanner logs                                        | n/a                |

### Compatibility

This version of the add-on is compatible with the following platform, OS and CIM versions:

|                                  |                      |
|----------------------------------|----------------------|
| Splunk Platform                  | 8.x and later        |
| CIM                              | 4.2 and later        |
| Supported OS for data collection | Any supported by GCE |

## Installation

_TBC_

## Configuration

_TBC_

## Credits, References & Notes

This add-on was loosely based on the original [App](https://download.greenbone.net/tools/Greenbone-Splunk-App-1.0.1.tar.gz) built by Greenbone Networks Gmbh. which is documented [here](https://docs.greenbone.net/GSM-Manual/gos-21.04/en/connecting-other-systems.html#setting-up-the-greenbone-splunk-app).

 “Greenbone” is a trademark of Greenbone Networks GmbH and they are in no way affiliated with this work.  Any rights, title and interest in these trademarks remains solely with them.

> Author: Christian Cloutier <ccloutier@splunk.com>