<img width="1600" alt="From Zero to Hero" src="https://user-images.githubusercontent.com/103318089/184580274-219a8e5c-29c7-4c06-b6d5-af4b015880ba.png">

## :speech_balloon: Intro

This repository contains a collection of material and advanced features of Python programming and the Python Ecosystem including as part of the PYTHON FOR DATA ANALYSIS II course of the Part-Time MASTER IN BUSINESS ANALYTICS AND BIG DATA.

This course is intended for people who have learned some basics of Python and are looking to deepen their Python skills and take the next step. Before moving  on to the coding part, I will explain the intuition behind advanced topics. So you can understand not only what it is, but also why we are bringing it up and what the practical use of this concept is. I will try to explain all topics as real examples as possible so that later you can develop something useful from them.


## :package: How to use this repository

Each Python topic in this repository has the following structure

- Find the topic you want to learn or review
- Read the linked and/or documented comments  in each script's docstring (like in the example above). 
- Look at the code samples and validation to see usage examples and expected output. 
- Modify the code or add a new assertion to see how everything works. 
- Run tests and analyze the code to see if it works and is written correctly.


<div id="getting-started"></div>

## :rocket: Table of Contents

- [Functional Programming](https://github.com/dianisley/PythonfromZerotoHero/blob/78cd7d2c6a70e5a1e5487434cb9d1ec93998c2e1/Functional%20Programming/ReadmeFP)
- [Object Oriented Programming](https://github.com/dianisley/PythonfromZerotoHero/blob/54fd6c8b08b153508f71ffcaa58743ddedb15e8a/Object%20Oriented%20Programming/ReadmeOOP.md)
- [Object Relational Mapping](https://github.com/dianisley/PythonfromZerotoHero/blob/d925880d32bfb39d8b5f47a11077bf797d41c327/Object%20Relational%20Mapping/ReadmeORM.md)
- [Github and Pypi](https://github.com/dianisley/PythonfromZerotoHero/blob/00c74bb7491487de6320d1ac5434e7744a8a5e2b/Git%20and%20Pypi/ReadmeGit.md)
- [Scipy - Statistical Python](https://github.com/dianisley/PythonfromZerotoHero/blob/a20b4138c033af345ef42560760dcb21c0d7fcb3/Scipy%20Statistical%20Python/ReadmeSci.md)
- [Web Development](https://github.com/dianisley/PythonfromZerotoHero/blob/25107070df977ed2fa7545f342823cf436b80d1a/Web%20Development/ReadmeWD.md)
- [Graphing on Web](https://github.com/dianisley/PythonfromZerotoHero/blob/944d37d60ec448d30231730e75858cff59c4d9f7/Python%20Dynamic%20Graphing%20on%20Web%20Browsers/ReadmeGW.md)

</details>

### Npm&Yarn install:

```bash
#Nostalgic
$ npm install repo-name
#Hipster
$ yarn add repo-name
```

>descr (if needed)
### Clone the repo:

Clone the repo to get all source files as they are available on Github:

```bash
$ git clone https://github.com/your-github-name/repo-name.git
$ cd repo-name/
```

And then install NPM-Modules via:

```bash
#Nostalgic
npm install
#Hipster
yarn
```

This install the required __node_modules__.

>descr (if needed)
<a href="#contents">:top: <sub>back to top</sub></a>

<div id="technologies-used"></div>

## :bento: Technologies used

>Technologies or features that you used when creating the project.
>For example:
<details>
  <summary><strong>JavaScript</strong></summary>

- [ES2017](https://medium.com/komenco/what-to-expect-from-javascript-es2017-the-async-edition-618e28819711) - support through compiler [Babel](https://babeljs.io/).

- [Node](https://nodejs.org/) - is an open-source, cross-platform JavaScript run-time environment that executes JavaScript code outside of a browser.

</details>

<details>
  <summary><strong>Testing</strong></summary>

- [Cypress](https://www.cypress.io/) - is a fast, easy and reliable testing for anything that runs in a browser.

</details>

<details>
  <summary><strong>Styles</strong></summary>

- [Sass](https://sass-lang.com/) - is the most mature, stable, and powerful professional grade CSS extension language in the world.

- [Sassdoc](http://sassdoc.com/) - is a documentation system to build pretty and powerful docs in the blink of an eye.

- [PostCSS](https://postcss.org/) - is a tool for transforming CSS with JavaScript.

- [Critical](https://github.com/addyosmani/critical) - extracts & inlines critical-path (above-the-fold) CSS from HTML.

</details>

<details>
  <summary><strong>Automation</strong></summary>

- [Gulp](https://gulpjs.com/) - is a toolkit for automating painful or time-consuming tasks in your development workflow.

- [Webpack](https://webpack.js.org/) - is a bundler for modules.

</details>

<details>
  <summary><strong>Optimization</strong></summary>

- [Imagemin](https://github.com/imagemin/imagemin) - minify PNG, JPEG, JPG, GIF and SVG images.

- [Uglify](https://github.com/mishoo/UglifyJS2) - is a JavaScript parser, minifier, compressor and beautifier toolkit.

</details>

<details>
  <summary><strong>Server</strong></summary>

- [BrowserSync](http://www.browsersync.io/) - is a time-saving synchronised browser testing.

</details>

<details>
  <summary><strong>Linting</strong></summary>

- [ESlint](http://eslint.org/) - is to provide a pluggable linting utility for JavaScript.

- [HTMLHint](https://htmlhint.io/) - is a Static Code Analysis Tool for HTML.

- [Stylelint](https://stylelint.io/) - is a mighty, modern linter that helps you avoid errors and enforce conventions in your styles.

- [Prettier](https://prettier.io/) - is an opinionated code formatter.

</details>

<details>
  <summary><strong>Code Management</strong></summary>

- [Editorconfig](http://editorconfig.org/) - helps developers define and maintain consistent coding styles between different editors and IDEs.

- [Git](https://git-scm.com/) - is a distributed version control system designed to handle everything from small to very large projects.

</details>

<a href="#contents">:top: <sub>back to top</sub></a>

<div id="commands"></div>

## :triangular_flag_on_post: Commands

>An example of the presentation of commands for working with your project, in the form of a table.
 _With Webpack you have to use NPM Script Commands_

| Action                                                                                      | Npm                  | Yarn              |
| :------------------------------------------------------------------------------------------ | :------------------: | :---------------: |
| Intialize your Project and the Sass Documentation (/sassdocs/)                              | `npm run init`       | `yarn run init`   |
| Main development task with BrowserSync and Webpack                                          | `npm run dev`        | `yarn dev`        |
| Minify JS, Images, CSS. Is for a automated Build Process, comes after a Gulp Init.          | `npm run build`      | `yarn build`      |
| Rebuild all JS Files except the Application JS File                                         | `npm run scripts`    | `yarn scripts`    |
| Rebuild all Image Files for CSS, copy it to distribution, build Bitmap- and Vector Sprites. | `npm run uiimages`   | `yarn uiimages`   |
| Copy all Imagefiles for Documentusage.                                                      | `npm run htmlassets` | `yarn htmlassets` |
| Copy all or Generate the Template Files.                                                    | `npm run template`   | `yarn template`   |
| Generate Favicons and the HTML Snippet (generated Files you will find in `src/.system/`)    | `npm run favicon`    | `yarn favicon`    |

<a href="#contents">:top: <sub>back to top</sub></a>

<div id="structure"></div>

## :wrench: Structure

>Description of the structure of your project.
>Example schema that illustrates it (if needed):
**SRC Folderstructure:**

```
src/
├── .system/                          => Internal System Files
├── fonts/                            => Font Files
├── framework/                        => Sass Framework
├── images/                           => All Images
|   ├── bitmapSingle-assets           => Single Bitmap Images
|   ├── bitmapSprite-assets           => Images for Bitmap Sprites
|   ├── htmlimages                    => Content Images (`<img>`)
|   ├── vectorSingle-assets           => Single Vector Images
|   └── vectorSprite-assets           => Vector Images for Vector Sprites
├── js/                               => JS Files (e.g. main.js)
├── scripts/                          => Script files that are not installed
├── structure/                        => Source Files for Copy (e.g. Template Files for a WP Theme)
└── style/                            => Styling Source Files
```

<a href="#contents">:top: <sub>back to top</sub></a>

<div id="build"></div>

## :hammer: Build

>Description of the build of your project and its subtleties of implementation
<a href="#contents">:top: <sub>back to top</sub></a>

<div id="license"></div>

## :page_facing_up: License

>Your License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

[![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/your-github-name/repo-name/blob/master/LICENSE)

<a href="#contents">:top: <sub>back to top</sub></a>

<div id="author"></div>

## :penguin: Author

Author : Diana Fernandez
Email : dianaf@student.ie.edu
Github : https://github.com/dianisley/PythonfromZerotoHero.git


[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)

