<p align="center">
  <a href="https://fingerprint.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/fingerprintjs/botd/main/resources/fp_logo_white.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/fingerprintjs/botd/main/resources/fp_logo_blue.svg">
      <img alt="Fingerprint" width="312px" src="https://raw.githubusercontent.com/fingerprintjs/botd/main/resources/fp_logo_orange_blue.svg">
    </picture>
  </a>
</p>
<p align="center">
  <a href="https://www.npmjs.com/package/@fpjs-incubator/botd-agent">
    <img src="https://img.shields.io/npm/v/@fpjs-incubator/botd-agent.svg" alt="Current NPM version">
  </a>
  <a href="https://www.npmjs.com/package/@fpjs-incubator/botd-agent">
    <img src="https://img.shields.io/npm/dm/@fpjs-incubator/botd-agent.svg" alt="Monthly downloads from NPM">
  </a>
  <a href="https://www.jsdelivr.com/package/npm/@fpjs-incubator/botd-agent">
    <img src="https://img.shields.io/jsdelivr/npm/hm/@fpjs-incubator/botd-agent.svg" alt="Monthly downloads from jsDelivr">
  </a>
</p>
<p align="center">
  <a href="https://discord.gg/P6Ya76HkbF">
    <img src="https://img.shields.io/discord/852099967190433792?style=for-the-badge&label=Discord&logo=Discord&logoColor=white" alt="Discord server">
  </a>
</p>

## BotD

```diff
# Before

- 40% of your website traffic is from bots
- They're taking over accounts, scraping prices and ruining your website reputation

# After

+ BotD is a browser library for JavaScript bot detection
+ Easily add ability to detect automation tools
+ Requires adding only a few lines of JavaScript on your website
```

