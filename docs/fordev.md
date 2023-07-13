---
layout: default
title: 13. For developers
nav_order: 13
---

# 13. For developers

A service application, when it connects to a blank site for the first time, supplies a **Site Structure** object to the platform, which uses it to build the structure of the site. Whenever the service application reconnects to the site, the platform verifies if the current Site Structure object attached to the service app matches the original one that was used to build the site structure. Typically, if the service application is the same, then the Site Structure object is always the same as well. However, if you are a developer and you are developing a service application utilizing the Softnet platform, things might be different.  

The Site Structure contains elements and declarations used to build the site with the structure needed for the service interface. And the service interface, as you know, is indicated by the names of the **service type** and **contract author**, which are also elements of the Site Structure. In Softnet MS, they are displayed in the following format: &lt;<span class="text-st">service type</span>&gt; (&lt;<span class="text-st">contract author</span>&gt;). During application development, you may change the content of the Site Structure object, and the next time you connect the application to the site for testing purposes, you can get an error status for the service entity on the site. 