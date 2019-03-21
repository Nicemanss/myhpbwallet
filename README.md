### [https://myhpbwallet.com](https://myhpbwallet.com)

### [Download the Latest Release](https://github.com/Nicemanss/hpbwallet)

-  HPB Donation Address: 0x6b668c559600186477baf091fc572ffdcca7d8ea

- The wallet uses a light node running on AWS.

### MyHPBWallet

- MyHPBWallet is a free, open-source, client-side tool for easily & securely interacting with the HPB network.

- My HPB Wallet is a clone from MyEtherWallet which has been rewritten to work with the HPB Network. MyEtherWallet was created and is maintained by [kvhnuke](https://github.com/kvhnuke) and [tayvano](https://github.com/tayvano).


#### Features

- Create new wallets completely client side.
- Access your wallet via unencrypted private key, encrypted private key, keystore files, mnemonics, and soon Ledger Nano S or TREZOR hardware wallet.
- Easily send HPB to others.
- Generate, sign & send transactions offline, ensuring your private keys never touch an internet-connected device.


### Our Philosophy

 - **Empower the people**: Give people the ability to interact with the HPB blockchain easily, without having to run a full node.
 - **Make it easy & free**: Everyone should be able to create a wallet and send HPB without additional cost.
 - **People are the Priority**: People are the most important & their experience trumps all else. If monetization worsens the experience, we don't do it. (e.g. ads)
 - **A learning experience, too**: We want to educate about HPB, security, privacy, the importance of controlling your own keys, how the blockchain works, and how HPB and blockchain technologies enable a better world.
 - **If it can be hacked, it will be hacked**: Never save, store, or transmit secret info, like passwords or keys.
 - **Offline / Client-Side**: User should be able to run locally and offline without issue.
 - **Private**: No tracking!!! No emails. No ads. No demographics. We don't even know how many wallets have been generated, let alone who / what / where you are.
 - **Open source & audit-able**


### Users (non-developers)

- [It is recommended you start here.](https://kb.myhpbwallet.com/getting-started/getting-started-new.html)
- You can run MyHPBWallet.com on your computer. You can create a wallet completely offline & send transactions from the "Offline Transaction" page.

1. Go to https://github.com/Nicemanss/hpbwallet .
2. Click on "Clone or download".
3. Click on Download Zip.
4. Unzip it and double-click index.html.
5. MyHPBWallet.com is now running entirely on your computer.

In case you are not familiar, you need to keep the entire folder in order to run the website, not just index.html. Don't touch or move anything around in the folder. If you are storing a backup of the MyHPBWallet repo for the future, we recommend just storing the ZIP so you can be sure the folder contents stay intact.

As we are constantly updating MyHPBWallet.com, we recommend you periodically update your saved version of the repo.


### Developers

If you want to help contribute, here's what you need to know to get it up and running and compiling.

- Both the Chrome Extension and the MyHPBWallet.com are compiling from the same codebase. This code is found in the `app` folder. Don't touch the `dist` or `chrome-extension` folders.
- We use angular and bootstrap. We used to use jQuery and Bootstrap until it was converted in April 2016. If you wonder why some things are set up funky, that's why.
- The mercury branch is currently the active development branch. We then push the dist folder live to gh-pages, which then gets served to MyHPBWallet.com.
- We use npm / gulp for compiling. There is a lot of stuff happening in the compilation.

**Getting Started**

- Start by running `npm install`.
- Run `npm run dev`. Gulp will then watch & compile everything and then watch for changes to the HTML, JS, or CSS.
- For distribution, run `npm run dist`.

**Folder Structure**
- `fonts` and `images` get moved into their respective folders. This isn't watched via gulp so if you add an image or font, you need to run `gulp` again.
- `includes` are the pieces of the pages / the pages themselves. These are pretty self-explanatory and where you will make most frontend changes.
- `layouts` are the pages themselves. These basically take all the pieces of the pages and compile into one massive page. The navigation is also found here...sort of.
    * `index.html` is for MyHPBWallet.com.
    * `cx-wallet.html` is the main page for the Chrome Extension.
    * `embedded.html` is for https://myhpbwallet.com/embedded.html.

- `embedded.html` is for embedding the wallet generation into third-party sites. [Read more about it and how to listen for the address generated here.](https://www.reddit.com/r/ethereum/comments/4gn37o/embeddable_myetherwallet_super_simple_wallet/)
- The wallet decrypt directives are at `scripts/directives/walletDecryptDrtv.js`. These show up on a lot of pages.
- The navigation is in `scripts/services/globalServices.js`. Again, we control which navigation items show up in which version of the site in this single file.
- As of September 2016, almost all the copy in the .tpl files are only there as placeholders. It all gets replaced via angular-translate. If you want to change some copy you need to do so in `scripts/translations/en.js` folder. You should also make a note about what you changed and move it to the top of the file so that we can make sure it gets translated if necessary.
- `styles` is all the less. It's a couple custom folders and bootstrap. This badly needs to be redone. Ugh.


### Use Your Own Servers / Node Guide

- [Setting up on AWS super easily.](https://github.com/hpb-project/hpb-release/tree/master/docker)


#### MyHPBWallet.com & MyHPBWallet CX are licensed under The MIT License (MIT).
