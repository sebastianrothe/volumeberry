oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g volumeberry
$ volumeberry COMMAND
running command...
$ volumeberry (--version)
volumeberry/0.0.0 darwin-arm64 node-v21.2.0
$ volumeberry --help [COMMAND]
USAGE
  $ volumeberry COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`volumeberry hello PERSON`](#volumeberry-hello-person)
* [`volumeberry hello world`](#volumeberry-hello-world)
* [`volumeberry help [COMMANDS]`](#volumeberry-help-commands)
* [`volumeberry plugins`](#volumeberry-plugins)
* [`volumeberry plugins:install PLUGIN...`](#volumeberry-pluginsinstall-plugin)
* [`volumeberry plugins:inspect PLUGIN...`](#volumeberry-pluginsinspect-plugin)
* [`volumeberry plugins:install PLUGIN...`](#volumeberry-pluginsinstall-plugin-1)
* [`volumeberry plugins:link PLUGIN`](#volumeberry-pluginslink-plugin)
* [`volumeberry plugins:uninstall PLUGIN...`](#volumeberry-pluginsuninstall-plugin)
* [`volumeberry plugins reset`](#volumeberry-plugins-reset)
* [`volumeberry plugins:uninstall PLUGIN...`](#volumeberry-pluginsuninstall-plugin-1)
* [`volumeberry plugins:uninstall PLUGIN...`](#volumeberry-pluginsuninstall-plugin-2)
* [`volumeberry plugins update`](#volumeberry-plugins-update)

## `volumeberry hello PERSON`

Say hello

```
USAGE
  $ volumeberry hello PERSON -f <value>

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

_See code: [src/commands/hello/index.ts](https://github.com/sebastianrothe/volumeberry/blob/v0.0.0/src/commands/hello/index.ts)_

## `volumeberry hello world`

Say hello world

```
USAGE
  $ volumeberry hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ volumeberry hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/sebastianrothe/volumeberry/blob/v0.0.0/src/commands/hello/world.ts)_

## `volumeberry help [COMMANDS]`

Display help for volumeberry.

```
USAGE
  $ volumeberry help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for volumeberry.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.20/src/commands/help.ts)_

## `volumeberry plugins`

List installed plugins.

```
USAGE
  $ volumeberry plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ volumeberry plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/index.ts)_

## `volumeberry plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ volumeberry plugins add plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ volumeberry plugins add

EXAMPLES
  $ volumeberry plugins add myplugin 

  $ volumeberry plugins add https://github.com/someuser/someplugin

  $ volumeberry plugins add someuser/someplugin
```

## `volumeberry plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ volumeberry plugins inspect PLUGIN...

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
  $ volumeberry plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/inspect.ts)_

## `volumeberry plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ volumeberry plugins install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ volumeberry plugins add

EXAMPLES
  $ volumeberry plugins install myplugin 

  $ volumeberry plugins install https://github.com/someuser/someplugin

  $ volumeberry plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/install.ts)_

## `volumeberry plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ volumeberry plugins link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ volumeberry plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/link.ts)_

## `volumeberry plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ volumeberry plugins remove plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ volumeberry plugins unlink
  $ volumeberry plugins remove

EXAMPLES
  $ volumeberry plugins remove myplugin
```

## `volumeberry plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ volumeberry plugins reset
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/reset.ts)_

## `volumeberry plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ volumeberry plugins uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ volumeberry plugins unlink
  $ volumeberry plugins remove

EXAMPLES
  $ volumeberry plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/uninstall.ts)_

## `volumeberry plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ volumeberry plugins unlink plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ volumeberry plugins unlink
  $ volumeberry plugins remove

EXAMPLES
  $ volumeberry plugins unlink myplugin
```

## `volumeberry plugins update`

Update installed plugins.

```
USAGE
  $ volumeberry plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.1.8/src/commands/plugins/update.ts)_
<!-- commandsstop -->
