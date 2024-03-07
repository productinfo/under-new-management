![Under New Management](src/logo128.png)

# Under New Management

**Detect when your extensions have changed owners**

Intermittenty checks your installed extensions to see if the developer information listed on the Chrome Web Store has changed. If anything is different, the extension icon will display a red badge, alerting you to the change.

Created by [Matt Frisbie](https://www.mattfriz.com/)

Media:

- [Hacker News discussion](https://news.ycombinator.com/item?id=39620060)
- [Featured in *tl;dr sec Newsletter*](https://tldrsec.com/p/tldr-sec-221)
- [Featured in *The Register*](https://www.theregister.com/2024/03/07/chrome_extension_changes/)

![image](unm-screenshot-1280x800.png)

## Why is this needed?

Extension developers are [constantly getting offers to buy their extensions](https://github.com/extesy/hoverzoom/discussions/670). In nearly every case, the people buying these extensions want to rip off the existing users.

**The users of these extensions have no idea an installed extension has changed hands, and may now be compromised.**

Under New Management gives users notice of the change of ownership, giving them a chance to make an informed decision about the software they're using.

## Installation

Install here: [https://chromewebstore.google.com/detail/under-new-management/jppepdecgemgbgnjnnfjcmanlleioikj](https://chromewebstore.google.com/detail/under-new-management/jppepdecgemgbgnjnnfjcmanlleioikj?hl=en&authuser=0)

OR

Download a [prebuilt release](https://github.com/classvsoftware/under-new-management/releases), unpack the .zip file, and load the `dist` directory into Chrome.

## Building from source

**Under New Management** uses Parcel, React, Typescript, and TailwindCSS

`yarn install` to install dependencies

`yarn start` to run locally

`yarn build` to build a release

## Why does this need an external server?

Browsers have special rules about modifying extension marketplace domains. For example, you cannot set `declarative_net_request` rules for `chromewebstore.google.com`. Therefore, this extension delegates the developer info checking to the [ExBoost](https://extensionboost.com) API server.
