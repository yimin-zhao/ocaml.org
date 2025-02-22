---
title: "opam 2.0.0 Release Candidate 3 is out!"
authors: [ "Raja Boujbel", "Louis Gesbert"]
date: "2018-06-22"
description: "Release announcement for OPAM 2.0.0~rc3"
tags: [platform]
---

We are pleased to announce the release of a third release candidate for opam 2.0.0. This one is expected to be the last before 2.0.0 comes out.

Changes since the [2.0.0~rc2](../opam-2-0-0-rc2) are, as expected, mostly fixes. We deemed it useful, however, to bring in the following:

- a new command `opam switch link` that allows to select a switch to be used in a given directory (particularly convenient if you use the shell hook for automatic opam environment update)
- a new option `opam install --assume-built`, that allows to install a package using its normal opam procedure, but for a source repository that has been built by hand. This fills a gap that remained in the local development workflows.

The preview of the opam 2 webpages can be browsed at https://opam.ocaml.org/2.0-preview/ (please report issues [here](https://github.com/ocaml/opam2web/issues)).

Installation instructions (unchanged):

1. From binaries: run

    ```
    sh <(curl -sL https://raw.githubusercontent.com/ocaml/opam/master/shell/install.sh)
    ```

    or download manually from [the Github "Releases" page](https://github.com/ocaml/opam/releases/tag/2.0.0-rc3) to your PATH. In this case, don't forget to run `opam init --reinit -ni` to enable sandboxing if you had version 2.0.0~rc manually installed.

2. From source, using opam:

    ```
    opam update; opam install opam-devel
    ```

   (then copy the opam binary to your PATH as explained, and don't forget to run `opam init --reinit -ni` to enable sandboxing if you had version 2.0.0~rc manually installed)

3. From source, manually: see the instructions in the [README](https://github.com/ocaml/opam/tree/2.0.0-rc3#compiling-this-repo).

Thanks a lot for testing out this new RC and [reporting](https://github.com/ocaml/opam/issues) any issues you may find.
