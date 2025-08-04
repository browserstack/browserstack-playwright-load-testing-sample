# node-js-playwright-browserstack
This repo contains samples for running [Playwright](https://playwright.dev/docs/intro) tests on BrowserStack using the browserstack-node-sdk.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Setup

* Clone the repo `git clone -b sdk https://github.com/browserstack/node-js-playwright-browserstack.git` and run `cd node-js-playwright-browserstack`. //insert ours here
* Set `BROWSERSTACK_USERNAME` and `BROWSERSTACK_ACCESS_KEY` as environment variables with your [BrowserStack Username and Access Key](https://www.browserstack.com/accounts/settings) 
* Run `npm i` to install the dependencies.
* Update the same in `browserstack-load.yaml` file.

## Running your tests

- To run the sample tests in parallel across the platforms specified in the `browserstack-load.yaml`, run `npx browserstack-cli load run`.

## Notes
* You can view your test results on the [BrowserStack Load-Testing dashboard](https://load.browserstack.com/projects)
