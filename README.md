# Angular APP

### Steps to reproduce

* Generate a new project (`ng new test-app --skip-install`) with:
    * Angular CLI: 14.2.1
    * Node: 16.14.0
    * Package Manager: npm 8.5.3
    * OS: darwin x64

* Change the Angular version in package.json to `^14.2.0`

* Run `npm i`

* Add the localize package with `ng add @angular/localize` as described [here](https://angular.io/guide/i18n-common-add-package)

* Modify the angular.json to add the following:

   * [Define locales in the build configuration](https://angular.io/guide/i18n-common-merge#define-locales-in-the-build-configuration)
   * [Generate application variants for each locale](https://angular.io/guide/i18n-common-merge#generate-application-variants-for-each-locale)

* Install @angular/pwa pacakge as described [here](https://angular.io/guide/service-worker-getting-started#adding-a-service-worker-to-your-project)

* See the modifications done in the angular.json in the last commit

* Serve the app and see the following error:

```
[webpack-dev-middleware] Error: ENOENT: no such file or directory, readdir '<project-directory>/test-app/dist/test-app/'
    at createError (<project-directory>/test-app/node_modules/memfs/lib/volume.js:128:17)
    at Volume.readdirBase (<project-directory>/test-app/node_modules/memfs/lib/volume.js:1415:19)
    at Immediate.<anonymous> (<project-directory>/test-app/node_modules/memfs/lib/volume.js:695:33)
    at processImmediate (node:internal/timers:466:21) {
  code: 'ENOENT'
}
```
