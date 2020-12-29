DOSBox games sometimes need different configuration files, including
different keyboard mappings, to run well.  This repository contains a
wrapper script, `dosbox-wrapper`, to launch DOSBox with a particular
config file, mapper file, and executable, all described in a single JSON
file.

The repostiory also contains a handful of JSON files in the `examples/`
directory to make a few classics from the 80s and 90s run on a
RetroPie-based arcade cabinet with an [Ultimarc
I-PAC2](https://www.ultimarc.com/control-interfaces/i-pacs/i-pac2/).  My
default DOSBox mapping has `"p1b4": "enter"` and `"p1b8": "esc"`, so
`enter` and `esc` are normally not mapped in the per-game config files.

`dosbox-wrapper` is spiritually similer to [Boxer](http://boxerapp.com/)
on macOS, but much more Linux-y.

To run a game with a given JSON config file, just run:
```sh
./dosbox-wrapper something.json
```

Note that the JSON files in `examples/` have comments.  JSON files
_should_ allow comments.

Requirements:
 - Ruby
