# zs-extract

Zippyshare download data extractor

[![npm](https://img.shields.io/npm/v/zs-extract.svg)](https://npmjs.com/package/zs-extract)
[![node](https://img.shields.io/node/v/zs-extract.svg)](https://nodejs.org)

[![size](https://packagephobia.now.sh/badge?p=zs-extract)](https://packagephobia.now.sh/result?p=zs-extract)
[![downloads](https://img.shields.io/npm/dm/zs-extract.svg)](https://npmcharts.com/compare/zs-extract?minimal=true)

[![Build Status](https://github.com/JrMasterModelBuilder/zs-extract/workflows/main/badge.svg?branch=master)](https://github.com/JrMasterModelBuilder/zs-extract/actions?query=workflow%3Amain+branch%3Amaster)

# Overview

This module simplifies extracting download info from a Zippyshare link. Instead of parsing their ever-changing JavaScript for the variables to compute the download URL, this module uses Node's VM functionality to safely emulate a browser in a sandboxed environment, making it much more resilient to changes in the obfuscated download link generation code.

# Usage

```js
Esm
import {extract} from 'zs-extract';

console.log(await extract('https://www83.zippyshare.com/v/yakMuCxe/file.html'));

Cjs
let zsExtract = require ('zs-extract')

let res = await zsExtract.extract(link)

```

```
{
  download: 'https://www83.zippyshare.com/d/yakMuCxe/12345/jmmb%20avatar.png',
  filename: 'jmmb avatar.png'
}
```

# Bugs

If you find a bug or have compatibility issues, please open a ticket under issues section for this repository.

# License

Copyright (c) 2019-2021 JrMasterModelBuilder

Licensed under the Mozilla Public License, v. 2.0.

If this license does not work for you, feel free to contact me.
