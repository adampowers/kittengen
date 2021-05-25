---
title: kittenGen — Power User Resource Portal

language_tabs:
  - shell
  - yaml: MAML

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

search: true
---


# Introduction

![kittenGen cover image](http://i.imgur.com/RdvXl5u.png)

### Welcome to the kittenGen Power User Resource Portal!

This guide contains everything you need to unlock the full potential of your kittenGen V1 bioPrinter, including the ability to print kittens from the CLI, advanced configuration using our proprietary markup language, MAML, and accessing the full feature set of our GUI application in a headless environment. **Happy printing!**

<aside class="notice">The information in this guide assumes a basic familiarity with terminal commands, as well as comfort editing configuration files using your text editor of choice.</aside>

# Your First Kitten

This quick-start guide will walk you through the basic steps to install the CLI tools, and get you up and running with your first kitten. You should already have your bioPrinter plugged into a USB port. If you haven't unboxed and assembled your bioPrinter yet, please refer to our [kittenGen Quick-Start Hardware Guide](#) [PDF].

<aside class="notice">The CLI tools referenced in this guide only run on UNIX-like systems such as Ubuntu Linux and macOS. Our Windows users are important to us, and we have compatible versions of our software scheduled for release in Q4 2017.</aside>

## Downloading and installing the CLI tools

```shell
wget "http://kitten.io/support/cli-latest.sh"
chmod +x ./cli-latest.sh
./cli-latest.sh
```
Start by downloading the latest installation package from our server using `wget`. This requires an Internet connection. (If you don't have `wget`, `curl -O` works as well.)

Then make the downloaded install file executable, and run it.

<aside class="warning">Don't run as root! The installation package requires write privileges to one of the following locations: /usr/bin, /usr/local/bin. If the installation fails with a permission denied error, resolve the permission error rather than resorting to sudo or su.</aside>

If you accept the defaults as offered, your kittenGen config folder will be located at `~/.kittenrc`.

## Starting a project

```shell
mkdir ~/kittengen | cd ~/kittengen
kitten new --examples
```
To initialize a kitten project, create a folder (we'll be using `~/kittengen` in our examples) and use the `kitten new` command. We'll be appending the `--examples` flag, which produces the pre-written kitten sourcefiles we'll be using for this tutorial.

This will create the following file structure:

Folder | Description
-------|------------
src | kitten sourcefiles
cfg | project-specific configuration files

## Printing a kitten

```shell
kitten make lexi
> ...Printing Lexi.
> ...
> ...
> ...finished printing. Meow~!
```

Using the `--examples` flag in the previous step populated the `/src` folder with some sample kittens. We'll be printing Lexi, one of our most popular kittens, using the command `kitten make`.

`kitten make 'name'` checks for a `src/name.kg` in your project folder.

**You've just printed your first kitten! Once the cooldown window has elapsed, Lexi will be ready to play!**

<aside class="notice">Kittens are living creatures and require food. Please check our <a href="#">Kitten General Store</a> for food, toys, and nutritional syrups specially formulated for your bioprinted kitten.</aside>

# Frequently Asked Questions

## Can I print animals other than kittens?

In short, no. Preparing a species for bioprinting requires exhaustive genomic sequencing, metadata tagging, and ethical certification before being suitable for release to our customers.

Technically, other species are possible, but for our initial release, our development has focused solely on the genome of _Felis catus_, the common house cat.

## How does the kittenGen unit know how to print a kitten?

Each kittenGen bioPrinter comes with a non-user-serviceable firmware containing the _F. catus_ genome, which the machine's Nucleotide Processing Unit (NPU) reads to produce lifeforms within constraints that ensure their long-term viability.

Given the highly complex nature of mammalian bioprinting, a field still in its infancy, this is the central innovation in usability that allows the general public to participate in the miraculous life-creation process formerly reserved for scientists, deities, and mama cats.

## How do I produce kittens that are siblings?

The kittenGen system separates concerns by parameterizing all facets of the bioprinting process. The bioPrinter does not have any capability to create or modify kittens itself, besides reprinting the last kitten sent to its buffer. A litter could technically be created in this fashion, but they would have to be separated to prevent inbreeding, which has distinctly deleterious results compared to inbreeding in litters of unprinted kittens.

Instead, if one desires a litter of kittens, we recommend using build-time config written in MAML, our proprietary markup language. If the system detects a `litter.mml` in your project folder, it will reprint your kitten a number of times specified in the `litter_mean` and `litter_stdev` keys  while allowing for customizable variance in size, color, breed, and personality.

## I've grown tired of my adult cats. Is there a way to reclaim the materials used to create them?

That is called killing your cat, and is strongly recommended against.

kittenGen bioJet™ cartridges are a proprietary blend of synthetic mammalian stem cells, retrovirals, and nanoparticles, and do not involve the harvesting of genetic material from felines, living or dead. There is currently no known way to turn a printed cat "back into" its constituent components.

Instead, if you have tired of your cat, we recommend donating them to one of the approved shelters on our [shelter search page](#). If your cat goes unhoused for too long, these shelters have been trained in the process of sending your former cat to us, for rehousing through our _Paws For A Cause™_ program that donates unwanted cats to hospital wards and nursing homes across the country.

And then, of course, you're welcome to begin anew a relationship with a freshly-sculpted kitten! 🐈
