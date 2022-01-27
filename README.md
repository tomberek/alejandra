<h1 align="center">Alejandra 💅</h2>

<p align="center">The Uncompromising Nix Code Formatter</p>

<p align="center">
  <a
    href="https://coveralls.io/github/kamadorueda/alejandra?branch=main"
  >
    <img
      alt="Coverage"
      src="https://coveralls.io/repos/github/kamadorueda/alejandra/badge.svg?branch=main"
    >
    </img>
  </a>
  <a
    href="https://github.com/kamadorueda/alejandra/blob/main/UNLICENSE"
  >
    <img
      alt="License: The Unlicense"
      src="https://img.shields.io/badge/license-The Unlicense-green.svg"
    >
  </a>
  <a
    href="https://github.com/kamadorueda/alejandra"
  >
    <img
      alt="style: Alejandra"
      src="https://img.shields.io/badge/code%20style-Alejandra-green.svg"
    >
  </a>
</p>

## Features

- ✔️ **Fast**

  It's written in [Rust](https://www.rust-lang.org/)
  and formats [Nixpkgs](https://github.com/NixOS/nixpkgs)
  in just a few seconds[^benchmark-specs].

  | Cores | Seconds |
  |:-----:|:--------:
  | 1     | 40      |
  | 2     | 21      |
  | 4     | 15      |
  | 8     | 11      |
  | 16    | 10      |

- ✔️ **Powerful**

  All elements in the Nix grammar have a totally defined style.

- ✔️ **Reliable**

  Coverage is currently 80%,
  and we'll have 💯% soon.

- ✔️ **Developer aware**

  Syntax errors are gracefully handled
  by leaving that specific zone unformatted.

  The rest of the file will be formatted normally.

- ✔️ **Reproducible**

  Formatting many times yields the same results.

- 🚧 **Beautiful**

  Beauty is subjective, right?

  Yet there are a few improvements to implement like:
  - Multiline strings indentation is missing `'' ... ''`.

  Style is negotiable at this moment.

## Getting started

Let's get Alejandra on our systems:

- Nix with Flakes:

  ```bash
  $ nix run github:kamadorueda/alejandra -- --help
  ```

- Nix stable:

  Pick one depending on your platform:
  ```bash
  $ nix-env -ivA aarch64-darwin -f https://github.com/kamadorueda/alejandra/tarball/main
  $ nix-env -ivA aarch64-linux -f https://github.com/kamadorueda/alejandra/tarball/main
  $ nix-env -ivA i686-linux -f https://github.com/kamadorueda/alejandra/tarball/main
  $ nix-env -ivA x86_64-darwin -f https://github.com/kamadorueda/alejandra/tarball/main
  $ nix-env -ivA x86_64-linux -f https://github.com/kamadorueda/alejandra/tarball/main
  ```

  Then run with:

  ```bash
  $ alejandra --help
  ```

## Do I need to configure anything?

- No.

## Discussion

- [RFC 0101 - Nix formatting](https://github.com/NixOS/rfcs/pull/101)

## Cool libraries

- [rnix-parser](https://github.com/nix-community/rnix-parser)

## Alternatives

- [nixpkgs-fmt](https://github.com/nix-community/nixpkgs-fmt)
- [nixfmt](https://github.com/serokell/nixfmt)

## Footnotes

[^benchmark-specs]:

    Running on a [machine](https://github.com/kamadorueda/machine) with:

    - CPU: 16 x Intel(R) Core(TM) i7-10700K
    - MHz: 3800.00
    - BogoMips: 7599.80
    - Cache Size: 16384 KB
