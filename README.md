# jest-canary-18.5.0-alpha.7da3df39
Demonstrate error in Jest 19 alpha

```sh
yarn install
npm test

module.js:472
    throw err;
    ^

Error: Cannot find module 'json-stable-stringify'
    at Function.Module._resolveFilename (module.js:470:15)
    at Function.Module._load (module.js:418:25)
    at Module.require (module.js:498:17)
    at require (internal/module.js:20:19)
    at Object.<anonymous> (/Users/mark/gitrepos/jest-canary-18.5.0-alpha.7da3df39/node_modules/jest-runtime/build/transform.js:22:25)
    at Module._compile (module.js:571:32)
    at Object.Module._extensions..js (module.js:580:10)
    at Module.load (module.js:488:32)
    at tryModuleLoad (module.js:447:12)
    at Function.Module._load (module.js:439:3)
```

https://github.com/facebook/jest/blob/master/packages/jest-runtime/src/transform.js#L22

`node_modules` folder had `json-stable-stringify` as of a few days ago but not this build.
