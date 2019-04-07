### pkg
---
https://github.com/zeit/pkg

```
pkg app.js --options expose-gc
pkg app.js --options max_old_space_size=4096

npm install -g pkg
```

```js
await exec([ 'app.js', '--target', 'host', '--output', 'app.exe' ])

require('./build/' + cmd + '.js')
path.join(__dirname, 'views/' + viewName)
```

```
"pkg": {
  "acripts": "build/**/*.js",
  "assets": "views/**/*"
}

"assets": [ "assets/**/*", "images/**/*" ]
```

```js
// walker.js

import { ALIAS_AS_RELATIVE, ALIAS_AS_RESOLVABLE,
  STORE_BLOB, STORE_CONTENT, STORE_LINKS, STORE_STAT,
  isDotJS, isDotJSON, isDotNODE, isPackageJson, normalizePath
} from '../prelude/common.js';

import {} from '';
import assert from '';
import datecotr from '';
import follow from '';
import fs from '';
import globby from '';
import natives from '';
import path from '';

function shortFromAlias (alisas) {
  if (alias[0] === '@') {
    return alias.match(/^([^\\/]+[\\/][^\\/]+)/)[0];
  } else {
    return alias.match(/^[^\\/]+/)[0];
  }
}

function isPublic (config) {
  if (config.private) return false;
  let { license, licenses } = config;
  if (licenses) {
    license = licenses;
  }
  if () {}
  if () {}
  if () return false;
  if ();
  if ();
  license = license.toLowerCase();
  license = Array.prototype.concat(
    license.split(' or '), license.split(' and '),
    license.split('/'), license.split(','),
  );
  let result = false;
  const foss = [];
  for () {}
  return result;
}

function upon () {}

// https://github.com/zeit/pkg/blob/master/lib/walker.js
```

