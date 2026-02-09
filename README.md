# ![Juice Shop Logo](https://raw.githubusercontent.com/juice-shop/juice-shop/master/frontend/src/assets/public/images/JuiceShop_Logo_100px.png) OWASP Juice Shop

<p align="center">
  <em>Probably the most modern and sophisticated insecure web application</em>
</p>

[![OWASP Flagship](https://img.shields.io/badge/owasp-flagship%20project-48A646.svg)](https://owasp.org/projects/#sec-flagships)
[![GitHub release](https://img.shields.io/github/release/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![Twitter Follow](https://img.shields.io/twitter/follow/owasp_juiceshop.svg?style=social&label=Follow)](https://twitter.com/owasp_juiceshop)
[![Subreddit subscribers](https://img.shields.io/reddit/subreddit-subscribers/owasp_juiceshop?style=social)](https://reddit.com/r/owasp_juiceshop)

![CI/CD Pipeline](https://github.com/juice-shop/juice-shop/workflows/CI/CD%20Pipeline/badge.svg?branch=master)
[![Coverage Status](https://coveralls.io/repos/github/juice-shop/juice-shop/badge.svg?branch=develop)](https://coveralls.io/github/juice-shop/juice-shop?branch=develop)[![Cypress tests](https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/simple/3hrkhu/master&style=flat&logo=cypress)](https://dashboard.cypress.io/projects/3hrkhu/runs)
[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/223/badge)](https://www.bestpractices.dev/projects/223)
![GitHub stars](https://img.shields.io/github/stars/juice-shop/juice-shop.svg?label=GitHub%20%E2%98%85&style=flat)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

> [The most trustworthy online shop out there.](https://twitter.com/dschadow/status/706781693504589824)
> ([@dschadow](https://github.com/dschadow)) —
> [The best juice shop on the whole internet!](https://twitter.com/shehackspurple/status/907335357775085568)
> ([@shehackspurple](https://twitter.com/shehackspurple)) —
> [Actually the most bug-free vulnerable application in existence!](https://youtu.be/TXAztSpYpvE?t=26m35s)
> ([@vanderaj](https://twitter.com/vanderaj)) —
> [First you 😂😂then you 😢](https://twitter.com/kramse/status/1073168529405472768)
> ([@kramse](https://twitter.com/kramse)) —
> [But this doesn't have anything to do with juice.](https://twitter.com/coderPatros/status/1199268774626488320)
> ([@coderPatros' wife](https://twitter.com/coderPatros))

OWASP Juice Shop is probably the most modern and sophisticated insecure web application! It can be used in security
trainings, awareness demos, CTFs and as a guinea pig for security tools! Juice Shop encompasses vulnerabilities from 
the entire [OWASP Top Ten](https://owasp.org/www-project-top-ten) along with many other security flaws found in 
real-world applications!

![Juice Shop Screenshot Slideshow](screenshots/slideshow.gif)

For a detailed introduction, full list of features and architecture overview please visit the official project page:
<https://owasp-juice.shop>

## :warning: Security Warning

**OWASP Juice Shop is an intentionally insecure application!** It contains numerous security vulnerabilities that you 
would **never** want to introduce into a real production application. This application is designed for training 
purposes only and should never be used as a template for building real applications.

- **Do not host this application on public servers** unless you know exactly what you're doing
- **Do not use any code from this application** in production systems
- Running Juice Shop on your local machine or in an isolated environment is recommended
- Use at your own risk - this application will expose your system to security risks if improperly configured

## Quick Start

Get started with OWASP Juice Shop in less than 5 minutes:

```bash
# Using Docker (Recommended)
docker pull bkimminich/juice-shop
docker run --rm -p 3000:3000 bkimminich/juice-shop

# Or from source
git clone https://github.com/juice-shop/juice-shop.git --depth 1
cd juice-shop
npm install
npm start
```

Then browse to <http://localhost:3000> and start hacking!

## Features

- **100+ Hacking Challenges** covering all major vulnerability categories
- **OWASP Top 10 Coverage** - All current OWASP Top 10 vulnerabilities included
- **Realistic User Interface** - Modern web application built with Angular
- **Multiple Difficulty Levels** - From trivial to expert level challenges
- **Hacking Instructor** - Built-in tutorial mode for beginners
- **CTF Support** - Built-in CTF flag codes and integration with CTFd
- **Score Board** - Track your hacking progress
- **Multi-language Support** - Available in 40+ languages
- **Coding Challenges** - Find and fix vulnerable code snippets
- **Self-healing** - Application can restore itself after being compromised
- **Extensive Documentation** - Free companion guide with solutions
- **Realistic Scenarios** - E-commerce application with products, reviews, orders
- **API Endpoints** - RESTful API for additional attack surface
- **Web3/Blockchain Challenges** - Including NFT and smart contract vulnerabilities
- **Monitoring** - Prometheus metrics and Grafana dashboards
- **Customizable** - Easy to rebrand and customize for your training needs

## Table of contents

- [Security Warning](#warning-security-warning)
- [Quick Start](#quick-start)
- [Features](#features)
- [Setup](#setup)
    - [From Sources](#from-sources)
    - [Packaged Distributions](#packaged-distributions)
    - [Docker Container](#docker-container)
    - [Vagrant](#vagrant)
- [Demo](#demo)
- [Documentation](#documentation)
    - [Node.js version compatibility](#nodejs-version-compatibility)
    - [Pwning OWASP Juice Shop](#official-companion-guide)
    - [Troubleshooting](#troubleshooting)
- [Architecture](#architecture)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [References](#references)
- [Community & Support](#community--support)
- [Merchandise](#merchandise)
- [Donations](#donations)
- [FAQ](#faq)
- [Contributors](#contributors)
- [Licensing](#licensing)

## Setup

> You can find some less common installation variations as well as instructions to run Juice Shop on a variety of cloud computing providers in
> [the _Running OWASP Juice Shop_ documentation](https://pwning.owasp-juice.shop/companion-guide/latest/part1/running.html).

### From Sources

![GitHub repo size](https://img.shields.io/github/repo-size/juice-shop/juice-shop.svg)

1. Install [node.js](#nodejs-version-compatibility)
2. Run `git clone https://github.com/juice-shop/juice-shop.git --depth 1` (or
   clone [your own fork](https://github.com/juice-shop/juice-shop/fork)
   of the repository)
3. Go into the cloned folder with `cd juice-shop`
4. Run `npm install` (only has to be done before first start or when you change the source code)
5. Run `npm start`
6. Browse to <http://localhost:3000>

### Packaged Distributions

[![GitHub release](https://img.shields.io/github/downloads/juice-shop/juice-shop/total.svg)](https://github.com/juice-shop/juice-shop/releases/latest)
[![SourceForge](https://img.shields.io/sourceforge/dm/juice-shop?label=sourceforge%20downloads)](https://sourceforge.net/projects/juice-shop/)
[![SourceForge](https://img.shields.io/sourceforge/dt/juice-shop?label=sourceforge%20downloads)](https://sourceforge.net/projects/juice-shop/)

1. Install a 64bit [node.js](#nodejs-version-compatibility) on your Windows, MacOS or Linux machine
2. Download `juice-shop-<version>_<node-version>_<os>_x64.zip` (or
   `.tgz`) attached to
   [latest release](https://github.com/juice-shop/juice-shop/releases/latest)
3. Unpack and `cd` into the unpacked folder
4. Run `npm start`
5. Browse to <http://localhost:3000>

> Each packaged distribution includes some binaries for `sqlite3` and
> `libxmljs2` bound to the OS and node.js version which `npm install` was
> executed on.

### Docker Container

[![Docker Pulls](https://img.shields.io/docker/pulls/bkimminich/juice-shop.svg)](https://hub.docker.com/r/bkimminich/juice-shop)
![Docker Stars](https://img.shields.io/docker/stars/bkimminich/juice-shop.svg)
[![](https://images.microbadger.com/badges/image/bkimminich/juice-shop.svg)](https://microbadger.com/images/bkimminich/juice-shop
"Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/bkimminich/juice-shop.svg)](https://microbadger.com/images/bkimminich/juice-shop
"Get your own version badge on microbadger.com")

1. Install [Docker](https://www.docker.com)
2. Run `docker pull bkimminich/juice-shop`
3. Run `docker run --rm -p 127.0.0.1:3000:3000 bkimminich/juice-shop`
4. Browse to <http://localhost:3000> (on macOS and Windows browse to
   <http://192.168.99.100:3000> if you are using docker-machine instead of the native docker installation)

### Vagrant

1. Install [Vagrant](https://www.vagrantup.com/downloads.html) and
   [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
2. Run `git clone https://github.com/juice-shop/juice-shop.git` (or
   clone [your own fork](https://github.com/juice-shop/juice-shop/fork)
   of the repository)
3. Run `cd vagrant && vagrant up`
4. Browse to [192.168.56.110](http://192.168.56.110)

## Demo

Feel free to have a look at the latest version of OWASP Juice Shop:
<http://demo.owasp-juice.shop>

> This is a deployment-test and sneak-peek instance only! You are __not
> supposed__ to use this instance for your own hacking endeavours! No
> guaranteed uptime! Guaranteed stern looks if you break it!

## Documentation

### Node.js version compatibility

![GitHub package.json dynamic](https://img.shields.io/github/package-json/cpu/juice-shop/juice-shop)
![GitHub package.json dynamic](https://img.shields.io/github/package-json/os/juice-shop/juice-shop)

OWASP Juice Shop officially supports the following versions of
[node.js](http://nodejs.org) in line with the official
[node.js LTS schedule](https://github.com/nodejs/LTS) as close as possible. Docker images and packaged distributions are
offered accordingly.

| node.js | Supported              | Tested             | [Packaged Distributions](#packaged-distributions) | [Docker images](#docker-container) from `master` | [Docker images](#docker-container) from `develop` |
|:--------|:-----------------------|:-------------------|:--------------------------------------------------|:-------------------------------------------------|:--------------------------------------------------|
| 25.x    | :x:                    | :x:                |                                                   |                                                  |                                                   |
| 24.x    | :heavy_check_mark:     | :heavy_check_mark: | Windows (`x64`), MacOS (`x64`), Linux (`x64`)     |                                                  |                                                   |
| 23.x    | ( :heavy_check_mark: ) | :x:                |                                                   |                                                  |                                                   |
| 22.x    | :heavy_check_mark:     | :heavy_check_mark: | Windows (`x64`), MacOS (`x64`), Linux (`x64`)     | `latest` (`linux/amd64`, `linux/arm64`)          | `snapshot` (`linux/amd64`, `linux/arm64`)         |
| 21.x    | ( :heavy_check_mark: ) | :x:                |                                                   |                                                  |                                                   |
| 20.x    | :heavy_check_mark:     | :heavy_check_mark: | Windows (`x64`), MacOS (`x64`), Linux (`x64`)     |                                                  |                                                   |
| <20.x   | :x:                    | :x:                |                                                   |                                                  |                                                   |

Juice Shop is automatically tested _only on the latest `.x` minor version_ of each node.js version mentioned above!
There is no guarantee that older minor node.js releases will always work with Juice Shop!
Please make sure you stay up to date with your chosen version.

### Troubleshooting

[![Gitter](http://img.shields.io/badge/gitter-join%20chat-1dce73.svg)](https://gitter.im/bkimminich/juice-shop)

If you need help with the application setup please check 
[our existing _Troubleshooting_](https://pwning.owasp-juice.shop/companion-guide/latest/part4/troubleshooting.html)
guide. If this does not solve your issue please post your specific problem or question in the
[Gitter Chat](https://gitter.im/bkimminich/juice-shop) where community members can best try to help you.

:stop_sign: **Please avoid opening GitHub issues for support requests or questions!**

### Official companion guide

[![Write Goodreads Review](https://img.shields.io/badge/goodreads-write%20review-372213.svg)](https://www.goodreads.com/review/edit/49557240)

OWASP Juice Shop comes with an official companion guide eBook. It will give you a complete overview of all
vulnerabilities found in the application including hints how to spot and exploit them. In the appendix you will even
find complete step-by-step solutions to every challenge. Extensive documentation of
[custom re-branding](https://pwning.owasp-juice.shop/companion-guide/latest/part4/customization.html),
[CTF-support](https://pwning.owasp-juice.shop/companion-guide/latest/part4/ctf.html),
[trainer's guide](https://pwning.owasp-juice.shop/companion-guide/latest/part4/trainers.html)
and much more is also included.

[Pwning OWASP Juice Shop](https://leanpub.com/juice-shop) is published under
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)
and is available **for free** in PDF, Kindle and ePub format on LeanPub. You can also
[browse the full content online](https://pwning.owasp-juice.shop)!

[<img alt="Pwning OWASP Juice Shop cover" src="https://raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/cover.jpg" width="200"/>](https://leanpub.com/juice-shop)
[<img alt="Pwning OWASP Juice Shop back cover" src="https://raw.githubusercontent.com/juice-shop/pwning-juice-shop/master/docs/modules/ROOT/assets/images/introduction/back.jpg" width="200"/>](https://leanpub.com/juice-shop)

## Architecture

OWASP Juice Shop is a full-stack web application with the following architecture:

```
┌─────────────────────────────────────────────────────────────┐
│                        Frontend (Angular)                    │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐     │
│  │   Products   │  │    Basket    │  │   Account    │     │
│  │   Reviews    │  │   Checkout   │  │  Challenges  │     │
│  └──────────────┘  └──────────────┘  └──────────────┘     │
└─────────────────────────────────────────────────────────────┘
                            ↕ HTTP/REST API
┌─────────────────────────────────────────────────────────────┐
│                    Backend (Node.js/Express)                 │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐     │
│  │   Routes     │  │    Models    │  │     Lib      │     │
│  │  (REST API)  │  │  (Sequelize) │  │  (Business   │     │
│  │              │  │              │  │    Logic)    │     │
│  └──────────────┘  └──────────────┘  └──────────────┘     │
└─────────────────────────────────────────────────────────────┘
                            ↕
┌─────────────────────────────────────────────────────────────┐
│                    Database (SQLite)                         │
│  Users, Products, Baskets, Challenges, Reviews, etc.        │
└─────────────────────────────────────────────────────────────┘
```

### Key Components:

- **Frontend**: Single Page Application built with Angular 17+
- **Backend**: RESTful API built with Node.js and Express
- **Database**: SQLite3 for data persistence (easily replaceable)
- **ORM**: Sequelize for database abstraction
- **Authentication**: JWT tokens (with intentional vulnerabilities)
- **File Storage**: Local filesystem for uploads
- **WebSocket**: Socket.io for real-time notifications
- **Monitoring**: Prometheus metrics endpoint

## Technology Stack

### Backend
- **Runtime**: Node.js 20-24
- **Framework**: Express 4.x
- **Language**: TypeScript 5.x
- **Database**: SQLite3 (via Sequelize ORM)
- **Authentication**: JSON Web Tokens (JWT)
- **WebSocket**: Socket.io
- **Testing**: Mocha, Jest, Frisby
- **Validation**: express-validator
- **Security**: helmet, express-rate-limit (with bypasses)

### Frontend
- **Framework**: Angular 17+
- **Language**: TypeScript 5.x
- **UI Components**: Angular Material
- **State Management**: RxJS
- **HTTP Client**: Angular HttpClient
- **Testing**: Jasmine, Karma, Cypress
- **Build Tool**: Angular CLI / Webpack

### DevOps & Tools
- **Containerization**: Docker
- **CI/CD**: GitHub Actions
- **Code Quality**: ESLint, StyleLint
- **Test Coverage**: NYC (Istanbul), Coveralls
- **Security Scanning**: CodeQL, OWASP ZAP
- **Documentation**: Swagger/OpenAPI

### Additional Technologies
- **Web3/Blockchain**: ethers.js, Web3.js
- **Chatbot**: juicy-chat-bot
- **Internationalization**: i18n
- **PDF Generation**: PDFKit
- **Image Processing**: sharp
- **CAPTCHA**: svg-captcha

## Project Structure

```
juice-shop/
├── app.ts                      # Application entry point
├── server.ts                   # Server configuration
├── routes/                     # Express route handlers
│   ├── login.ts               # Authentication endpoints
│   ├── basket.ts              # Shopping basket API
│   ├── product.ts             # Product management
│   └── ...                    # Other API endpoints
├── models/                     # Sequelize database models
│   ├── user.ts                # User model
│   ├── product.ts             # Product model
│   └── ...                    # Other models
├── lib/                        # Business logic and utilities
│   ├── insecurity.ts          # Intentionally insecure functions
│   ├── utils.ts               # Helper utilities
│   └── ...                    # Other libraries
├── data/                       # Data and configuration
│   ├── static/                # Static data files
│   │   ├── challenges.yml     # Challenge definitions
│   │   ├── users.yml          # Default users
│   │   └── i18n/              # Translations
│   └── datacreator.ts         # Database seeding
├── frontend/                   # Angular frontend application
│   ├── src/
│   │   ├── app/               # Angular components
│   │   ├── assets/            # Static assets
│   │   └── environments/      # Environment configs
│   └── package.json           # Frontend dependencies
├── test/                       # Test suites
│   ├── api/                   # API integration tests
│   ├── server/                # Server unit tests
│   └── cypress/               # E2E tests
├── config/                     # Application configurations
│   ├── default.yml            # Default configuration
│   ├── ctf.yml                # CTF mode configuration
│   └── ...                    # Other config files
├── ftp/                        # FTP folder (intentionally exposed)
├── uploads/                    # File upload directory
├── encryptionkeys/            # JWT and other keys
└── views/                      # Server-side templates
```

## Configuration

Juice Shop can be customized through YAML configuration files in the `config/` directory:

- **`default.yml`** - Default configuration
- **`ctf.yml`** - CTF mode with flag codes
- **`fbctf.yml`** - Facebook CTF integration
- **`tutorial.yml`** - Tutorial/training mode
- **`unsafe.yml`** - Disables some security features

### Environment Variables

Key environment variables:

- `NODE_ENV` - Set to `production` or `development`
- `PORT` - Server port (default: 3000)
- `NODE_CONFIG` - Configuration file to use (e.g., `ctf`)

### Customization

You can customize:
- Application name and branding
- Product inventory
- User accounts
- Challenge definitions
- Security questions
- Translations

See the [Customization Guide](https://pwning.owasp-juice.shop/companion-guide/latest/part4/customization.html) for details.

## Testing

### Run All Tests

```bash
npm test                # Run all tests (frontend + backend)
```

### Backend Tests

```bash
npm run test:server     # Server unit tests (Mocha)
npm run test:api        # API integration tests (Frisby/Jest)
```

### Frontend Tests

```bash
cd frontend
npm test                # Unit tests (Jasmine/Karma)
npm run e2e            # E2E tests (Cypress)
```

### E2E Tests

```bash
npm run cypress:open    # Open Cypress UI
npm run cypress:run     # Run Cypress headless
```

### Test Coverage

Test coverage reports are generated in `build/reports/coverage/`:
- Server tests coverage
- API tests coverage
- Frontend tests coverage

## Deployment

### Docker

```bash
# Pull and run official image
docker pull bkimminich/juice-shop
docker run -d -p 3000:3000 bkimminich/juice-shop
```

### Docker Compose

```bash
docker-compose up -d
```

### Cloud Platforms

Juice Shop can be deployed to various cloud platforms:

- **Heroku**: One-click deployment available
- **AWS**: EC2, ECS, Elastic Beanstalk
- **Azure**: App Service, Container Instances
- **Google Cloud**: App Engine, Cloud Run, GKE
- **DigitalOcean**: Droplets, App Platform

Detailed deployment guides available in the [companion guide](https://pwning.owasp-juice.shop/companion-guide/latest/part1/running.html).

### Kubernetes

Example Kubernetes deployment:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: juice-shop
spec:
  replicas: 1
  selector:
    matchLabels:
      app: juice-shop
  template:
    metadata:
      labels:
        app: juice-shop
    spec:
      containers:
      - name: juice-shop
        image: bkimminich/juice-shop
        ports:
        - containerPort: 3000
```

## Contributing

[![GitHub contributors](https://img.shields.io/github/contributors/juice-shop/juice-shop.svg)](https://github.com/juice-shop/juice-shop/graphs/contributors)
[![JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)
[![Crowdin](https://d322cqt584bo4o.cloudfront.net/owasp-juice-shop/localized.svg)](https://crowdin.com/project/owasp-juice-shop)
![GitHub issues by-label](https://img.shields.io/github/issues/juice-shop/juice-shop/help%20wanted.svg)
![GitHub issues by-label](https://img.shields.io/github/issues/juice-shop/juice-shop/good%20first%20issue.svg)

We are always happy to get new contributors on board! Please check
[CONTRIBUTING.md](CONTRIBUTING.md) to learn how to
[contribute to our codebase](CONTRIBUTING.md#code-contributions) or the
[translation into different languages](CONTRIBUTING.md#i18n-contributions)!

## References

Did you write a blog post, magazine article or do a podcast about or mentioning OWASP Juice Shop? Or maybe you held or
joined a conference talk or meetup session, a hacking workshop or public training where this project was mentioned?

Add it to our ever-growing list of [REFERENCES.md](REFERENCES.md) by forking and opening a Pull Request!

## Community & Support

- **Gitter Chat**: [![Gitter](http://img.shields.io/badge/gitter-join%20chat-1dce73.svg)](https://gitter.im/bkimminich/juice-shop)
- **GitHub Discussions**: Ask questions and share ideas
- **Twitter**: [@owasp_juiceshop](https://twitter.com/owasp_juiceshop)
- **Reddit**: [r/owasp_juiceshop](https://reddit.com/r/owasp_juiceshop)
- **Official Website**: <https://owasp-juice.shop>
- **Companion Guide**: <https://pwning.owasp-juice.shop>

## Merchandise

* On [Spreadshirt.com](http://shop.spreadshirt.com/juiceshop) and
  [Spreadshirt.de](http://shop.spreadshirt.de/juiceshop) you can get some swag (Shirts, Hoodies, Mugs) with the official
  OWASP Juice Shop logo
* On
  [StickerYou.com](https://www.stickeryou.com/products/owasp-juice-shop/794)
  you can get variants of the OWASP Juice Shop logo as single stickers to decorate your laptop with. They can also print
  magnets, iron-ons, sticker sheets and temporary tattoos.

## Donations

[![](https://img.shields.io/badge/support-owasp%20juice%20shop-blue)](https://owasp.org/donate/?reponame=www-project-juice-shop&title=OWASP+Juice+Shop)

The OWASP Foundation gratefully accepts donations via Stripe. Projects such as Juice Shop can then request reimbursement
for expenses from the Foundation. If you'd like to express your support of the Juice Shop project, please make sure to
tick the "Publicly list me as a supporter of OWASP Juice Shop" checkbox on the donation form. You can find our more
about donations and how they are used here:

<https://pwning.owasp-juice.shop/companion-guide/latest/part3/donations.html>

## FAQ

<details>
<summary><strong>Is this really an insecure application?</strong></summary>

Yes! OWASP Juice Shop is **intentionally insecure**. It contains numerous security vulnerabilities for educational purposes.
</details>

<details>
<summary><strong>Can I use this for my security training?</strong></summary>

Absolutely! That's exactly what it's designed for. It's perfect for security trainings, workshops, CTFs, and awareness demos.
</details>

<details>
<summary><strong>How do I reset the application?</strong></summary>

Simply delete the `data/juiceshop.sqlite` database file and restart the application. It will recreate itself with default data.
</details>

<details>
<summary><strong>Where can I find solutions to the challenges?</strong></summary>

Solutions are available in the [companion guide](https://pwning.owasp-juice.shop) and in [SOLUTIONS.md](SOLUTIONS.md).
</details>

<details>
<summary><strong>Can I customize Juice Shop for my organization?</strong></summary>

Yes! Check out the [customization guide](https://pwning.owasp-juice.shop/companion-guide/latest/part4/customization.html).
</details>

<details>
<summary><strong>Is Juice Shop suitable for beginners?</strong></summary>

Yes! It includes a built-in hacking instructor tutorial mode that guides beginners through their first challenges.
</details>

## Contributors

The OWASP Juice Shop Project Leaders are:

- [Björn Kimminich](https://github.com/bkimminich) aka `bkimminich` [![Keybase PGP](https://img.shields.io/keybase/pgp/bkimminich)](https://keybase.io/bkimminich)
- [Jannik Hollenbach](https://github.com/J12934) aka `J12934`

For a list of all contributors to the OWASP Juice Shop please visit our
[HALL_OF_FAME.md](HALL_OF_FAME.md).

## Licensing

[![license](https://img.shields.io/github/license/juice-shop/juice-shop.svg)](LICENSE)

This program is free software: you can redistribute it and/or modify it under the terms of the [MIT license](LICENSE).
OWASP Juice Shop and any contributions are Copyright © by Bjoern Kimminich & the OWASP Juice Shop contributors
2014-2026.

![Juice Shop Logo](https://raw.githubusercontent.com/juice-shop/juice-shop/master/frontend/src/assets/public/images/JuiceShop_Logo_400px.png)
