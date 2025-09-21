---
layout: post
title: "Projects & Technical Skills"
subtitle: "A showcase of my hands-on experience with cloud-native technologies"
cover-img: /assets/img/code-background.jpg
tags: [projects, devops, terraform, kubernetes, aws, docker]
author: David Gitman
---

This page provides a deeper look into my technical capabilities, highlighting a key project and the primary tools I use to build and manage modern infrastructure. My approach is hands-on, focusing on automation and creating resilient, scalable systems.

---

## Featured Project: Automated Home Media Server

To sharpen my skills in a practical environment, I built a fully automated personal media server using Docker. This "homelab" project mirrors a real-world microservices architecture and reinforces core DevOps principles.

{: .box-note}
**Objective:** Create a self-hosted, personal streaming service that automatically manages and serves media content, all defined as code.

The entire system is orchestrated with a single **Docker Compose** file, making the environment reproducible and easy to manage.

Key services include:
* **Plex:** For streaming media to any device.
* **Sonarr & Radarr:** To automate the management of TV shows and movies.

This setup is a practical application of containerization and automation, running 24/7 in a lightweight Linux environment.

### Core Configuration (`docker-compose.yml`)

Here’s a simplified snippet of the configuration that defines the Plex service. The full setup includes multiple interconnected containers.

{% highlight yaml linenos %}
version: "3.7"
services:
  plex:
    image: lscr.io/linuxserver/plex:latest
    container_name: plex
    network_mode: host
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Asia/Jerusalem
    volumes:
      - /path/to/your/plex/config:/config
      - /path/to/your/media/tv:/tv
      - /path/to/your/media/movies:/movies
    restart: unless-stopped
{% endhighlight %}

---

## Core Technology Stack

My skills are centered around the modern tools necessary for building and maintaining cloud-native applications and infrastructure.

| Category | Key Technologies |
| :--- | :--- |
| **Infrastructure as Code** | Terraform, Ansible, Helm |
| **Containerization** | Docker, Kubernetes (EKS) |
| **CI/CD** | Jenkins, GitHub Actions |
| **Cloud Platforms** | Amazon Web Services (AWS), Google Cloud Platform (GCP) |
| **Monitoring & Logging**| Kibana, Elasticsearch, Prometheus, Grafana |
| **Scripting** | Bash, Python |

My experience at companies like **Wix** and **Devalore** has allowed me to apply these skills at scale, contributing to robust backend systems and leading complex DevOps initiatives.
