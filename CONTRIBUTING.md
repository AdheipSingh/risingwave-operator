# Contribution and Development Guidelines

Thanks for your interest in contributing to this project! We welcome and appreciate contributions.

If you have questions, please [create a Github issue](https://github.com/singularity-data/risingwave-operator/issues/new) or ask in the RisingWave Community channel on Slack. Please use the [invitation link](https://join.slack.com/t/risingwave-community/shared_invite/zt-120rft0mr-d8uGk3d~NZiZAQWPnElOfw) to join the channel.

## Setting Up Development Environment

### Go
RisingWave Operator is written in [Go](https://golang.org). If you don't have a Go development environment, [set one up](https://golang.org/doc/code.html).

The version of Go should be 1.16 or later.

After Go is installed, you need to define `GOPATH` and modify `PATH` to access your Go binaries. You can configure them as follows.

```shell
$ export GOPATH=$HOME/go
$ export PATH=$PATH:$GOPATH/bin
```

### PostgreSQL

RisingWave is compatible with `PostgreSQL` (`psql`). To connect to the RisingWave server, you need to install `psql`.

The version of `psql` should be 14.1 or later.

To install it in macOS, run:

```shell
brew install postgresql
```

To install it in Debian-based Linux systems, run:

```shell
sudo apt install postgresql-client
```

## Submit a PR

### Pull Request Title

As described in [here](https://github.com/commitizen/conventional-commit-types/blob/master/index.json), a valid PR title should begin with one of the following prefixes:

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
- `ci`: Changes to RisingWave CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)
- `chore`: Other changes that don't modify src or test files
- `revert`: Reverts a previous commit

For example, a PR title could be:

- `refactor: modify executor protobuf package path`
- `feat(execution): enable comparison between nullable data arrays`, where `(execution)` means that this PR mainly focuses on the execution component.

You may also check out previous PRs in the [PR list](https://github.com/singularity-data/risingwave-operator/pulls).

### Pull Request Description

- If your PR is small (such as a typo fix), you can go brief.
- If it is large and you have changed a lot, it's better to write more details.
