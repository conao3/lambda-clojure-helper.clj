# lambda-clojure-helper

A Leiningen plugin for deploying Clojure functions to AWS Lambda.

## Deprecation Notice

This project is deprecated. The functionality provided here overlaps significantly with [lein-lambda](https://github.com/paulbutcher/lein-lambda), which offers a more comprehensive and actively maintained solution for AWS Lambda deployment. Users are encouraged to migrate to that project.

## Overview

lambda-clojure-helper was designed to simplify the deployment workflow for Clojure applications targeting AWS Lambda. It provides a command-line interface through Leiningen for managing Lambda function deployments.

### Features

- Deploy Clojure functions to AWS Lambda
- Configuration-based deployment workflow
- Integration with AWS CLI tooling

## Installation

Add the following dependency to your `project.clj`:

```clojure
:plugins [[com.conao3/lambda-clojure-helper "0.0.2"]]
```

## Usage

```bash
lein lambda <action> [options]
```

### Available Actions

| Action | Description |
|--------|-------------|
| `echo` | System command execution test |
| `show-config` | Display current configuration |
| `dryrun` | Preview deployment without executing |
| `deploy` | Deploy functions to AWS Lambda |

### Options

| Option | Description |
|--------|-------------|
| `-v, --verbose` | Show debug messages |
| `-h, --help` | Display help information |

## Configuration

Create a configuration file at `resources/lambda-clojure-helper-config.edn` to define your deployment settings.

## Requirements

- Leiningen
- AWS CLI configured with appropriate credentials
- Clojure 1.9.0 or later

## License

Copyright 2019 conao3

This program is available under the GNU Affero General Public License version 3 or later. See the [AGPL-3.0 License](https://www.gnu.org/licenses/agpl-3.0.html) for details.
