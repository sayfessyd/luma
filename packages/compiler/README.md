# Luma compiler

This package is used to compile Luma's template string into a virtual dom tree. You may need it separately if you are writing other tools that use Luma's template language.

## Installation

``` bash
npm install @lumajs/compiler
```

``` js
import { compile } from '@lumajs/compiler'
```

## API

### compile(template)

Compiles a template string and returns a virtual dom tree. The returned result is an object of the following format:

``` js
{
  type: string | Function; // The string of the DOM node to create or Component constructor to render
  children: Array<VirtualDomTree | string> | null;
  attributes: any;
  key: Key;
}
```
