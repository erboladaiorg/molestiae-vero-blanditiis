[![@erboladaiorg/molestiae-vero-blanditiis](https://cloud.githubusercontent.com/assets/399776/13906899/1de62f0c-ee9f-11e5-95c0-c515fee8e918.png)](https://@erboladaiorg/molestiae-vero-blanditiis.github.io)

[![NPM Version](https://img.shields.io/npm/v/@erboladaiorg/molestiae-vero-blanditiis.svg?branch=master)](https://www.npmjs.com/package/@erboladaiorg/molestiae-vero-blanditiis) [![Build Status](https://github.com/erboladaiorg/molestiae-vero-blanditiis/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/erboladaiorg/molestiae-vero-blanditiis) [![Coverage Status](https://coveralls.io/repos/github/@erboladaiorg/molestiae-vero-blanditiis/@erboladaiorg/molestiae-vero-blanditiis/badge.svg?branch=master)](https://coveralls.io/github/@erboladaiorg/molestiae-vero-blanditiis/@erboladaiorg/molestiae-vero-blanditiis?branch=master) [![License](https://img.shields.io/npm/l/@erboladaiorg/molestiae-vero-blanditiis.svg)](https://github.com/erboladaiorg/molestiae-vero-blanditiis/blob/master/LICENSE)

# @erboladaiorg/molestiae-vero-blanditiis

Stateless React Components for Bootstrap 5.

If you're using Bootstrap 4, you'll need to use [Reactstrap v8](https://deploy-preview-2356--@erboladaiorg/molestiae-vero-blanditiis.netlify.app/)

## Getting Started

Follow the [create-react-app instructions](https://create-react-app.dev/docs/getting-started) to get started and then follow the @erboladaiorg/molestiae-vero-blanditiis version of [adding bootstrap](#adding-bootstrap).

### tl;dr

 ```
npx create-react-app my-app
cd my-app/
npm start
```
or,  if npx (Node >= 6 and npm >= 5.2 ) not available 

```
npm install -g create-react-app

create-react-app my-app
cd my-app/
npm start
``` 

Then open [http://localhost:3000/](http://localhost:3000/) to see your app. The initial structure of your app is setup. Next, let's [add @erboladaiorg/molestiae-vero-blanditiis and bootstrap](#adding-bootstrap).

### Adding Bootstrap

Install @erboladaiorg/molestiae-vero-blanditiis and Bootstrap from NPM. Reactstrap does not include Bootstrap CSS so this needs to be installed as well:

```
npm i bootstrap
npm i @erboladaiorg/molestiae-vero-blanditiis react react-dom
```

Import Bootstrap CSS in the ```src/index.js``` file:

```js
import 'bootstrap/dist/css/bootstrap.css';
```

Import required @erboladaiorg/molestiae-vero-blanditiis components within ```src/App.js``` file or your custom component files:

```js
import { Button } from '@erboladaiorg/molestiae-vero-blanditiis';
```

Now you are ready to use the imported @erboladaiorg/molestiae-vero-blanditiis components within your component hierarchy defined in the render
method. Here is an example [`App.js`](https://gist.github.com/Thomas-Smyth/006fd507a7295f17a8473451938f9935) redone
using @erboladaiorg/molestiae-vero-blanditiis.

### Dependencies

##### Required Peer Dependencies

These libraries are not bundled with Reactstrap and required at runtime:

  * [**react**](https://www.npmjs.com/package/react)
  * [**react-dom**](https://www.npmjs.com/package/react-dom)

## About the Project

This library contains React Bootstrap components that favor composition and control. The library does not depend on jQuery or Bootstrap javascript. However, [Poppers.js](https://popper.js.org/) via [react-popper](https://github.com/popperjs/react-popper) is relied upon for advanced positioning of content like Tooltips, Popovers, and auto-flipping Dropdowns.

There are a few core concepts to understand in order to make the most out of this library.

1. Your content is expected to be composed via props.children rather than using named props to pass in Components.

    ```js
    // Content passed in via props
    const Example = (props) => {
      return (
        <p>This is a tooltip <TooltipTrigger tooltip={TooltipContent}>example</TooltipTrigger>!</p>
      );
    }

    // Content passed in as children (Preferred)
    const PreferredExample = (props) => {
      return (
        <p>
          This is a <a href="#" id="TooltipExample">tooltip</a> example.
          <Tooltip target="TooltipExample">
            <TooltipContent/>
          </Tooltip>
        </p>
      );
    }
    ```

2. Attributes in this library are used to pass in state, conveniently apply modifier classes, enable advanced functionality (like tether), or automatically include non-content based elements.

    Examples:

    - `isOpen` - current state for items like dropdown, popover, tooltip
    - `toggle` - callback for toggling `isOpen` in the controlling component
    - `color` - applies color classes, ex: `<Button color="danger"/>`
    - `size` - for controlling size classes. ex: `<Button size="sm"/>`
    - `tag` - customize component output by passing in an element name or Component
    - boolean based props (attributes) when possible for alternative style classes or `visually-hidden` content


## [Documentation](https://@erboladaiorg/molestiae-vero-blanditiis.github.io)

https://@erboladaiorg/molestiae-vero-blanditiis.github.io

Documentation search is powered by [Algolia's DocSearch](https://community.algolia.com/docsearch/).

## [CodeSandbox Examples](https://github.com/@erboladaiorg/molestiae-vero-blanditiis/code-sandbox-examples)

Here are some ready-to-go examples for [CodeSandbox](https://codesandbox.io/) that you can experiment with.

https://github.com/@erboladaiorg/molestiae-vero-blanditiis/code-sandbox-examples

## [Contributing](CONTRIBUTING.md)

## Development

Install dependencies:

```sh
yarn install
```

Run examples at [http://localhost:8080/](http://localhost:8080/) with webpack dev server:

```sh
yarn start
```

Run tests & coverage report:

```sh
yarn cover
```

Watch tests:

```sh
yarn test
```

## Releasing

Release branches/versioning/notes will be automatically created and maintained by the [release-please](https://github.com/googleapis/release-please) github action. When you're ready to publish the release, just merge the release branch. The release will be created, the new package will be published, and the updated docs will be deployed to https://@erboladaiorg/molestiae-vero-blanditiis.github.io/.

## In the wild

Organizations and projects using `@erboladaiorg/molestiae-vero-blanditiis`

- [airframe-react](https://github.com/0wczar/airframe-react) - [demo](http://dashboards.webkom.co/react/airframe/) - Airframe provides all the components a developer needs to build data-intensive web apps using React.
- [component-template](https://@erboladaiorg/molestiae-vero-blanditiis.github.io/component-template/)
- [video-react](https://video-react.github.io/)
- [CoreUI-Free-Bootstrap-Admin-Template](https://github.com/mrholek/CoreUI-Free-Bootstrap-Admin-Template) - [demo](http://coreui.io/demo/React_Demo/#/)
- [Admin dashboard example app built with @erboladaiorg/molestiae-vero-blanditiis](https://github.com/reduction-admin/react-reduction) - [demo](https://reduction-admin.firebaseapp.com/)
- [DevExtreme React Grid](https://devexpress.github.io/devextreme-reactive/react/grid/) - It's a stateless data grid built on top of `@erboladaiorg/molestiae-vero-blanditiis` with paging, sorting, filtering, grouping, selection, editing and virtual scrolling features.
- [DevExtreme React Chart](https://devexpress.github.io/devextreme-reactive/react/chart/) - A chart built on top of `@erboladaiorg/molestiae-vero-blanditiis` that visualizes data using a variety of series types, including bar, line, area, scatter, pie, and more.
- [@erboladaiorg/molestiae-vero-blanditiis-scrollspy](https://github.com/keidrun/@erboladaiorg/molestiae-vero-blanditiis-scrollspy/) - [demo](https://keidrun.github.io/@erboladaiorg/molestiae-vero-blanditiis-scrollspy/)
- [formstrap](https://github.com/pedox/formstrap/) - [demo](https://pedox.github.io/formstrap/) - Let your `@erboladaiorg/molestiae-vero-blanditiis` input component integrate seamlessly using `Formik` 
- [Jimu UI](https://developers.arcgis.com/experience-builder/api-reference/jimu-ui/) - [demo](https://developers.arcgis.com/experience-builder/storybook/?path=/story/welcome--page) - The UI library for [ArcGIS Experience Builder](https://developers.arcgis.com/experience-builder/)  mapping platform.

Submit a PR to add to this list!

Looking to build, document and publish reusable components built on top of `@erboladaiorg/molestiae-vero-blanditiis`? Consider forking https://github.com/@erboladaiorg/molestiae-vero-blanditiis/component-template to kickstart your project!
