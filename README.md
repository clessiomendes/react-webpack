# Grails React-Webpack Profile
A profile for creating Grails applications with a React frontend using Webpack (requires Grails 3.3.2 or greater)

[![Build Status](https://travis-ci.org/grails-profiles/react-webpack.svg?branch=master)](https://travis-ci.org/grails-profiles/react-webpack)


```
grails create-app myApp -profile react-webpack
```

This profile is based on the approach described in this post: http://grailsblog.objectcomputing.com/posts/2016/05/28/using-react-with-grails.html  Please read this post for more information.

This profile is a superset of the `webpack` profile, which can be found here: https://github.com/grails-profiles/webpack

# Getting Started

To get started with this profile, simply run the Grails application using `grails run-app` or `./gradlew bootRun`. The profile will configure the Gradle-node plugin (https://github.com/srs/gradle-node-plugin) with `npm` scripts to build the React application on build time. This way the React app will be bundled and ready to serve every time you start the app.

In order to take advantage of webpack's "watch" mode to automatically reload changes, you will need to run webpack along with the Grails application. Use `npm run webpack` or use the Gradle wrapper: `./gradlew webpack`

# Running Tests

Mocha is configured to run tests from `src/main/js`. Run it using `npm run test` or use the Gradle wrapper: `./gradlew mochaTest`.

