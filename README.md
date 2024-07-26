![project is maintained](https://img.shields.io/maintenance/yes/2024.svg)

# ddev-sitediff <!-- omit in toc -->

* [What is ddev-sitediff?](#what-is-ddev-sitediff)
* [Getting started](#getting-started)
* [Usage](#usage)

## What is ddev-sitediff?

SiteDiff is a tool to verify security updates and other upgrades. With its advanced site crawler and an easy-to-use web interface, compare before and after versions of your website in no time.

SiteDiff compares different versions of code, highlighting differences and allowing your team to understand and correct code regressions before releasing.

`evolvingweb/ddev-sitediff` is an add-on integrating Sitediff as and additional service into Ddev.

## Getting started

In a Ddev setup, add `ddev-sitediff` by running 

`ddev get evolvingweb/ddev-sitediff`

## Usage

### Without a recipe 

``` 
ddev sitediff init https://example.com 
ddev sitediff crawl     # crawl and cache example.com
ddev sitediff diff      # diff the previously cached version with the actual version
```

### Using existing `sitediff.yaml` config 

Given a `./prod-stage/sitediff/sitediff.yaml` and a `./selected-paths.txt` both exist.

```
ddev sitediff diff -C prod-stage/sitediff/ --paths-file ./selected-paths.txt 
```

For more details on how to use Sitediff, checkout [this blog post](https://evolvingweb.com/blog/sitediff-compare-multiple-versions-website)
