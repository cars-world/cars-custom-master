<!--
@license
Copyright (c) rljson

Use of this source code is governed by terms that can be
found in the LICENSE file in the root of this package.
-->

# Build the image into crcars

## Motivation

- cars-custom-master is the master of the custom side, where released
  catalogs are edited further for customers; so far it answers a
  greeting
- The registry and the stages had new names: one registry `crcars` for
  all stages instead of one per stage, and the stages `dev`, `test` and
  `prod`

## Strategy

- Change the README only; the code stays as it is

## Image and stages

- The README builds the image with
  `az acr build --registry crcars --image cars-custom-master:<version> .`
- It names the stages `dev`, `test` and `prod` and says the master runs
  as a container in each, also behind a proxy that serves it under a
  path and strips that prefix

## Result

- `cars-custom-master:0.0.1` lies in `crcars` and answers
  `Hello from cars-custom-master`

## Open Points

- The master holds no data yet
