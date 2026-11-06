# node-js-playwright-browserstack
This repo contains samples for running [Playwright](https://playwright.dev/docs/intro) tests on BrowserStack using the browserstack-node-sdk.

![BrowserStack Logo](https://d98b8t1nnulk5.cloudfront.net/production/images/layout/logo-header.png?1469004780)

## Setup

* Clone the repo `git clone https://github.com/browserstack/browserstack-playwright-load-testing-sample.git`.
* Set your credentials as environment variables, as described in [Set your credentials](#set-your-credentials).
* Run `npm i` to install the dependencies.
* Open `browserstack-load.yml` and update it with your load test configuration.

## Set your credentials

The BrowserStack CLI reads your credentials from environment variables. Copy your username and access key from [Account Settings](https://www.browserstack.com/accounts/settings) and export them in the shell you run the test from:

On macOS or Linux (bash or zsh), run the lines below. The second one prompts for the key without echoing it, so the key stays out of your shell history:

```sh
export BROWSERSTACK_USERNAME="<your-username>"
printf 'BrowserStack access key: '; read -rs BROWSERSTACK_ACCESS_KEY; echo; export BROWSERSTACK_ACCESS_KEY
```

On Windows, run these in PowerShell. The second line prompts for the key in the same way:

```powershell
$env:BROWSERSTACK_USERNAME = "<your-username>"
$env:BROWSERSTACK_ACCESS_KEY = [System.Net.NetworkCredential]::new('', (Read-Host -AsSecureString 'BrowserStack access key')).Password
```

These variables last only for the current terminal session. If the CLI reports an authentication error, check that both are set in the terminal you run it from.

**Never commit your credentials.** Leave the `userName` and `accessKey` placeholders in `browserstack-load.yml` as they are (the environment variables override them), and keep your access key out of every file you push. If a key is ever exposed, regenerate it from Account Settings.

## Running your tests

- To run the sample tests in parallel across the platforms specified in the `browserstack-load.yml`, run `npx browserstack-cli load run`.

## Notes
* You can view your test results on the [BrowserStack Load-Testing dashboard](https://load.browserstack.com/projects)
