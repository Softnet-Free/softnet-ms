---
layout: default
title: 13. For developers
nav_order: 13
---

# 13. For developers

A service application that uses the Softnet platform provides the site with a **Site Structure** object when it first connects to the blank site. Softnet uses this object to build the structure of the site. Whenever the service application reconnects, the site verifies if the current Site Structure object attached to service endpoint matches the original one that was used to build the structure of the site. If the service application that connects to the site is the same, then the Site Structure object is always the same as well.
