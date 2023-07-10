---
layout: default
title: 11. Guest access
nav_order: 11
has_children: true
---

# 11. Guest access

Some service applications may support guest access. It is convenient for users as guest clients do not require registration. Let's see how guest access is implemented in Softnet. Traditionally, a guest client has no state on the server as it has no account. However, some client-server interaction scenarios require that clients preserve the state on the server between reconnections. Imagine that some client makes a request to the service, but the response might be ready after an indefinite period of time. When the requested data is ready, the service needs to deliver it to the client. In Softnet, services use Private events for this purpose. However, Private events can only be sent to stateful (registered) clients. So that guest clients could also receive Private events, they are implemented as stateful clients, each with an account on the server and unique URI. If a Softnet service supports a guest access mode, it is called a public service. Any person can find any public service in a Softnet network and create a stateful guest client without even being logged into the Softnet MS.  

Some service applications may not necessarily require for guest clients to be able to receive Private events. Such services can support stateless guest clients. This is convenient for Softnet users as it does not require the creation of an account for each guest client. Stateless clients connect to the site using a guest shared URI. Users can find it on the site management page.

Whether a client is a stateless guest client can be determined from its URI. Both regular clients and stateful guest clients have the URI scheme "softnet-s" for single-service clients and "softnet-m" for multi-service clients. For example, the following is a URI of a stateful single-service client: "softnet-s://yn52p0js2@ts.softnet-iot.org", and the following is a URI of a stateful multi-service client: "softnet-m://aw378v7t5@ts.softnet-iot.org". However, stateless guest clients have the URI scheme "softnet-ss" for single-service clients and "softnet-ms" for multi-service clients. For example, the following is a URI of a stateless single-service client: "softnet-ss://gn1560vs7@ts.softnet-iot.org", and the following is a URI of a stateless multi-service client: "softnet-ms://q2378ver1@ts.softnet-iot.org".  

When a Softnet user provides a client URI to a client application, the client app can determine if the URI is for a stateless guest client and can prompt the user whether it can operate as a stateless client or what features will not be available if the app is connected as a stateless client.