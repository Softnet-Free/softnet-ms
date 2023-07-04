---
layout: default
title: 9. Users & access rights
nav_order: 9
has_children: true
---

# 9. Users & access rights

A domain user is an entity to which you assign access rights for various services in a domain. Initially, a domain contains two integrated users, **Owner** and **Guest**. You cannot delete them, but can only disable or enable. Owner is a generic user that represents the project owner. Typically, this is the most authoritative user in a domain. Clients associated with Owner interact with services deployed in the domain on behalf of the project owner. Guest is a generic user that represents all anonymous clients. In addition, you can create Private users and Contact users. A Private user is not necessarily associated with a real person. For example, you can create it for client devices deployed in real-world environments and assign it as few permissions as possible. On the other hand, a Contact user is associated with one of your partners. If you want to give your partner access to your devices, you are advised to use Contact users.  

This chapter uses a [demo project]({{ site.baseurl }}{% link docs/users/demo.md %}) containing various devices as an example to demonstrate how to manage users and access rights.
