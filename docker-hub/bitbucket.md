---
description: Docker Hub Automated Builds using Bitbucket
keywords:
- Docker, docker, registry, accounts, plans, Dockerfile, Docker Hub, docs, documentation,
  trusted, builds, trusted builds,  automated builds, bitbucket
menu:
  main:
    parent: mn_pubhub
    weight: 8
title: Automated Builds with Bitbucket
---

# Automated Builds with Bitbucket

If you've previously linked Docker Hub to your Bitbucket account,
you'll be able to skip to [Creating an Automated Build](bitbucket.md#creating-an-automated-build).

## Linking to your Bitbucket account

In order to set up an Automated Build of a repository on Bitbucket, you need to
link your [Docker Hub](https://hub.docker.com/account/authorized-services/)
account to a Bitbucket account. This will allow the registry to see your Bitbucket
repositories.

To add, remove or view your linked account, go to the "Linked Accounts & Services"
section of your Hub profile "Settings".

![authorized-services](images/authorized-services.png)

Then follow the onscreen instructions to authorize and link your
Bitbucket account to Docker Hub. Once it is linked, you'll be able
to create a Docker Hub repository from which to create the Automatic Build.

## Creating an Automated Build

You can [create an Automated Build](
https://hub.docker.com/add/automated-build/bitbucket/orgs/) from any of your
public or private Bitbucket repositories with a `Dockerfile`.

To get started, log in to Docker Hub and click the
"Create &#x25BC;" menu item at the top right of the screen. Then select
[Create Automated Build](https://hub.docker.com/add/automated-build).

Select the the linked Bitbucket account, and then choose a repository to set up
an Automated Build for.

## The Bitbucket webhook

When you create an Automated Build in Docker Hub, a webhook is added to your Bitbucket repository automatically.

You can also manually add a webhook from your repository's **Settings** page. Set the URL to `https://registry.hub.docker.com/hooks/bitbucket`, to be triggered for repository pushes.

![bitbucket-hooks](images/bitbucket-hook.png)
