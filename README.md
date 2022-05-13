
<h3 align="center">Homarr</h3>
  <p align="center">
<img align="end" width=500 src="https://user-images.githubusercontent.com/49837342/168315259-b778c816-10fe-44db-bd25-3eea6f31b233.png" />
  </p>
  <p align = "center">
    A homepage for <i>your</i> server.
  <br/>
  <a href = "https://github.com/ajnart/homarr/deployments/activity_log?environment=Production" > <strong> Demo ↗️ </strong> </a> • <a href = "#-installation" > <strong> Install ➡️ </strong> </a>
  <br />
  <br />
    <i>Join the discord!</i>
  <br />
    <a href = "https://discord.gg/aCsmEV5RgA" > <img src="https://discordapp.com/api/guilds/972958686051962910/widget.png?style=shield" > </a>
</p>


# 📃 Table of Contents
- [📃 Table of Contents](#-table-of-contents)
- [🚀 Getting Started](#-getting-started)
  - [ℹ️ About](#ℹ️-about)
  - [⚡ Installation](#-installation)
    - [Deploying from Docker Image 🐳](#deploying-from-docker-image-)
    - [Building from Source 🛠️](#building-from-source-️)
- [💖 Contributing](#-contributing)

<!-- Getting Started -->
# 🚀 Getting Started

## ℹ️ About

Homarr is a simple and lightweight homepage for your server, that helps you easily access all of your services in one place.
    
**[⤴️ Back to Top](#-table-of-contents)**

## ⚡ Installation

### Deploying from Docker Image 🐳
> Supported architectures: x86-64, ARM, ARM64

_Requirements_:
- [Docker](https://docs.docker.com/get-docker/)

**Standard Docker Install**
```sh
docker run --name homarr -p 7575:7575 -v /data/docker/homarr:/app/data/configs -d ghcr.io/ajnart/homarr:latest
```

**Docker Compose**
```yml
---
version: '3'
#--------------------------------------------------------------------------------------------#
#                               Homarr -  A homepage for your server.                        #
#--------------------------------------------------------------------------------------------#
services:
  homarr:
    container_name: homarr
    image: ghcr.io/ajnart/homarr:latest
    restart: unless-stopped
    volumes:
      - /data/docker/homarr:/app/data/configs
    ports:
      - '7575:7575'
```

***Getting EACCESS errors in the logs? Try running `sudo chmod 775 /directory-you-mounted-to`!***

### Building from Source 🛠️

_Requirements_:
- [Git](https://git-scm.com/downloads)
- [NodeJS](https://nodejs.org/en/) _(Latest or LTS)_
- [Yarn](https://yarnpkg.com/)

**Installing**

- Clone the GitHub repo: `git clone https://github.com/ajnart/homarr.git` & `cd homarr`
- Install all dependencies: `yarn install`
- Build the source: `yarn build`
- Start the NextJS web server: ``yarn start``
- *Note: If you want to update the code in real time, launch with ``yarn dev``*

# 💖 Contributing
**Please read our [Contribution Guidelines](/CONTRIBUTING.md)**

All contributions are highly appreciated.
    
**[⤴️ Back to Top](#-table-of-contents)**
