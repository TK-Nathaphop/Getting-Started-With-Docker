# Microservices and the Real World

## Docker Module Overview from course

- Cloud-native Microservices
- Multi-container apps with Docker Compose
- Docker Swarm, alternative from Kubernetes
- Docker Services
- Multi-container apps with Docker Stacks

## Cloud-native Microservices

**Why Microservices?**

If we keep everything in 1 app, when we want to patch something, it needs to update the whole app. Which is quite worse and hard to scalable something. So, this is how Microservices design pattern become. It’s better to make many things independently and easy to scalable without breaking another thing.

**Cloud-native != only run in cloud**

Actually, we can use anything e.g. cloud services, private/public cloud, or on-prem data center

**What is on-cloud? on-prem ?**

- Cloud is an IT system that has Cloud provider to take care of it and can access through internet.
- But while on-prem (On-premise) is an IT system that host on some place that need to take care by owner e.g. server in CPE KMUTT.

In the past, many companies use on-prem because on-cloud is not popular as much as now. But when we drive into the era of the big data and have a lake of the data. if still invest with the on-prem, it could cause a lot of money for take care or could cost for over spec without using it that high. So, if we change it to on cloud, we can reduce or increase server spec at anytime.

Ref: https://www.coraline.co.th/single-post/on-cloud-vs-on-premise

**Multi-container apps with Docker Compose**
`docker-compose` → Set config for docker to manage

Better than remember all command and easier to track multi-container app.
