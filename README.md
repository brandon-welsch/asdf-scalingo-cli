<div align="center">

# asdf-scalingo-cli [![Build](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/build.yml/badge.svg)](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/build.yml) [![Lint](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/lint.yml/badge.svg)](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/lint.yml)

**[scalingo-cli](https://doc.scalingo.com/platform/cli/start) plugin for the [asdf version manager](https://asdf-vm.com).**

</div>

> **Note**
>
> This asdf plugin also work nicely with [**rtx**](https://github.com/jdxcode/rtx) which is a fork of
asdf in Rust, with better performance and more features.
> **I recommend using `rtx` instead of `asdf` for a better usage experience**
(see https://github.com/asdf-vm/asdf/issues/290).

> **Warning**
>
> This is not an official Scalingo repository, but the plugin uses the
[official binaries compiled by Scalingo](https://github.com/Scalingo/cli/releases).

# Contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

# Requirements

- `bash`, `curl`, `tar`: generic POSIX utilities.

# Installation

## With asdf

```shell
asdf plugin add scalingo-cli https://github.com/brandon-welsch/asdf-scalingo-cli.git
```

## With rtx

```shell
rtx plugins install scalingo-cli https://github.com/brandon-welsch/asdf-scalingo-cli
```

# Usage

## With asdf

```shell
# Show all installable versions
asdf list-all scalingo-cli

# Install specific version
asdf install scalingo-cli 1.29.1

# Install latest version
asdf install scalingo-cli latest

# Set a version globally (on your ~/.tool-versions file)
asdf global scalingo-cli 1.29.1

# Set always latest as a global version
asdf global scalingo-cli latest

# Show installed versions
asdf list scalingo-cli

# Now Scalingo CLI commands are available
scalingo --help
```

Check [asdf](https://github.com/asdf-vm/asdf) README for more instructions on how to
install & manage versions.

## With rtx

```bash
# Show all installable versions
rtx list-all scalingo-cli

# Install specific version
rtx install scalingo-cli@1.29.1

# Install latest version
rtx install scalingo-cli@latest

# Set a version globally
rtx use -g scalingo-cli@1.29.1

# Set always latest as a global version
rtx use -g scalingo-cli@latest

# Show installed versions
rtx list scalingo-cli

# Now Scalingo CLI commands are available
scalingo --help
```

Check [rtx](https://github.com/jdxcode/rtx) README for more instructions on how to
install & manage versions.

## Environment Variables

### Architecture Override

The `ASDF_SCALINGO_CLI_OVERWRITE_ARCH` variable can be used to override the architecture that is
used for determining which Scalingo CLI release download. Useful, for example, for allowing users
on M1 Macs to install amd64 binary when there's no arm64 binary available when using old Scalingo
CLI versions.

# Contributing

Contributions of any kind welcome! See the [contributing guide](contributing.md).

[Thanks goes to these contributors](https://github.com/brandon-welsch/asdf-scalingo-cli/graphs/contributors)!

# License

See [LICENSE](LICENSE) © [Brandon WELSCH](https://github.com/brandon-welsch/)
