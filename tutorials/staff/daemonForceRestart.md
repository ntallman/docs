---
layout: default
title: Restart All Daemons
parent: Staff Tutorials
grand_parent: Tutorials
---

The daemon can make most configuration changes on the fly, but some configuration parameterss are only read at startup from the title database. It takes a restart to force existing AUs to start using an updated plugin.

To cause all the daemons in your network to exit and restart, set org.lockss.app.exitOnce to true, wait twice the time defined in org.lockss.config.reloadInterval (or more) then set it back to false.

Daemons exit when the see exitOnce transition from false to true. (If it's true when they start, they won't exit until it goes false, then true again.) Daemons check for prop changes approximately every reloadInterval - there's some randomization applied, so you have to wait longer than that interval to make sure all daemons have seen the change. Two times the interval is probably longer than necessary, but safe.