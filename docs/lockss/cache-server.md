---
layout: default
title: Cache Server
parent: LOCKSS
---
<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
Cache Daemon Release Notes
--------------------------

LOCKSS periodically releases new Daemon versions. Some releases are pure bug fixes others include new features. Our [Daemon Release Notes](https://wiki.metaarchive.org/metawiki/index.php/CacheDaemon_ReleaseNotes) page summarizes the changes that are relevant to the MetaArchive network.

Cache Purchasing
----------------

In order to keep the workloads as reasonable as possible at each member institution, the MetaArchive Cooperative makes a selection of one hardware configuration in October of each year, and supports the installation and maintenance of the network's software across all of the servers in the network that adopt that configuration. The current hardware Technical Specifications can be obtained [here](http://www.metaarchive.org/public/resources/charter_member/ma_2014technicalspecifications.pdf)

Member institutions that choose to implement this hardware gain the assistance of the MetaArchive central staff and extended community in the installation, maintenance, and troubleshooting of their preservation server. This substantially decreases the burden of work on the local systems administrators at member sites.

The MetaArchive identifies a vendor with the most competitive product that meets our current Technical Specifications. For new Member institutions that must provide additional documentation to their Office of Procurement to justify purchases from such vendors in the event they are not registered with their institution, the MetaArchive is providing a [Sole Source Checklist](http://www.metaarchive.org/public/resources/for_members/Sole_Source_Procurement.doc) to facilitate purchase from our preferred vendor.

Cache Setup
-----------

1.  The member institution provides an IP and domain name for the new cache.
2.  MetaArchive staff makes sure the new cache has access to the MetaArchive configuration files
3.  MetaArchive staff updates the IP lists used by web server administrators at member institutions to maintain firewall rules allowing the new cache to access memeber content.
4.  MetaArchive Staff provides an ISO and install instructions [Cache Configuration](https://wiki.metaarchive.org/metawiki/index.php/Cache_Configuration)

Cache Access, Ports, and Firewalls
----------------------------------

The LOCKSS daemon's web interface runs on port 8081. Caches communicate with each other by sending and receiving messages on port 9729. Caches provide port 8080 as a proxy port for preserved content, useful when content needs to be restored. Port 22 is used to ssh into a cache.

For proper monitoring by the central staff port 8081 needs to be opened to administrative servers. For network communication to work smoothly administrators need to make sure that port 9729 of the caches under their supervision are open to all other cache IPs in the network.

The relevant IP addresses are hosted at two urls. Detailed instructions about how to use these IP lists can be found in the README file at the bottom of the lists:

1.  [admin.metaarchive.org/protected/network/ips](http://admin.metaarchive.org/protected/network/ips). Access to this list requires use of the relevant login/pass on our [Credentials](https://wiki.metaarchive.org/metawiki/index.php/Credentials) page.
2.  [admin.metaarchive.org/network/ips/](http://admin.metaarchive.org/network/ips). Access to this list is open to all of the caches in the network.

Cache Maintenance
-----------------

Occasionally MetaArchive staff ask system administrators to perform local administration tasks. This happens infrequently. It usually involves executing specific command or scripts provided by MetaArchive staff.

The commands needed to perform maintenance tasks are detailed in [CachesMaintain](https://wiki.metaarchive.org/metawiki/index.php/CachesMaintain)

Cache Bandwidth
---------------

-   The bandwidth for the cache has two parts.
-   There is almost always a low amount of bandwidth being used for communications with the other caches. Short messages are constantly sent back and forth. A very busy cache might send and receive 300-400 Mbytes of data in a week in these messages.
-   The second part is when the cache needs to ingest content. This is generally a lot of bandwidth over short periods of time. Your cache might need to receive from a few GBytes of data, to hundreds of Gbytes over just a day or two. Right now this ingest happens maybe once or twice a month at most.
-   When it comes to bandwidth the peak usage comes when our members are having their own content ingested by the other caches in the network. But this is not an issue for your Lockss cache, it will be an issue for you content server.

Cache Monitoring
----------------

Some of our members use Nagios to monitor their servers. A suggested configuration for metaarchive/LOCKSS caches can be found at [CacheNagios](https://wiki.metaarchive.org/metawiki/index.php/CacheNagios)