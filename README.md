# Raen Website

Shopify website on [slate v0](https://shopify.github.io/slate/)

## Requirements

## Install

```
yarn install
```

## Development Workflow

Here is a workflow for our current deployment process with slate:

* Github:
    * All work should be done on feature branches branched off of the dev branch
    * Once completed submit a Pull request on github to the Dev branch.
    * Once the code has been reviewed it will be merged in a deployed to the dev theme on shopify.
* Shopify:
    * Create a duplicate of the dev theme so your work will be isolated.
    * The theme has been converted to slate v0.14.0. No work should be done directly in shopify's theme editor moving forward.

## Shopify Credentials

Copy the `config.yml.default` local and update the `password` fields from [private app in Shopify](https://raenus.myshopify.com/admin/apps/private/68617961533) `Password`.

```
cp config.yml.default config.yml
```

## Development

Sync changes to the dev theme with live preview.

```
slate watch
```

## Deploy

Get the latest theme updates and clean assets directory.

```
yarn run download
```

Deploy current files to production theme.

```
slate deploy -e production
```