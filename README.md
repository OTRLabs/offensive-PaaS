# Offensive PaaS | Weaponizing OSS PaaS Systems

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/yourusername/offensivepaas.svg)](https://github.com/yourusername/offensivepaas/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/offensivepaas.svg)](https://github.com/yourusername/offensivepaas/issues)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

> Researching & designing offensive tooling based around OSS [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service) systems ([Supabase](https://supabase.com), [Pocketbase](https://github.com/pocketbase/pocketbase), [[Encore](https://encore.dev/)](https://[encore](https://encore.dev/).dev))

## Table of Contents

1. [Introduction](#introduction)
   - [Background](#background)
   - [Problem Statement](#problem-statement)
   - [Motivation](#motivation)
2. [Plan](#plan)
   - [Objectives](#objectives)
   - [Methodology](#methodology)
   - [Target Platforms](#target-platforms)
3. [Project Structure](#project-structure)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)

## Part 1 | Introduction to `Offensive PaaS`
---

### Background

Before diving into the technical aspects of this project, it's crucial to understand the context and motivation behind "Offensive PaaS". This research initiative is part of a broader effort to develop a [PaaS](https://en.wikipedia.org/wiki/Platform_as_a_service) application tailored for Red Teams, offensive security organizations, and security enthusiasts.

The primary focus of this larger project is [CryptCloud](https://github.com/OTRLabs/CryptCloud-Platform), a Red Teaming PaaS platform developed by [OTR Labs](https://github.com/OTRLabs). For more information about CryptCloud, visit the [OTR Labs website](https://otrlabs.com/) or the [GitHub repository](https://github.com/OTRLabs/CryptCloud-Platform).

### Problem Statement

During the development of [CryptCloud](https://github.com/OTRLabs/CryptCloud-Platform), a realization emerged: there was a lack of hands-on experience with existing PaaS software. This gap in knowledge raised questions about the necessity of designing a new PaaS system from scratch versus leveraging existing solutions.

### Motivation for working on `Offensive PaaS`:

While the appeal of creating a custom PaaS system is strong, it's essential to justify this decision. The primary motivations for developing a new PaaS system include:

1. **Learning Opportunity**: Gaining in-depth knowledge of PaaS architecture and implementation.
2. **Offensive Security Focus**: Tailoring the system specifically for red teaming and offensive security operations, particularly in database and ML features.
3. **Enhanced Privacy**: Implementing stronger privacy controls than typically found in general-purpose PaaS offerings.
4. **Customized Service Integration**: Carefully selecting and integrating third-party services, with a focus on:
   - OAuth providers
   - Alternatives to commonly used services like Redis
5. **Develop & Prototype React Components**: Developing and prototyping React components for CryptCloud. We will be using [palantir/blueprint](https://blueprintjs.com/) as our UI toolkit.


To ensure that developing a custom PaaS system is not redundant, this project aims to:

- Explore existing open-source PaaS platforms
- Identify areas for improvement and innovation
- Develop proof-of-concept features that demonstrate the unique value proposition of CryptCloud

## Part 2 | Planning for `Offensive PaaS`
---

### Objectives

The primary objectives of the `Offensive PaaS` project are:

#### 📚 Gain practical experience with existing open-source PaaS platforms

Explore existing open-source PaaS platforms and gain hands-on experience with their architecture, features, and security models. This will provide valuable insights into the strengths and weaknesses of different platforms and enable you to design CryptCloud with a broader understanding of the market.

#### 📊 Implement prototype versions of features planned for the CryptCloud Platform

Develop prototype implementations of key features planned for CryptCloud using selected open-source PaaS platforms. This will allow you to assess the feasibility and performance of these features in various environments and identify potential improvements.

#### 🔍 Identify limitations and potential security implications of current PaaS offerings

Examine the limitations and potential security implications of current PaaS offerings. This will enable you to identify areas where CryptCloud can differentiate itself and provide a more secure and feature-rich platform for red teaming and offensive security operations.

#### 🔨 Develop a comprehensive list of improvements and innovations for CryptCloud

Create a comprehensive list of improvements and innovations that can be incorporated into CryptCloud. This will serve as a roadmap for future development and ensure that CryptCloud remains a cutting-edge platform tailored to the needs of red teamers and offensive security professionals.

---

If you're ready to embark on this exciting journey, let's dive into the methodology and explore the target platforms!

### Methodology

The project will follow these steps:

1. **Research**: Thoroughly investigate existing open-source PaaS platforms, focusing on their architecture, features, and security models.

2. **Feature Mapping**: Identify key features planned for CryptCloud and map them to equivalent functionalities in existing PaaS systems.

3. **Proof-of-Concept Development**: Create prototype implementations of CryptCloud features using selected open-source PaaS platforms.

4. **Security Analysis**: Assess the security implications of implementing offensive security tools on general-purpose PaaS systems.

5. **Documentation**: Thoroughly document findings, including limitations, potential risks, and areas for improvement.

6. **Iteration**: Use insights gained from this process to refine the CryptCloud Platform design and feature set.



### Target Platforms

The project aims to explore three open-source platform-as-a-service (PaaS) systems:


**1. Supabase**
[Supabase](https://supabase.com) is an open-source alternative to Firebase. It provides a set of backend services, including authentication, database, and storage. With Supabase, red teamers can take advantage of its feature-rich authentication system, real-time database, and storage capabilities.

**2. Pocketbase**

[Pocketbase](https://github.com/pocketbase/pocketbase) is a backend-as-a-service platform that allows developers to build their own custom backend for their SaaS and mobile applications. It provides features like authentication, database, storage, and email integration. By integrating Pocketbase with CryptCloud, users can leverage its powerful backend capabilities to enhance their offensive security operations.

### Pocketbase C2

The idea behind Pocketbase C2 is to establish HTTP(S) based communications with custom agents using Pocketbase's pseudo REST API system. Here are various methods for tunneling/exposure:

- [Tor hidden service](https://www.torproject.org/docs/hidden-services.html.en)
- [Tor + Tor2Web Proxy](https://www.torproject.org/projects/tor2web.html.en)
- [Cloudflared](https://www.cloudflare.com/products/cloudflared/)
- [Nginx](https://www.nginx.com/)
- [Apache](https://httpd.apache.org/)
- [Traefik](https://traefik.io/)

Pocketbase C2 could of course be containerized using platforms like [Pockethub](https://github.com/pocketbase/pockethub).



**3. [Encore](https://encore.dev/)**
[Encore](https://encore.dev/) is a backend development engine that aims to provide a modern and efficient way to build backend services. It offers features like database, authentication, and storage, making it an attractive choice for red teamers. By integrating [Encore](https://encore.dev/) with CryptCloud, users can seamlessly integrate its powerful backend capabilities into their offensive security operations.


**4. [SurrealDB](https://surrealdb.com/)**
[SurrealDB](https://surrealdb.com) calls itself "The **ultimate** `multi-model` `database`". 
It is an open-source alternative to traditional Graph & NoSQL databases. It provides an advanced and powerful backend for storing and querying data.
While it is not quite the same as something like Supabase & Pocketbase, it is a great choice for offensive security operations revolving around AI, ML, and large databases!

**5. [Nocodb](https://nocodb.com/)**

---

Build Databases As Spreadsheets :

📚 No-Coding Required

NocoDB allows building **no-code** database solutions with **ease of spreadsheets**.

📈 Bring your own database or choose ours!

🔥 Millions of rows? Not a problem.

🔑 Your Data. Your rules. You are in control.

---
