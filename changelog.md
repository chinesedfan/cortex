# Change Log, TL;DR

## 6.x

- **6.2.0**:
  - support load module with md5 hash
  - use cache object to prevent css background image copy multi times
  - fix cortex install not read --dest argument
  - fix bug in node-replier which will cause broken message on huge json send
  - improve cortex watch performance
  - add `cortex neuron-version` to output bundled neuron version

- **6.1.0**:
  - [#489][489]: Adds command `cortex link` to link a global dependency
  - `cortex install` will skip existing packages by default but `--force` to force installing. [#491][491]
  - support error handling with node-notifier
  - supporting specify init template
  - add postwatch and postbuild hooks
  - add directories.img, directories.html, directories.font
  - support traverse install asyncDependencies

- **6.0.0**:
  - [#476][476]: Handle pre-release versions to solve the problem of deploying projects at different pre-release stages.

## 5.x

- **5.7.0**:
  - [#458][458]: Use ini instead of JSON for more complicated configurations in the future.
  - [#463][463]: Cortex will explode NEURON_VERSION and current bin path when spawns.
- **5.6.0**: [#452][452]: Completely support cyclic dependencies. Modules will run in complete separated sandboxes, supports all impossibilies of dependency graph.
- **5.5.0**:
  - [#443][443]: `cortex install --stable-only` to force install stable versions.
  - [#442][442]: neuron.js will be a symlink.
  - [#445][445]: `cortex shrinkwrap` will adds `engines` field of neuron by default.
- **5.4.0**: [#436][436]: Supports `cortex.as` to set the alias of a package.
- **5.3.0**:
  - [#429][429]: Completely support [File Modules](http://nodejs.org/api/modules.html#modules_file_modules), `require()` directories, `__dirname` and `__filename`.
  - [#430][430]: Cortex build will transform filenames to lowercased paths.
- **5.2.0**: A new command `cortex ls` to print the dependency tree.
- **5.1.0**: [#386][386]: Supports packages with entries but no main entry, but this kind of packages could not be published.
- **5.0.0**: [#396][396]:
  - Full support for [semver ranges](https://github.com/mojombo/semver/issues/113).
  - Completely refactors module management and package management.

## 4.x
.
4.x contains several important refactors, including:

- **4.5.0**: [#393][393]: Supports ranges like `^0.1.0` and validates ranges.
- **4.4.0**: [#388][388]: Improves the performance of cortex build by using `fs.symlink` to create ranges.
- **4.3.0**
  - [#381][381]: Removes `config.server_mode`;
  - [#281][281]: Creates a symbolic link from "neurons" to `built_root`.
- **4.2.0**: [#372][372]: Better cortex update.
  No longer publish package.json by default.
- **4.1.0**: [#362][362]: `cortex.css` supports glob.
- **4.0.0**:
  - [#351][351]: Redesigns, removes `directories.css`, `directories.template`.
  - Supports package with only css files.

## 3.x

- **3.29.0**: `cortex install --save` and `cortex update` will also update cortex-shrinkwrap.json(if exists).
- **3.28.0**: [#344][344] [#342][342]: Migrate cortex plugin shrinkwrap as a builtin command.
- **3.27.0**: [#341][341]: Support package.engines.
- **3.26.0**: [#338][338], [#339][339]: Support install from cortex-shrinkwrap.json; Support more directories.
- **3.25.0**: [#325][325]: Better support for plugins. Eliminates all synchronous invocations of fs.
- **3.24.0**: [#284][284], [#285][285]: Builder and initializer are now built-in modules.
- **3.23.2**: [#304][304]: Improves all logics about async by using `async.eachSeries` and `async.each`.
- **3.23.1**: [#303][303]: Removes all sync fs.
- **3.23.0**: [#297][297]: Ignores empty folders and `node_modules` directory by default when publishing. Fixes the bug that directories could not be ignored.
- **3.22.1**: Redesigns cortex config command and bug fixes.
- **3.19.0**: Redesigns path calculation to make sure it won't be wrong.


## Former

Oh, the changes are too old to track :p

[491]: https://github.com/cortexjs/cortex/issues/491
[489]: https://github.com/cortexjs/cortex/issues/489
[476]: https://github.com/cortexjs/cortex/issues/476
[463]: https://github.com/cortexjs/cortex/issues/463
[458]: https://github.com/cortexjs/cortex/issues/458
[452]: https://github.com/cortexjs/cortex/issues/452
[442]: https://github.com/cortexjs/cortex/issues/442
[443]: https://github.com/cortexjs/cortex/issues/443
[445]: https://github.com/cortexjs/cortex/issues/445
[436]: https://github.com/cortexjs/cortex/issues/436
[429]: https://github.com/cortexjs/cortex/issues/429
[430]: https://github.com/cortexjs/cortex/issues/430
[396]: https://github.com/cortexjs/cortex/issues/396
[393]: https://github.com/cortexjs/cortex/issues/393
[388]: https://github.com/cortexjs/cortex/issues/388
[381]: https://github.com/cortexjs/cortex/issues/381
[281]: https://github.com/cortexjs/cortex/issues/281
[372]: https://github.com/cortexjs/cortex/issues/372
[362]: https://github.com/cortexjs/cortex/issues/362
[351]: https://github.com/cortexjs/cortex/issues/351
[344]: https://github.com/cortexjs/cortex/issues/344
[342]: https://github.com/cortexjs/cortex/issues/342
[341]: https://github.com/cortexjs/cortex/issues/341
[338]: https://github.com/cortexjs/cortex/issues/338
[339]: https://github.com/cortexjs/cortex/issues/339
[325]: https://github.com/cortexjs/cortex/issues/325
[284]: https://github.com/cortexjs/cortex/issues/284
[304]: https://github.com/cortexjs/cortex/issues/304
[303]: https://github.com/cortexjs/cortex/issues/303
[297]: https://github.com/cortexjs/cortex/issues/297

