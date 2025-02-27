# Clickberry Web Services
A set of micro-services powering a video portal.

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
In the heart of the web services there is a messaging service called Bus. We use [NSQ](http://nsq.io) as a distributed realization of messaging service for our application. Since NSQ is distributed, we usually instantiate several `nsqd` instances registered in a few `nsqlookupd` routers. 

We use special ecs-optimized [nsqd](//github.com/clickberry/nsqd-ecs) docker images which allows us easily scale up and down the Bus, because they automatically retrieve their public IP addresses and registers them in nsqlookupd.

## [Auth. API](//github.com/clickberry/auth-api-nodejs)
JWT-based authentication micro-service.

## [Email Service](//github.com/clickberry/email-service-python)
Email notification micro-service.

## [Profiles API](//github.com/clickberry/profiles-api-nodejs)
Profiles API micro-service.

## [Profiles Service](//github.com/clickberry/profiles-service-nodejs)
Profiles worker micro-service.

## [Comments API](//github.com/clickberry/comments-api-nodejs)
Comments API micro-service.

## [Metadata API](//github.com/clickberry/metadata-api-nodejs)
Metadata API micro-service.

## [Videos API](//github.com/clickberry/videos-api-nodejs)
Video encoding proxy micro-service on Node.js.

## [Images API](//github.com/clickberry/images-api-nodejs)
Images API micro-service on Node.js.

## [Projects API](//github.com/clickberry/projects-api-nodejs)
Projects API micro-service.

## [Projects Service](//github.com/clickberry/projects-service-nodejs)
Projects worker micro-service.

## [Projects admin API](//github.com/clickberry/projects-admin-api-nodejs)
Projects admin API micro-service.

## [Users admin API](//github.com/clickberry/users-admin-api-nodejs)
Users admin API micro-service.

## [Users admin Service](//github.com/clickberry/users-admin-service-nodejs)
Users admin worker micro-service.

## Contacts
support@clickberry.com
