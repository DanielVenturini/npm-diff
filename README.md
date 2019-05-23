
# npm-diff(2)

  Diff two versions of a node module.

  ![screenshot](https://www.dropbox.com/s/ek1yp7jk1slkokd/screen1.png?dl=1)

## Installation

```bash
$ make install
```

## Usage

```bash
$ npm-diff
Usage: npm-diff <module> <versionA> <versionB>
```

  __npm-diff(1)__ outputs regular __diff(1)__ content so it plays nice with other tooling.

  Also works for range versions, where the last version accepted by the range will be used:

```bash
$ npm-diff intersect 0 1.0.1 | less
```

  ![screenshot](https://www.dropbox.com/s/ymolkhmwlvblnip/screen2.png?dl=1)

## Tips

  Page big diffs:

```bash
$ npm-diff intersect 0.0.0 0.1.0 | less
``` 

  Pipe to [colordiff](http://www.colordiff.org) for colored git like diffs:

```bash
$ npm-diff intersect 0.0.0 0.1.0 | colordiff | less -R
```

If you don't have [colordiff](http://www.colordiff.org), and want to use it (on the Linux, use sudo; in the Mac, don't use):

```bash
$ make colordiff
```

## License

  MIT

