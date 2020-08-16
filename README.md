## C compiler

This repository is almost all copy of [rui314/chibicc](https://github.com/rui314/chibicc)

### How to use

9cc only works on Linux.

```
$ cd master
$ make 9cc-gen2
$ ./9cc-gen2 examples/nqueen.c > tmp.s
$ gcc -static -o tmp tmp.s
$ ./tmp
```

### Reference

1. [低レイヤを知りたい人のための C コンパイラ作成入門](https://www.sigbus.info/compilerbook)
2. [rui314/chibicc](https://github.com/rui314/chibicc)

MIT License

Copyright (c) 2019 Rui Ueyama

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
