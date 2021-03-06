---
title: Changelog
layout: default
section: main
---

### Next release

### v3.1.8 2019-01-09
- Working release of 3.1.7, forgot the dist files in previous release.

### v3.1.7 2019-01-09
- Replaced usage of deprecated Buffer constructor (see: [#506](https://github.com/Stuk/jszip/pull/506))

### v3.1.6 2019-01-09
- Initial release of jszip2, no changes from v3.1.5

### v3.1.5 2017-11-09
- Fix IE11 memory leak (see [#429](https://github.com/Stuk/jszip/pull/429)).
- Handle 2 nodejs deprecations (see [#459](https://github.com/Stuk/jszip/pull/459)).
- Improve the "unsupported format" error message (see [#461](https://github.com/Stuk/jszip/pull/461)).
- Improve webworker compatibility (see [#468](https://github.com/Stuk/jszip/pull/468)).
- Fix nodejs 0.10 compatibility (see [#480](https://github.com/Stuk/jszip/pull/480)).
- Improve the error without type in async() (see [#481](https://github.com/Stuk/jszip/pull/481)).

### v3.1.4 2017-08-24
- consistently use our own utils object for inheritance (see [#395](https://github.com/Stuk/jszip/pull/395)).
- lower the memory consumption in `generate*` with a lot of files (see [#449](https://github.com/Stuk/jszip/pull/449)).

### v3.1.3 2016-10-06
- instanceof failing in window / iframe contexts (see [#350](https://github.com/Stuk/jszip/pull/350)).
- remove a copy with blob output (see [#357](https://github.com/Stuk/jszip/pull/357)).
- fix crc32 check for empty entries (see [#358](https://github.com/Stuk/jszip/pull/358)).
- fix the base64 error message with data uri (see [#359](https://github.com/Stuk/jszip/pull/359)).

### v3.1.2 2016-08-23
- fix support of nodejs `process.platform` in `generate*` methods (see [#335](https://github.com/Stuk/jszip/pull/335)).
- improve browserify/webpack support (see [#333](https://github.com/Stuk/jszip/pull/333)).
- partial support of a promise of text (see [#337](https://github.com/Stuk/jszip/pull/337)).
- fix streamed zip files containing folders (see [#342](https://github.com/Stuk/jszip/pull/342)).

### v3.1.1 2016-08-08
- Use a hard-coded JSZip.version, fix an issue with webpack (see [#328](https://github.com/Stuk/jszip/pull/328)).

### v3.1.0 2016-08-03
- utils.delay: use macro tasks instead of micro tasks (see [#288](https://github.com/Stuk/jszip/pull/288)).
- Harden base64 decode (see [#316](https://github.com/Stuk/jszip/pull/316)).
- Add JSZip.version and the version in the header (see [#317](https://github.com/Stuk/jszip/pull/317)).
- Support Promise(Blob) (see [#318](https://github.com/Stuk/jszip/pull/318)).
- Change JSZip.external.Promise implementation (see [#321](https://github.com/Stuk/jszip/pull/321)).
- Update pako to v1.0.2 to fix a DEFLATE bug (see [#322](https://github.com/Stuk/jszip/pull/322)).

### v3.0.0 2016-04-13
This release changes a lot of methods, please see [the upgrade guide](http://stuk.github.io/jszip/documentation/upgrade_guide.html).

- replace sync getters and `generate()` with async methods (see [#195](https://github.com/Stuk/jszip/pull/195)).
- support nodejs streams (in `file()` and `generateAsync()`).
- support Blob and Promise in `file()` and `loadAsync()` (see [#275](https://github.com/Stuk/jszip/pull/275)).
- add `support.nodestream`.
- zip.filter: remove the defensive copy.
- remove the deprecated API (see [#253](https://github.com/Stuk/jszip/pull/253)).
- `type` is now mandatory in `generateAsync()`.
- change the createFolders default value (now `true`).
- Dates: use UTC instead of the local timezone.
- Add `base64` and `array` as possible output type.
- Add a forEach method.
- Drop node 0.8 support (see [#270](https://github.com/Stuk/jszip/pull/270)).

### v2.6.1 2016-07-28
- update pako to v1.0.2 to fix a DEFLATE bug (see [#322](https://github.com/Stuk/jszip/pull/322)).

### v2.6.0 2016-03-23
- publish `dist/` files in the npm package (see [#225](https://github.com/Stuk/jszip/pull/225)).
- update pako to v1.0.0 (see [#261](https://github.com/Stuk/jszip/pull/261)).
- add support of Array in JSZip#load (see [#252](https://github.com/Stuk/jszip/pull/252)).
- improve file name / comment encoding support (see [#211](https://github.com/Stuk/jszip/pull/211)).
- handle prepended data (see [#266](https://github.com/Stuk/jszip/pull/266)).
- improve platform coverage in tests (see [#233](https://github.com/Stuk/jszip/pull/233) and [#269](https://github.com/Stuk/jszip/pull/269)).

### v2.5.0 2015-03-10
- add support for custom mime-types (see [#199](https://github.com/Stuk/jszip/issues/199)).
- add an option to set the DEFLATE level (see [#201](https://github.com/Stuk/jszip/issues/201)).
- improve the error message with corrupted zip (see [#202](https://github.com/Stuk/jszip/issues/202)).
- add support for UNIX / DOS permissions (see [#200](https://github.com/Stuk/jszip/issues/200) and [#205](https://github.com/Stuk/jszip/issues/205)).

### v2.4.0 2014-07-24
- update pako to 0.2.5 (see [#156](https://github.com/Stuk/jszip/issues/156)).
- make JSZip work in a Firefox addon context (see [#151](https://github.com/Stuk/jszip/issues/151)).
- add an option (`createFolders`) to control the subfolder generation (see [#154](https://github.com/Stuk/jszip/issues/154)).
- allow `Buffer` polyfill in the browser (see [#139](https://github.com/Stuk/jszip/issues/139)).

### v2.3.0 2014-06-18
- don't generate subfolders (see [#130](https://github.com/Stuk/jszip/issues/130)).
- add comment support (see [#134](https://github.com/Stuk/jszip/issues/134)).
- on `ZipObject#options`, the attributes `date` and `dir` have been deprecated and are now on `ZipObject` (see [the upgrade guide](http://stuk.github.io/jszip/documentation/upgrade_guide.html)).
- on `ZipObject#options`, the attributes `base64` and `binary` have been deprecated (see [the upgrade guide](http://stuk.github.io/jszip/documentation/upgrade_guide.html)).
- deprecate internal functions exposed in the public API (see [#123](https://github.com/Stuk/jszip/issues/123)).
- improve UTF-8 support (see [#142](https://github.com/Stuk/jszip/issues/142)).

### v2.2.2, 2014-05-01
 - update pako to v0.2.1, fix an error when decompressing some files (see [#126](https://github.com/Stuk/jszip/issues/126)).

### v2.2.1, 2014-04-23
 - fix unreadable generated file on Windows 8 (see [#112](https://github.com/Stuk/jszip/issues/112)).
 - replace zlibjs with pako.

### v2.2.0, 2014-02-25
 - make the `new` operator optional before the `JSZip` constructor (see [#93](https://github.com/Stuk/jszip/pull/93)).
 - update zlibjs to v0.2.0.

### v2.1.1, 2014-02-13
 - use the npm package for zlib.js instead of the github url.

### v2.1.0, 2014-02-06
 - split the files and use Browserify to generate the final file (see [#74](https://github.com/Stuk/jszip/pull/74))
 - packaging change : instead of 4 files (jszip.js, jszip-load.js, jszip-inflate.js, jszip-deflate.js) we now have 2 files : dist/jszip.js and dist/jszip.min.js
 - add component/bower support
 - rename variable: 'byte' is a reserved word (see [#76](https://github.com/Stuk/jszip/pull/76))
 - add support for the unicode path extra field (see [#82](https://github.com/Stuk/jszip/pull/82))
 - ensure that the generated files have a header with the licenses (see [#80](https://github.com/Stuk/jszip/pull/80))

# v2.0.0, 2013-10-20

 - `JSZipBase64` has been renamed to `JSZip.base64`.
 - The `data` attribute on the object returned by `zip.file(name)` has been removed. Use `asText()`, `asBinary()`, `asUint8Array()`, `asArrayBuffer()` or `asNodeBuffer()`.

 - [Fix issue with Android browser](https://github.com/Stuk/jszip/pull/60)

 - The compression/decompression methods now give their input type with the `compressInputType` and `uncompressInputType` attributes.
 - Lazily decompress data when needed and [improve performance in general](https://github.com/Stuk/jszip/pull/56)
 - [Add support for `Buffer` in Node.js](https://github.com/Stuk/jszip/pull/57).
 - Package for CommonJS/npm.

### v1.0.1, 2013-03-04

 - Fixed an issue when generating a compressed zip file with empty files or folders, see #33.
 - With bad data (null or undefined), asText/asBinary/asUint8Array/asArrayBuffer methods now return an empty string, see #36.

# v1.0.0, 2013-02-14

- First release after a long period without version.

