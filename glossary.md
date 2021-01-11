---
layout: default
title: Glossary
---
This page contains short definitions of LOCKSS/MetaArchive specific terms. Where appropiate we link to wikipedia for the definition of general technology terms for the less technical reader.

<dl>
  <dt>Archive</dt>
  <dd>a subject or genre-based grouping of content (e.g., Southern Digital Culture, Electronic Theses and Dissertations)</dd>
  <dt>Archival Unit (AU)</dt>
  <dd>an independent collection of content in a LOCKSS cache. LOCKSS daemons create AUs by crawling a website using the AU's plugin and parameters. AUs are maintained by daemons as a unit via crawling, recrawling, polling and voting</dd>
  <dt>Cache</dt>
  <dd>or LOCKSS cache server running the LOCKSS daemon software which participates in a LOCKSS network</dd>
  <dt>Cache Manager</dt>
  <dd> A web based software tool which queries LOCKSS caches about their status and presents the information in a web based user interface. It incorporates command line report generators.</dd>
  <dt>CLOCKSS</dt>
  <dd>or Controlled LOCKSS, a community-governed partnership of libraries and publishers working to achieve a sustainable, globally-distributed archive, see http://www.clockss.org/clockss</dd>
  <dt>Conspectus</dt>
  <dd>A web based tool developed for the NDIIPP MetaArchive project that maintains information about collections preserved in the network along with LOCKSS specific collection configuration settings.</dd>
  <dt>Crawl Rules Plugins </dt>
  <dd>contain crawl rules which define which URLs encountered in a daemon's web crawl are ingested/copied by the local disk of the daemons cache.</dd>
  <dt>Ingest(ing)</dt>
  <dd>LOCKSS daemons ingest/copy content from URLs when they crawl content with the help of a plugin. Content is copied as it is retrieved from content servers via http gets. Daemons do not encrypt or compress copied content.</dd>
  <dt>LOCKSS daemon </dt>
  <dd>A daemon executing the LOCKSS software usually on a dedicated LOCKSS cache</dd>
  <dt>Library Cache Auditing Protocol (LCAP)</dt>
  <dd>A very slow-acting network communication protocol used by LOCKSS daemons to communicate with each other in Votes and Polls.</dd>
  <dt>LOCKSS</dt>
  <dd>LOCKSS (Lots Of Copies Keep Stuff Safe) is an open source, peer-to-peer, decentralized digital preservation infrastructure, see http://www.lockss.org/lockss</dd>
  <dt>LOCKSS network</dt>
  <dd>A network of LOCKSS caches that are maintained with a common title database</dd>
  <dt>Manifest Page</dt>
  <dd>The LOCKSS Crawler requests explicit permission to harvest content which it locates in so called manifest pages, see http://www.lockss.org/lockss/Publisher_Manifest_Page</dd>
  <dt>MetaArchive</dt>
  <dd>The Private LOCKSS Network that is behind this wiki.</dd>
  <dt>Network</dt>
  <dd>The Cooperative's community of LOCKSS caches</dd>
  <dt>Plugin</dt>
  <dd>A small XML file that instructs the LOCKSS software how to crawl, in terms of defining a starting URL, where to look for Manifest Pages, and how to decide which URLs to ingest/copy from the content providing web site</dd>
  <dt>Plugin Identifier </dt>
  <dd>JAVA style identifier, eg org.lockss.ingest, that identifies a plugin uniquely in a LOCKSS network</dd>
  <dt>Plugin Name</dt>
  <dd>short descriptive name for your plugin</dd>
  <dt>Plugin Repository </dt>
  <dd>LOCKSS daemons are configured to read plugin definitions from a web accessible plugin repositories. Plugins are deployed to plugin repositories as signed and jared files.</dd>
   <dt>PluginTool</dt>
  <dd>Java application that simplifies the creation of new LOCKSS plugins, see http://www.lockss.org/lockss/Plugin_Tool </dd>
</dl>