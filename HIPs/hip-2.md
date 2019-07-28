---
eip: 2
title: Configuration files
status: Released
created: 2019-07-24
---

## Simple Summary
JSON files define a GAN

## Abstract
There are many ways to configure GANs and a lot of hyperparameters to keep track of.  JSON is a file format that is human readable and can be used to organize these parameters.

Each GAN Component (generator, discriminator, etc) each receives it's own configuration object.

## Motivation

Reproducability and parallel training

## Specification
```json
{
  "component1": {
    "option1": 1.0
  }
}
```

## Implementation

`hypergan new -l .` - list all configs

`hypergan new -c config` - create a new config

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

