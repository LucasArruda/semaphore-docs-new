---
layout: post
title: Setting up continuous delivery with Quay.io
category: Docker
---

[Quay.io](https://quay.io/) is a cloud hosted service for building, storing and
distributing Docker containers. If you don't already have an account on Quay.io,
you can [try it for free](https://quay.io/plans/?trial-plan=free).

Integrating **Quay.io** with **Semaphore** is intuitive and simple, and it
will only take a few clicks.

In order to enable **Docker Registry integrations**, you first need to set up
your project as a Docker project on Semaphore. Read
[Setting up continuous integration for a Docker project on Semaphore](/docs/docker/setting-up-continuous-integration-for-docker-project.html)
for more information.

Configuring the **Quay.io** project integration will enable you to **push** and
**pull** Docker images without having to log into Quay.io during builds
and deployments.

This can be done by visiting your project on Semaphore and clicking "Project
settings" in the upper right corner of your screen.

<img src="/docs/assets/img/docker/shared/click-add-ons.png" class="img-responsive img-bordered" alt="Click Project Add-ons">

Next, click "Docker Registry".

<img src="/docs/assets/img/docker/shared/select-docker-registry.png" class="img-responsive img-bordered" alt="Click Docker Registry">

Choose the "Quay.io" integration.

<img src="/docs/assets/img/docker/setting-up-quay-io-for-your-project/select-quay-io.png" class="img-responsive img-bordered" alt="Click Quay.io integration">

Next, you will be prompted with two input fields:

  - Quay.io `Username`,
  - Quay.io `Password`

<img src="/docs/assets/img/docker/setting-up-quay-io-for-your-project/quay-io-form.png" class="img-responsive img-bordered" alt="Quay.io form">

After you have inputted the credentials, click "Save". Your Quay.io credentials
will be securely encrypted and saved.

You can now push or pull images on Quay.io through Semaphore.

```
docker push quay.io/quay_username/repository_name
```

Happy building!
