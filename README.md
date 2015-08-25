# Clickberry Web Services
A set of micro-services powering video portal.

![](assets/Architecture.png?raw=true)

* Reliable. Even if one service is down the rest of the system is on.
* Easy to update, test, deploy and scale each service independently.
* Easy to add new functionality by developing new services.
* No Single-Point-of-Failure.
* Mix of technologies, platforms and languages: the best tech. stack for each service.
* Platform independent: can be hosted on AWS, Google, Heroku, Digital Ocean, Azure or even on a on-premises hardware.
* Open Source.
* Mobile-first Web UI.
* Rest API for Web, Mobile Devices, IoT and Desktop apps.
* Hybrid video encoder: cloud and on-premises hardware together.
* Great?

## Bus
In the heart of the web services there is a messaging service called Bus. We use [NSQ](http://nsq.io) as a distributed realization of messaging service for our application. Since NSQ is distributes, we usually instantiate several `nsqd` instances registered in a few `nsqlookupd` routers. 

We use special [nsqd-ecs](//github.com/clickberry/nsqd-ecs) ecs-optimized docker image which allows us easily scale up and down number of running nsqd instances.

## [Auth. API](//github.com/clickberry/auth-api-nodejs)
JWT-based authentication service.

## [Email Service](//github.com/clickberry/email-service-python)
Email notification service.

## Contacts
support@clickberry.com