[⚡ View Our Demo](https://fingerprintjs.github.io/BotD).

## Quick start

### CDN

```html
<script>
    // Initialize the agent at application startup.
    const botdPromise = import('https://openfpcdn.io/botd/v1').then((Botd) => Botd.load())

    botdPromise
        .then((botd) => botd.detect())
        .then((result) => console.log(result))
        .catch((error) => console.error(error))
</script>
```

### NPM

```bash
npm i @fpjs-incubator/botd-agent
# or
yarn add @fpjs-incubator/botd-agent
```

```js
import { load } from '@fpjs-incubator/botd-agent'

// Initialize an agent at application startup.
load()
    .then((botd) => botd.detect())
    .then((result) => console.log(result))
    .catch((error) => console.error(error))
```

[Run this code](https://stackblitz.com/edit/botd-cdn?devtoolsheight=100&file=index.html)

📕 [Full documentation](docs/api.md)

## 🤖 Use the free Pro version to get sophisticated bot detection

[Fingerprint Pro](https://fingerprint.com/products/bot-detection/) is a professional bot detection service that processes all information server-side and transmits it securely to your servers using server-to-server APIs.
Pro combines vast amounts of auxiliary data that bots leak (cursor movements, network overrides, browser changes and more) to be able to reliably deduplicate real users from automated software, resulting in the detection of popular automation tools, their derivatives and plugins.

**Pro plans start at $0/month - no credit card required.**

<br />

<p align="center">
  <a href="https://fingerprint.com/products/bot-detection/">
    <img src="resources/pro_botd_screenshot.png" alt="Pro BotD screenshot" width="512px" />
  </a>
</p>

<br />
<br />

Full product comparison:

<table>
  <thead>
    <tr>
      <th></th>
      <th align="center">Open Source</th>
      <th align="center">Pro</th>
    </tr>
  </thead>
  <tbody>
    <tr><td colspan="3"><h4>Core Features</h4></td></tr>
    <tr><td>100% open source</td><td align="center">yes</td><td align="center">no<sup>1</sup></td></tr>
    <!-- <tr><td>Accuracy</td><td align="center">up to 60%</td><td align="center"><b>99.5%</b></td></tr> -->
    <tr><td><b>Search engine detection</b><br/><i>works in all modern browsers - see our full list of <a href="https://dev.fingerprint.com/docs/browser-support/" target="_blank">browsers supported</a></i></td><td align="center">–</td><td align="center">✓</td></tr>
    <tr><td>Automation web services detection</td><td align="center">–</td><td align="center">✓</td></tr>
    <tr><td>Automation browser extensions detection</td><td align="center">–</td><td align="center">✓</td></tr>
    <tr><td colspan="3"><h4>Detectable automation tools & frameworks</h4></td></tr>
    <tr><td>Headless Browsers (<a href="https://www.google.com/chrome">Chrome</a>, <a href="https://www.mozilla.org/en-US/firefox/new/">Firefox</a>)</td><td align="center">✓</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/SeleniumHQ/selenium">seleniumHQ/selenium</a></b><br/><i>umbrella project encapsulating a variety of tools and libraries enabling web browser automation</i></td><td align="center">✓</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/microsoft/playwright">microsoft/playwright</a></b><br/><i>Node.js library to automate Chromium, Firefox and WebKit with a single API</i></td><td align="center">✓</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/ariya/phantomjs">ariya/phantomjs</a></b><br/><i>headless WebKit scriptable with JavaScript</i></td><td align="center">✓</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/segmentio/nightmare">segmentio/nightmare</a></b><br/><i>high-level browser automation library</i></td><td align="center">✓</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/electron/electron">electron/electron</a></b><br/><i>framework lets you write cross-platform desktop applications using JavaScript, HTML and CSS</i></td><td align="center">✓</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/laurentj/slimerjs">laurentj/slimerjs</a></b><br/><i>scriptable browser</i></td><td align="center">✓</td><td align="center">✓</td></tr>
    <!-- -->
    <tr><td colspan="3"><h4>Detectable stealth plugins</h4></td></tr>
    <tr><td><b><a href="https://github.com/berstend/puppeteer-extra/tree/master/packages/puppeteer-extra-plugin-stealth">berstend/puppeteer-extra/packages/puppeteer-extra-plugin-stealth</a></b><br/><i>plugin for puppeteer-extra to prevent detection.</i></td><td align="center">-</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/microlinkhq/browserless">microlinkhq/browserless</a></b><br/><i>efficient driver for controlling headless browsers built on top of <a href="https://github.com/puppeteer/puppeteer">puppeteer</a> developed for scenarios where performance matters</i></td><td align="center">-</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/ultrafunkamsterdam/undetected-chromedriver">ultrafunkamsterdam/undetected-chromedriver</a></b><br/><i>optimized Selenium Chromedriver patch which does not trigger anti-bot services</i></td><td align="center">-</td><td align="center">✓</td></tr>
    <tr><td><b><a href="https://github.com/MeiK2333/pyppeteer_stealth">MeiK2333/pyppeteer_stealth</a></b><br/><i>stealth plugin for <a href="https://github.com/miyakogi/pyppeteer">pyppeteer</a></i></td><td align="center">-</td><td align="center">✓</td></tr>
    <!-- <tr><td><a href="______">______</a><br/><i>____________</i></td><td align="center">✓</td><td align="center">✓</td></tr> -->
    <!-- -->
    <tr><td colspan="3"><h4>Additional Features</h4></td></tr>
    <tr><td><b>Server-side accuracy increase</b><br/><i>based on additional server-side signals, such as TLS crypto support, ipv4/v6 data and others</i></td><td align="center">–</td><td align="center">✓</td></tr>
    <tr><td><b>Query API & realtime Webhooks</b><br/><i>build flexible workflows</i></td><td align="center">–</td><td align="center">✓</td></tr>
    <!-- -->
    <tr><td colspan="3"><h4>Operations</h4></td></tr>
    <tr><td><b>Data security</b></td><td align="center">Your infrastructure</td><td align="center">Encrypted at rest</td></tr>
    <tr><td><b>Storage</b></td><td align="center">Your infrastructure</td><td align="center">Unlimited up to 1 yr</td></tr>
    <tr><td><b>Regions</b></td><td align="center">Your infrastructure</td><td align="center">Hosting in US, EU and Mumbai</td></tr>
    <tr><td><b>Compliance</b></td><td align="center">Your infrastructure</td><td align="center">GDPR, CCPA compliant<sup>2</sup></td></tr>
    <tr><td><b>SLA</b></td><td align="center">No SLA</td><td align="center">99.9% Uptime</td></tr>
    <tr><td><b>Support</b></td><td align="center">GitHub community</td><td align="center">Support team via email, chat, and call-back within 1 business day</td></tr>
   
  </tbody>
</table>

<sub>1. Pro uses the open source BotD library as well as proprietary technology for increased accuracy and identifier stability.</sub>

<sub>2. Fingerprint Pro is GDPR and CCPA compliant as the data processor. You still need to be compliant as the data controller and use the identification for fraud prevention under legitimate interest or ask for user consent.</sub>

Pro result example:

```js
{
    "bot": {
        "result": "bad"
        "type": "webdriver"
    }
}
```

🍿 [Live demo](https://fingerprint.com/products/bot-detection/)

⏱ [How to upgrade from Open Source to Pro in 30 seconds](https://dev.fingerprint.com/v3/docs/migrating-from-open-source-v3)

📕 [Fingerprint Pro documentation](https://dev.fingerprint.com)

<!--
▶️ [Video: use Fingerprint Pro to prevent multiple signups](https://www.youtube.com/watch?v=jWX9P5_jZn8) -->

<!-- 🤖 [Sample usage with React on the StackBlitz platform](https://stackblitz.com/edit/fingerprintjs-react-demo) -->

## Migrating from v0

-   [Migration guide](docs/migrating_v0_v1.md)
-   [V0 documentation](https://github.com/fingerprintjs/BotD/tree/v0)

## Supported browsers

The library supports all popular browsers.
See more details and learn how to run the library in old browsers in the [browser support guide](docs/browser_support.md).

## Where to get support

Thanks to our [series B funding](https://fingerprint.com/blog/series-b/), we are happy to provide technical support for our open-source FingerprintJS library. We recommend using GitHub [Issues](https://github.com/fingerprintjs/fingerprintjs/issues) to submit bugs or [Discussions](https://github.com/fingerprintjs/fingerprintjs/discussions) to ask questions.
Using issues and discussions publicly will help the open-source community and other users with similar issues.
However, if you require private support, please email us at [oss-support@fingerprint.com](mailto:oss-support@fingerprint.com).

## Contributing

See the [contributing guidelines](contributing.md) to learn how to start a playground, test and build.

## Other products by Fingerprint

-   [FingerprintJS -- browser fingerprinting library that queries browser attributes and computes a hashed visitor identifier from them](https://github.com/fingerprintjs/fingerprintjs)
-   [AEV -- Android App Environment Verification API](https://github.com/fingerprintjs/aev)

### License

[MIT](LICENSE)

<p align="center">
© 2022 FingerprintJS, Inc
</p>
