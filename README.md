# Vision Cat


## Dependencies
- node & npm - http://nodejs.org/download/
  - gulp: `npm install --global gulp` - http://gulpjs.com/
  - bower: `npm install --global bower` - http://bower.io/
  
## Running in the browser
```sh
gulp watch
```

#### Cordova CLI wrapper
```sh
gulp --cordova '<run any cordova command>'
```

# cordova command with local wrapper
gulp --cordova 'plugin add org.apache.cordova.camera --save'
```

#### Run on device or simulator
If you want to run your app on your connected iOS or Android device or a simulator run:
```sh
gulp --cordova 'run ios --device' # runs gulp build, then cordova run ios
gulp --cordova 'run android' # same for android

```
or
```sh
gulp --cordova 'emulate ios'
gulp --cordova 'emulate android'
```

#### Run using Xcode instead of command line
In order to view changes that you made in the project run the following:

```sh
gulp --cordova 'prepare ios'
# or individually
gulp build
gulp --cordova 'prepare ios' --no-build
```
Then run or simulate via Xcode.

# File structure
<pre>
└──  app/ - your application folder
│   └──  bower_components/    - local installation of bower packages
│   └──  main/                - ---main module---
│   │   ├──  assets/          - assets: fonts, images, translation, etc... go here
│   │   ├──  constants/       - angular constants
│   │   ├──  controllers/     - angular controllers
│   │   ├──  directives/      - angular directives
│   │   ├──  filters/         - angular filters
│   │   ├──  services/        - angular services
│   │   ├──  styles/          - scss styles
│   │   ├──  templates/       - angular templates
│   │   └──  main.js          - angular module definition, routing etc...
│   └──  anotherModule/       - ---another  module---
│   │   ├──  ...
│   ├──  app.js               - application module, includes main module, ionic, ui-router etc ...
│   └──  index.html           - angular entry point, injects: app files, bower files, fonts,  ...
├──  gulp/              - gulp tasks
├──  hooks/             - cordova hooks
├──  nodes_modules/     - local installation of node modules
├──  platforms/         - cordova platforms
├──  plugins/           - corodova plugins
├──  res/               - resources folder for splash screens and app icons
├──  test/              - unit and integration tests
├──  www/               - your gulp build goes here, cordova starts building from here
├──  .bowerrc           - bower configuration
├──  .editorconfig      - editor configuration
├──  .eslintignore      - ESLint ignore configuration
├──  .eslintrc          - ESLint configuration
├──  .gitattributes     - git's attribute configuration
├──  .gitignore         - git's ignore configuration
├──  .travis.yml        - travis continuous integration configuration
├──  .yo-rc.json        - yeoman's .yo-rc.json
├──  bower.json         - bower dependencies
├──  config.xml         - cordova's config.xml
├──  gulpfile.js        - entry point to all gulp tasks
├──  jenkins.sh         - shell script for jenkins continuous integration
├──  karma.conf.js      - karma configuration
├──  package.json       - node dependencies configuration
├──  protractor.conf.js - protractor configuration
├──  README.md          - the apps README.md
</pre>
