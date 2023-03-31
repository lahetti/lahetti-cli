oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g lahetti-cli
$ lahetti COMMAND
running command...
$ lahetti (--version)
lahetti-cli/0.0.0 darwin-arm64 node-v18.12.1
$ lahetti --help [COMMAND]
USAGE
  $ lahetti COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`lahetti hello PERSON`](#lahetti-hello-person)
* [`lahetti hello world`](#lahetti-hello-world)
* [`lahetti help [COMMANDS]`](#lahetti-help-commands)
* [`lahetti plugins`](#lahetti-plugins)
* [`lahetti plugins:install PLUGIN...`](#lahetti-pluginsinstall-plugin)
* [`lahetti plugins:inspect PLUGIN...`](#lahetti-pluginsinspect-plugin)
* [`lahetti plugins:install PLUGIN...`](#lahetti-pluginsinstall-plugin-1)
* [`lahetti plugins:link PLUGIN`](#lahetti-pluginslink-plugin)
* [`lahetti plugins:uninstall PLUGIN...`](#lahetti-pluginsuninstall-plugin)
* [`lahetti plugins:uninstall PLUGIN...`](#lahetti-pluginsuninstall-plugin-1)
* [`lahetti plugins:uninstall PLUGIN...`](#lahetti-pluginsuninstall-plugin-2)
* [`lahetti plugins update`](#lahetti-plugins-update)

## `lahetti hello PERSON`

Say hello

```
USAGE
  $ lahetti hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/lahetti/lahetti-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `lahetti hello world`

Say hello world

```
USAGE
  $ lahetti hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ lahetti hello world
  hello world! (./src/commands/hello/world.ts)
```

## `lahetti help [COMMANDS]`

Display help for lahetti.

```
USAGE
  $ lahetti help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for lahetti.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.8/src/commands/help.ts)_

## `lahetti plugins`

List installed plugins.

```
USAGE
  $ lahetti plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ lahetti plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.4.3/src/commands/plugins/index.ts)_

## `lahetti plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ lahetti plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ lahetti plugins add

EXAMPLES
  $ lahetti plugins:install myplugin 

  $ lahetti plugins:install https://github.com/someuser/someplugin

  $ lahetti plugins:install someuser/someplugin
```

## `lahetti plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ lahetti plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ lahetti plugins:inspect myplugin
```

## `lahetti plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ lahetti plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ lahetti plugins add

EXAMPLES
  $ lahetti plugins:install myplugin 

  $ lahetti plugins:install https://github.com/someuser/someplugin

  $ lahetti plugins:install someuser/someplugin
```

## `lahetti plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ lahetti plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ lahetti plugins:link myplugin
```

## `lahetti plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ lahetti plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ lahetti plugins unlink
  $ lahetti plugins remove
```

## `lahetti plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ lahetti plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ lahetti plugins unlink
  $ lahetti plugins remove
```

## `lahetti plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ lahetti plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ lahetti plugins unlink
  $ lahetti plugins remove
```

## `lahetti plugins update`

Update installed plugins.

```
USAGE
  $ lahetti plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
