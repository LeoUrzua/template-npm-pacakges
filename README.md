# template-npm-packages

This repository hosts the code that automate the npm package publications to different registries.

This repository provides the following benefits, and also you can configure them.

* semantic-realese.
* commit convention.
* CI/CD

```
CI: on every push
CD: on every push to master
```

## Table of Contents
    
- [Introduction](#introduction)
- [Local Installation](#local-installation)
  - [Prerequisites](#prerequisites)
  - [Installing](#installing)
- [Tests](#tests)
- [Publication](#publication)
- [Customization](#customization)
- [Contribution](#contribution)
- [Versions](#versions)
- [License](#license)

## Introduction

The technologies used include:

- `semantic-release` to have semantic-release versioning.
- `husky` to trigger hooks.
- `commitlint` helps your team adhering to a commit convention.


[⇧ back to top](#table-of-contents)

## Local Installation

This section describes how to run the project locally, so that you can develop
and test the code.

[⇧ back to top](#table-of-contents)

### Installing

Open a terminal and follow the next steps
to install the project:

1. Clone the repository:

   ```shell
   git clone https://github.com/LeoUrzua/template-npm-pacakges.git [your-project-name]
   ```

1. Move into the newly created folder:

   ```shell
   cd [your-project-name]
   ```

1. Install the project dependencies:

   ```shell
   npm install
   ```
   
1. Start to develop your package

1. Use `npm run commit` to use [Commitizen](http://commitizen.github.io/cz-cli/) to help you format your commit messages

[⇧ back to top](#table-of-contents)

## Tests

The following tests are available.

```shell
npm test
```

[⇧ back to top](#table-of-contents)

## Customization 

To publish your npm package to a different registry you need to do some changes in the `package.json` file


```json
{
  "publishConfig": {
    "registry": "https://npm.pkg.github.com/@LeoUrzua"
  }
}
```

Note: in the example above we are publishing to the `npm` registry to the `LeoUrzua` organization

to 

```json
{
  "publishConfig": {
    "registry": "[your-npm-registry]/@[your-org]"
  }
}
```

## Publication

This package could be pusblished to any registry we just need to create a new secret: `NPM_TOKEN` here: `https://github.com/[your-org]/[your-package]/settings/secrets`

That token generation is going to depend on the registry that you want to publish

github registry:

* Generate a personal access token in GitHub at the following site:
   `https://github.com/settings/tokens`. 

	**Note:** Select the **write:packages**, **read:packages**,  and **repo** option and all its children.

To publish to the npm registry

* Generate your npm token in `https://www.npmjs.com/settings/[your-organization]/tokens`


[⇧ back to top](#table-of-contents)

## Contribution

TBD.

[⇧ back to top](#table-of-contents)

## Versions

TBD.

[⇧ back to top](#table-of-contents)

## License

TBD.

[⇧ back to top](#table-of-contents)
