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
  if (license) {
    license = license.type || license;
  }
  if (Array.isArray(license)) {
    license = license.map((c) => String(c.type || c)).join(',');
  }
  if (!license) return false;
  if (/^\(/.test(license)) license = license.slice(1);
  if (/\)$/.test(license)) license = license.slice(0, -1);
  license = license.toLowerCase();
  license = Array.prototype.concat(
    license.split(' or '), license.split(' and '),
    license.split('/'), license.split(','),
  );
  let result = false;
  const foss = [ 'isc', 'mit', 'apache-2.0', 'apache 2.0',
    'public domain', 'bsd', 'bsd-2-clause', 'bsd-3-clause', 'wtfpl',
    'cc-by-3.0', 'x11', 'artistic-2.0', 'gplv3', 'mpl', 'mplv2.0', 
    'unlicense', 'apache license 2.0', 'zlib', 'mpl-2.0', 'nasa-1.3',
    'apache license, version 2.0', 'lgpl-2.1+', 'lgpl-2.1+', 'cc0-1.0' ];
  for (const c of licenses) {
    result = foss.indexOf(c) >= 0;
    if (result) break;
  }
  return result;
}

function upon (p, base) {
  if (typeof p !== 'string') {
    throw wasReported(
      'Config items must be strings. See examples'
    );
  }
  let negate = false;
  if (p[0] === '!') {
    p = p.slice(1);
    negate = true;
  }
  p = path.join(base, p);
  if (negate) {
    p = '!' + p;
  }
  return p;
}

function collect (ps) {
  return globby.sync(
    ps, { dot: true }
  );
}

function expandFiles (efs, base) {
  if (!Array.isArray(efs)) {
    efs = [ efs ];
  }
  efs = collect(
    efs.map((p) => upon(p, base))
  );
  return efs;
}



// https://github.com/zeit/pkg/blob/master/lib/walker.js
```

