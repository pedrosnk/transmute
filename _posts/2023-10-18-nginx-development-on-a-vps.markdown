---
layout: post
title:  Nginx development in a docker with a vps
date:   2023-10-18 10:20:00 -0400
---

## Using the a VPS to store my application

Beign a hacker I've seen the necessity to create and deploy and expose applications I'm working
on, neither by having fun or by trying to do somehitng serious. This is part of what I do daily.
And being part of my daily work I'd like to not be limited to do only work that's important to
the company that hires me. I'd love to do all kind of explorations and experimentations on my
own pace. That's why I see myself as a passionate software engineer.

Being a passionate software engineer also means I need to look for more than one way of doing the
same thing and decide which better solves the problems I'm facing on. It is hard to not do that
with lots of experimentations. That's why, to simplify the work I'm doing right now I'm basically
using a VPS with a nginx that serves as a request routers to my applications. Those applications
run on a docker containers on my local VPS and they all use a local postgres database that runs
on the same VPS.

The case of using Nginx as a simple proxy is because it is just simple to setup and configure.
Basically you can just use the official nginx docker image and expose the default ports (80/443)

```docker
FROM nginx:latest

EXPOSE 80
EXPOSE 443
```

You cam also have a folder with all your config that nginx loads. On this configs you place the
route to oher apps. As long as they expose their ports as well. on this config files you have the
map of each subdomain to each exposed app. My personal favorite way is to have a folder called
`nginx` which is copied over to the docker image itself. So the Docker file becomes something like
this:

```Docker
FROM nginx:latest

COPY nginx /etc/nginx

EXPOSE 80
EXPOSE 443
```

Over there we can have the global config with the defined routes to other applications.
