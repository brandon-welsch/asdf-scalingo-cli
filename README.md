<div align="center">

# asdf-scalingo-cli [![Build](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/build.yml/badge.svg)](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/build.yml) [![Lint](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/lint.yml/badge.svg)](https://github.com/brandon-welsch/asdf-scalingo-cli/actions/workflows/lint.yml)

**[scalingo-cli](https://doc.scalingo.com/platform/cli/start) plugin for the [asdf version manager](https://asdf-vm.com).**

</div>

> This asdf plugin also work nicely with [**rtx**](https://github.com/jdxcode/rtx) which is a fork of
asdf in Rust, with better performance and more features.
> **I recommend using `rtx` instead of `asdf` for a better usage experience** (see https://github.com/asdf-vm/asdf/issues/290).

# Contents

- [Dependencies](#dependencies)
- [Install](#install)
- [Contributing](#contributing)
- [License](#license)

# Dependencies

- `bash`, `curl`, `tar`: generic POSIX utilities.

# Install

Plugin:

```shell
asdf plugin add scalingo-cli
# or
asdf plugin add scalingo-cli https://github.com/brandon-welsch/asdf-scalingo-cli.git
```

scalingo-cli:

```shell
# Show all installable versions
asdf list-all scalingo-cli

# Install specific version
asdf install scalingo-cli 1.29.1

# Install latest version
asdf install scalingo-cli latest

# Set a version globally (on your ~/.tool-versions file)
asdf global scalingo-cli v1.29.1

# Set always latest as a global version
asdf global scalingo-cli latest

# Now scalingo-cli commands are available
scalingo --help
```

Check [asdf](https://github.com/asdf-vm/asdf) readme for more instructions on how to
install & manage versions.

# Usage

## Architecture Override

The `ASDF_SCALINGO_CLI_OVERWRITE_ARCH` variable can be used to override the architecture that is
used for determining which Scalingo CLI release download. Useful, for example, for allowing users
on M1 Macs to install amd64 binary when there's no arm64 binary available when using old Scalingo
CLI versions.

# Contributing

Contributions of any kind welcome! See the [contributing guide](contributing.md).

[Thanks goes to these contributors](https://github.com/brandon-welsch/asdf-scalingo-cli/graphs/contributors)!

# License

See [LICENSE](LICENSE) © [Brandon WELSCH](https://github.com/brandon-welsch/)
