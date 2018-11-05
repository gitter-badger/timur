# timur: Finite-state morphology for German

This package is basically a migration of a set of finite-state grammars for the morphological analysis of German words delivered with [`SFST`](http://www.cis.uni-muenchen.de/~schmid/tools/SFST/), a finite-state transducer (FST) toolkit by [Helmut Schmid](http://www.cis.uni-muenchen.de/~schmid/), to [`Pynini`](http://www.opengrm.org/twiki/bin/view/GRM/Pynini), another FST toolkit. The latter has the advantage that it is implemented as a python library allowing for seamless interaction with tons of other useful python packages.

## Installation

`timur` is implemented in Python 3. In the following, we assume a working Python 3 (tested versions 3.5 and 3.6) installation as well as a working C++ compiler supporting C++-11.

### OpenFST

The underlying FST toolkit `Pynini` is itself based on [`OpenFST`](http://www.openfst.org/twiki/bin/view/FST/WebHome) a C++ library for constructing, combining, optimizing, and searching weighted FSTs. [Get] (http://www.openfst.org/twiki/bin/view/FST/FstDownload) the latest version of OpenFST, unpack the archive, build and install via
```shell
$ configure --enable-grm
$ make
$ [sudo] make install && [sudo ldconfig]
```

### virtualenv
Using [`virtualenv`](https://virtualenv.pypa.io/en/stable/) is highly recommended, although not strictly necessary for installing `timur`. It may be installed via:

```console
$ [sudo] pip install virtualenv
```

Create a virtual environement in a subdirectory of your choice (e.g. `env`) using

```console
$ virtualenv -p python3 env
```

and activate it.

```console
$ . env/bin/activate
```

### Python requirements
`timur` uses various 3rd party Python packages (including `Pynini`) which may be best installed using `pip`:

```console
(env) $ pip install -r requirements.txt
```
