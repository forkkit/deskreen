[![codecov](https://codecov.io/gh/pavlobu/test-electron-boilerplate-ci/branch/master/graph/badge.svg)](https://codecov.io/gh/pavlobu/deskreen)
![build and test](https://github.com/pavlobu/deskreen/workflows/build%20and%20test/badge.svg?event=pull_request)
![release all os -- no code signing](https://github.com/pavlobu/deskreen/workflows/release%20all%20os%20--%20no%20code%20signing/badge.svg)
![codecov generate](https://github.com/pavlobu/deskreen/workflows/codecov%20generate/badge.svg)

# Deskreen

### Website: https://www.deskreen.com

## Deskreen turns any device with a web browser to a second screen for your computer

Deskreen is an `electron.js` based application that uses `WebRTC` to make a live stream of your
desktop to a web browser on any device.
It is built on top of [Electron React Boilerplate](https://github.com/electron-react-boilerplate)
For better security mechanism, end-to-end encrytpion is implemented, which is inspired by
[darkwire.io](https://github.com/darkwire/darkwire.io) , the difference is, that it is rewritten
in `Typescript` and trnasformed to use `node-forge` instead of `window.crypto.subtle`.
Why this was made? Because a client served with `http` without SSL, which makes `window.crypto. subtle` unavailable.
(TODO: write more docs about Deskreen architecture)

## Get Started for Developers

### Prerequisites

You will need to have `node` `npm` and `yarn` installed
globally on your machine.

1. git clone this repo
2. `yarn install`
3. `yarn dev` -- run in dev mode with live updates

### Useful yarn commands

`yarn start` -- run in production mode to test, without packaging
`yarn package` -- to package an app and make executables available in `release` folder

#### for more yarn commands look at `package.json`

### How to run tests

`yarn test` -- run all unit tests
`yarn build-ux && yarn test-ux` -- run User Experience tests (no tests for `app/client` yet)

### TODO: add e2e tests with host + client app interaction

#### run tests of host app

`yarn test-watch-not-silent` -- run tests in watch mode with console logs only for host app, excluding `app/client`
`yarn test -- -u` -- update snapshots

#### run tests for `app/client`

`yarn test` -- run client tests in watch mode
`test:nowatch` -- run client tests a single time
`yarn test -- -u` -- update snapshots

### Generate test coverage results

`yarn coverage` -- when run from project root, generates a coverage report for `host` and `app/client`

## Instruction for running a local Sonar Qube, community edition

### Prerequisites

You need to install Sonar Qube community edition for your machine.
And sonar-scanner. Then add sonar scanner to your PATH.

You need to run sonar-scanner separately on root directory
and on `app/client` directory.

Luckily for you sonar scanner is automatically triggered after `husky` checks.
So you only need to install and configure SonarCube locally and
create two separate projects in SonarCube panel.
First project for host app, and second project for client viewer app.
TODO: add how to get started with local SonarCube for Deskreen in details.

## Maintainer

- [Pavlo (Paul) Buidenkov](https://www.linkedin.com/in/pavlobu)

## License

AGPL-3.0 License © [Pavlo (Paul) Buidenkov](https://github.com/pavlobu/deskreen)

## Copyright

MIT © [Electron React Boilerplate](https://github.com/electron-react-boilerplate)
Deskreen Logo PNG Image -- © [Nadiia Plaunova](https://www.artstation.com/nadiiia)

## Donate

Click to donate on Deskreen's Patreon page: [DONATE!](https://github.com/electron-react-boilerplate)
