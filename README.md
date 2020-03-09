<h1 align="center">
  <a href="https://www.gatsbyjs.org">
    <img alt="Gatsby" src="https://www.gatsbyjs.org/monogram.svg" width="64" valign="middle" />
  </a>
  +
  <a href="https://relative-ci.com">
    <img alt="RelativeCI" src="https://raw.githubusercontent.com/relative-ci/agent/master/assets/relative-ci--logo.svg?sanitize=true" width="64" valign="middle" />
  </a>
</h1>

<p align="center">
  <a href="https://app.relative-ci.com/projects/PqaxqCUHsTMEg1aq30QX"><img src="https://badges.relative-ci.com/badges/PqaxqCUHsTMEg1aq30QX?branch=master" alt="relativeCI"></a>
</p>

> [@relative-ci/agent webpack plugin](https://github.com/relative-ci/agent) setup example for Gatsby & Gatsby Cloud

## 1. Installation

```shell
npm install --save-dev @relative-ci/agent
# or
yarn add --dev @relative-ci/agent
```

## 2. Webpack plugin configuration 

[`gatsby-node.js`](https://github.com/relative-ci/example-gatsby/tree/master/gatsby-node.js#L1-L9)
```js
const { RelativeCiAgentWebpackPlugin } = require("@relative-ci/agent")

exports.onCreateWebpackConfig = ({ stage, actions }) => {
  if (stage === "build-javascript") {
    actions.setWebpackConfig({
      plugins: [new RelativeCiAgentWebpackPlugin()],
    })
  }
}
```

To fully configure the service, follow the [setup instructions](https://relative-ci.com/documentation/setup).
