# Inconsistent resolution of imports/exports map with `moduleResolution: "Bundler"`

```
> ts-packagejson-import-maps-bug@1.0.0 tsc
> tsc

test/exports-map.ts:1:31 - error TS2307: Cannot find module 'ts-packagejson-import-maps-bug/components/MyComponent' or its corresponding type declarations.

1 import * as myComponent1 from "ts-packagejson-import-maps-bug/components/MyComponent";
                                ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

test/exports-map.ts:5:25 - error TS2307: Cannot find module 'tslib/modules' or its corresponding type declarations.

5 import * as tslib1 from 'tslib/modules'
                          ~~~~~~~~~~~~~~~

test/exports-map.ts:6:25 - error TS2307: Cannot find module 'tslib/modules/index' or its corresponding type declarations.

6 import * as tslib2 from 'tslib/modules/index'
                          ~~~~~~~~~~~~~~~~~~~~~

test/imports-map.ts:1:31 - error TS2307: Cannot find module '#components/MyComponent' or its corresponding type declarations.

1 import * as myComponent1 from "#components/MyComponent";
                                ~~~~~~~~~~~~~~~~~~~~~~~~~


Found 4 errors in 2 files.

Errors  Files
     3  test/exports-map.ts:1
     1  test/imports-map.ts:1
```