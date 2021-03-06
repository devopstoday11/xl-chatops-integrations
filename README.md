This repository contains a bot to integrate [XebiaLabs](https://www.xebialabs.com) tools into your ChatOps initiative.

# Introduction

Collaboration and teamwork are two of the cornerstones of how we work at XebiaLabs. Being a distributed team, this means using a chat tool to discuss and keep team members up-to-date. More and more, we have been including our tools in the chat room as well -- JIRA, Zendesk, PagerDuty, and, of course, our own products!

We've written an internal bot to connect XL Deploy to our chat room. This bot, based on the [Lita](http://www.lita.io) framework, allows communication to and from XL Deploy.

The source code is published here for you to try out. Give it a shot and let us know what you think!

# Quick start

In order to get started with the bot, follow these steps:

1. [Install](README.md#installation) the prerequisites for the bot.
2. Install the [XLD bot notifier](xld-bot-notifier) plugin in XL Deploy to notify the bot (and your chat room) of deployment status changes.
3. Check out and configure the [sample bot](sample-bot) to connect to XL Deploy and start playing around locally.
4. Connect the bot to your chat tool of choice, for instance [HipChat](sample-bot/README.md#connecting-to-hipchat) or [Slack](sample-bot/README.md#connecting-to-slack).

# Contents

This repository contains:

* [lita-xl-deploy](lita-xl-deploy): A handler to communicate with [XL Deploy](https://www.xebialabs.com/products/xl-deploy) from your chat room, written for the [Lita](http://www.lita.io) bot framework
* [xld-bot-notifier](xld-bot-notifier): A plugin for [XL Deploy](https://www.xebialabs.com/products/xl-deploy) that pushes status information to the bot
* [sample-bot](sample-bot): A sample bot configuration

# Prerequisites

To run the bot, you need to install [Lita](https://docs.lita.io/getting-started/). Lita requires:

* Ruby, version 2.0 or greater (JRuby 9.0.0.0+ or Rubinius 2+ also work)
* Ruby development libraries and header files
* Redis, version 2.6 or greater
* gcc and make

# Installation

## Installing Ruby 2.0

If your environment does not have Ruby 2.0 installed (for instance, Ubuntu 14), you can install it using the following commands:

```
sudo apt-add-repository ppa:brightbox/ruby-ng
sudo apt-get update
sudo apt-get install ruby2.0 ruby2.0-dev
```

## Installing Redis

```
sudo apt-get install redis-server
```

## Installing gcc and make

```
sudo apt-get install gcc make
```

## Installing Lita

Lita itself is installed as follows:

```
sudo gem install lita
```

# Feedback

If you have any feedback regarding this software or suggestions for improvements, please log them in the [XL Deploy forum](https://support.xebialabs.com/hc/en-us/community/topics/200267485-XL-Deploy).

Regards,
The XebiaLabs team
