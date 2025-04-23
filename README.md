# Sig-Util
### Setup
 
 - Install [Node.js](https://nodejs.org) version 14
 - Install [Node.js](https://nodejs.org) version 18
   - If you are using [nvm](https://github.com/creationix/nvm#installation) (recommended) running `nvm use` will automatically choose the right node version for you.
 - Install [Yarn v3](https://yarnpkg.com/getting-started/install)
 - Run `yarn install` to install dependencies and run any required post-install scripts

 - YARN_VERSION: ${{ steps.yarn-version.outputs.YARN_VERSION }}
     strategy:
       matrix:
         node-version: [14.x, 16.x, 18.x, 19.x]
         node-version: [16.x, 18.x, 20.5]
     steps:
       - uses: actions/checkout@v3
       - name: Use Node.js ${{ matrix.node-version }}
