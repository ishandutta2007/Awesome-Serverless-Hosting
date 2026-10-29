# Awesome-Serverless-Hosting

## Top Serverless Hosting Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on PaaS Deployment, Git-Push Workflows & Self-Hosted Alternatives to Vercel/Netlify*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Serverless Hosting**. These tools enable developers to deploy applications, static sites, and serverless functions without managing infrastructure—abstracting away servers while providing Git-integrated workflows, automatic HTTPS, and managed databases.



**Examples** include Oxygen, Vercel, Netlify, Cloudflare Pages, AWS Amplify, Render, Railway, Fly.io, Heroku, and Firebase App Hosting (the category leaders).



**Open-source emphasis**: Serverless Hosting is a domain where open-source tooling is **mature and production-proven at the PaaS layer**. **Coolify** is the most feature-complete self-hosted alternative to Vercel/Netlify/Heroku, with a modern dashboard, Git integration, managed databases, and multi-server support . **Dokku** provides the closest `git push` parity to classic Heroku with a minimal footprint . **CapRover** offers Docker Swarm-based multi-server deployment . For a true serverless functions experience, **Juno** provides self-hosted static hosting, authentication, datastore, and serverless functions in WASM containers , while **Fission** brings serverless functions to Kubernetes with ~100ms cold starts . No open-source project matches the global edge network and zero-config DX of Vercel, but Coolify and Juno provide compelling self-hosted alternatives for different use cases.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Oxygen (Shopify)](https://shopify.dev/docs/api/hydrogen/latest/oxygen)**  

  Shopify's hosting platform for Hydrogen storefronts; provides global CDN, server-side rendering, and integration with Shopify's commerce APIs.



- **[Vercel](https://vercel.com/)**  

  Frontend cloud platform with zero-config deployments, edge functions, preview deployments per Git branch, and global CDN; the creator of Next.js.



- **[Netlify](https://www.netlify.com/)**  

  Web development platform with Git-based deployments, serverless functions, form handling, and edge network; a pioneer of the JAMstack hosting model.



- **[Cloudflare Pages](https://pages.cloudflare.com/)**  

  Static site hosting with Git integration, edge functions (Workers), and global CDN; part of Cloudflare's developer platform.



- **[AWS Amplify](https://aws.amazon.com/amplify/)**  

  Full-stack development platform with hosting, CI/CD, and backend services (auth, data, storage) integrated with AWS.



- **[Render](https://render.com/)**  

  Unified cloud platform for deploying apps, static sites, databases, and cron jobs with automatic SSL and Git-based workflows.



- **[Railway](https://railway.app/)**  

  Infrastructure platform for deploying apps and databases with a focus on developer experience and instant deployments.



- **[Fly.io](https://fly.io/)**  

  Platform for running apps close to users with global edge deployment, Firecracker microVMs, and persistent volumes.



- **[Heroku](https://www.heroku.com/)**  

  The original PaaS with `git push` deployments, add-ons marketplace, and managed services; widely used for rapid prototyping and production apps.



- **[Firebase App Hosting](https://firebase.google.com/)**  

  Google's hosting solution for web apps with Git integration, server-side rendering support, and integration with Firebase services.



## Open-Source GitHub Projects



### Self-Hosted PaaS (Vercel/Heroku Alternatives)



- **[Coolify](https://github.com/coollabsio/coolify)**  

  The most feature-complete open-source self-hosted PaaS (Apache 2.0); an alternative to Vercel, Heroku, and Netlify that lets you deploy static sites, databases, full-stack applications, and 280+ one-click services on your own servers . Features a modern web dashboard, Git integration (GitHub, GitLab, Gitea, Bitbucket), automatic HTTPS via Let's Encrypt, managed databases (PostgreSQL, MySQL, MariaDB, MongoDB, Redis, ClickHouse), Docker Compose support, and multi-server management . **The recommended default for new self-hosted PaaS deployments** . Requires 2GB RAM minimum (4GB recommended) .



- **[Dokku](https://github.com/dokku/dokku)**  

  The closest open-source equivalent to classic Heroku (MIT); `git push` deployments using Heroku buildpacks or Dockerfiles, with a plugin ecosystem for databases, SSL, and other services . **Minimal footprint** (~1GB RAM) with no long-running control service—just scripts on the host . Best for solo developers or small teams wanting the simplest possible deployment workflow on a single server .



- **[CapRover](https://github.com/caprover/caprover)**  

  Docker Swarm-based PaaS with a web dashboard, one-click app templates, and multi-server support via worker nodes . **Battle-tested and stable** for long-running multi-server setups without Kubernetes . SSL via Let's Encrypt, Git-based deployment, and CLI/API access.



- **[Dokploy](https://github.com/dokploy/dokploy)**  

  Open-source alternative to Vercel, Netlify, and Heroku (Apache 2.0); features Docker Compose support, multi-node deployment, Traefik integration, and a modern dashboard . Positioned as a Docker Compose-first PaaS for teams already using Compose workflows .



### Self-Hosted Serverless (Functions & Static Hosting)



- **[Juno](https://github.com/junobuild/juno)**  

  Open-source serverless platform for hosting static websites, building web apps, and running serverless functions with self-hosting (BSD-3-Clause); described as **"Vercel + Firebase + Self-Hosting"** . Features authentication, datastore, file storage, hosting, serverless functions (Rust & TypeScript in WASM containers), analytics, and local-first development with a full emulator. Each project runs in its own WASM container fully controlled by you. **The most complete open-source Firebase/Vercel hybrid** for developers wanting managed-like DX with true ownership .



- **[Fission](https://github.com/fission/fission)**  

  Kubernetes-native serverless framework (Apache 2.0) for deploying functions triggered by HTTP, message queues, or schedules . Features **~100ms cold starts** via a pool of warm containers, support for NodeJS, Python, Ruby, Go, PHP, Bash, and any Linux executable. **The standard for serverless functions on Kubernetes**—requires an existing K8s cluster but provides production-grade function orchestration .



- **[Self-Hosted Serverless (mstgnz)](https://github.com/mstgnz/self-hosted-serverless)**  

  Lightweight, production-ready self-hostable alternative to AWS Lambda and Google Cloud Functions (Go) . Functions run as Go plugins or WASM modules with HTTP and gRPC support, API key authentication, rate limiting, function timeouts, panic recovery, and built-in metrics. Includes PostgreSQL, SQLite, and Redis integration, plus an event bus. **For teams wanting a simple, self-contained FaaS** without Kubernetes overhead .



### Additional Strong Open-Source Options



- **Taubyte** — Open-source Git-native PaaS for building, deploying, and scaling applications (BSD-3-Clause); infrastructure defined in Git with capabilities similar to Vercel, Firebase, and Cloudflare, plus built-in AI features .

- **Miabi** — Modern self-hosted PaaS (Go) with Docker-based deployment, GitOps, pipelines, marketplace templates, multi-cluster support, SSO, and privacy-first analytics . **More enterprise-focused** than Coolify, with SAML/SCIM in the Enterprise tier.

- **Levelrail** — Apache 2.0 self-hosted PaaS with health gates, blue-green cutover, rollback, and MCP support for AI agents . **Early-stage but architecturally ambitious**.



**Frameworks for building custom systems**: Choose based on deployment style. For **Vercel/Heroku-like PaaS with a dashboard**: Coolify is the most complete . For **git push simplicity on a single server**: Dokku . For **Docker Swarm multi-server**: CapRover . For **Firebase/Vercel hybrid with serverless functions**: Juno . For **Kubernetes-native functions**: Fission . No open-source project replicates Vercel's global edge network, but Coolify and Juno cover the most common self-hosted use cases.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Serverless hosting platforms handling application code and data must comply with applicable security policies and data governance requirements; self-hosted deployments require proper server hardening, backup planning, and TLS certificate management.

- **Open-source serverless hosting is mature at the PaaS layer**—Coolify and Dokku are production-proven Heroku alternatives . For true serverless functions (FaaS), Juno and Fission provide self-hosted options but require more operational knowledge than Vercel's zero-config experience . No open-source project matches the global edge network and instant preview deployments of Vercel or Netlify.

- Verify license terms for commercial use; Coolify uses Apache 2.0 , Dokku uses MIT , Juno uses BSD-3-Clause , and Fission uses Apache 2.0 .



---



**Made for developers, platform engineers, DevOps teams, and self-hosting enthusiasts.**  

Let's make serverless hosting more open, but with clear eyes about which layer each tool addresses.
