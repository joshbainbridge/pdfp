# PDFP

This project PDFP (Portable Document File Passer) aims to provide a CLI tool to pass PDF files, either from local disk or a web address, and output the text to stdout.

ADD GIF HERE.

It can be combined with AI / LLM tools like [AiBro](https://github.com/joshbainbridge/aibro) or [Mods](https://github.com/charmbracelet/mods) to evaluate and understand PDF documents. Just pipe the result on the command line from one tool to the other.

## Installation

Either set up a rust toolchain manually, or if you are using macOS and have Nix installed, use the provided Nix flake to create a development environment:

```bash
nix develop
```

Installation of the CLI command can then be done using cargo:

```bash
cargo install --path .
```

## Usage

```
Usage: pdfp [OPTIONS] <INPUT>

Arguments:
  <INPUT>
          Input source

Options:
  -m, --method <METHOD>
          Selected input method

          [default: file]

          Possible values:
          - file: Input from file on disk
          - web:  Download input from web address

  -l, --limit <LIMIT>
          Set byte limit on output

          [default: 100000]

  -i, --ignore-limit
          Ignore byte limit

  -h, --help
          Print help (see a summary with '-h')

  -V, --version
          Print version
```
