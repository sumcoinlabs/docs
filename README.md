# Sumcoin official documentation repository

----

## How to contribute:

There are two ways to contribute to Sumcoin Docs: Directly via Github website, or by running it locally. Follow the guide that better fits your needs (and knowledge).

#### Directly via Github:

1. Edit any of the [docs files](https://github.com/sumcoin-labs/docs/tree/master/app/assets/docs);
2. Submit a Pull Request with your changes.

#### Developing locally:

Make sure you have Node.js installed. If you don't, [**please follow this guide**](https://gist.github.com/kazzkiq/fe702215173e795d49d0c1ffbea363b5).
NVM is the easiest way. [**please follow this guide**](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-18-04).

#### Environment Tested:  
Ubuntu 18
NVM @ 14
Node 14.21.2
NPM 6.14.17

1. Clone this repo: 
```
git clone https://github.com/sumcoin-labs/docs.git
```
2. Inside the cloned folder, run: 
```
npm i -g brunch && npm i
```
(skip the first command if you already have `brunch` installed);
3. Run: 
```
npm start
```
4. Access http://localhost:3333/ in your browser.

Any changes in the project (both on docs and/or code) will be reflect automatically in the browser once you refresh it.

#### Deploying a public test version:

1. In your local project, run: `npm run deploy`.
2. Access your changes at: https://sumcoin.github.io/docs/

**Note: sumcoin.github.io/docs/ is a test version of the docs, and thus shouldn't be shared openly as the production documentation website.**

####
