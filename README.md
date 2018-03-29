# CircleCI Demo React Native App

[![CircleCI](https://circleci.com/gh/CircleCI-Public/circleci-demo-react-native.svg?style=svg)](https://circleci.com/gh/CircleCI-Public/circleci-demo-react-native)

## Building and running locally

1. Run `yarn` to install the JS dependencies.
2. Run `yarn test` to run the JS tests (via `jest`).
3. Run `yarn start` to run the app in development mode. You can open it
   in the [Expo app](https://expo.io) on your phone. It will reload as
   you save edits to your files. You will see error messages and logs in
   your terminal window.

### Running the iOS app in the iOS simulator

This requires Xcode 9 or newer.

1. Run `bundle install` in the `ios` directory to install all
   dependencies.
2. Run `yarn run ios` to start the app in the iOS simulator.

You can also build the app directly by opening the iOS project in Xcode
and clicking **Product** -> **Run**.

To run tests, either select **Product** -> **Test** in Xcode, or run
`bundle exec fastlane test` in the command line inside the `ios`
directory.

### Running the Android app in the Android emulator.

1. Run `bundle install` in the `android` directory to install all
   dependencies.
2. Run `yarn run android` to start the app in the Android emulator.

To run tests, run `bundle exec fastlane test` in the command line inside
the `android` directory.

### Running tests using the CircleCI CLI

You can run individual jobs from the [configuration
file](https://github.com/CircleCI-Public/circleci-demo-ios/blob/master/.circleci/config.yml)
using the CircleCI CLI.

Please see [this doc](https://circleci.com/docs/2.0/local-jobs/#nav-button)
for details on how to install the CLI. Once it is installed, you can run
the `build` job by running the following in the root of this repo:

```bash
circleci build
```

To run the Android job, you can run the following:

```bash
circleci build --job android
```

It is currently not possible to run the iOS job locally.

## Building on CircleCI

This example is ready to be built on CircleCI. Once you have copied or
forked the repository, navigate to the CircleCI web interface, choose
**Projects** and then **Add project**. Select a project and click
**Start building**.

Try pushing some changes to your repo to see how a JS job runs, and
then the Android and iOS tests get run concurrently.
