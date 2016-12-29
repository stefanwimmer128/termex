# Termex

## Requirements

- Git (only for installation and update)
- Bash
- Python 3

## How to install

``` bash
curl -o- https://raw.githubusercontent.com/stefanwimmer128/termex/master/installer | bash
# or
wget -qO- https://raw.githubusercontent.com/stefanwimmer128/termex/master/installer | bash
```

## How to update

``` bash
~/.termex/updater
```

## How to uninstall

``` bash
~/.termex/uninstaller
```

## How to use

### Using Termex CLI

``` bash
termex
```

This opens a command line interface that accepts any commands Termex includes.

### Running code vom /dev/stdin

``` bash
termex << eof
echo \$TERMEX
eof
```

This prints out the installed version.

### Running script from file

Either add a shebang line on the top of your script:

``` bash
#!/usr/bin/env termex
```

or run script in commandline

``` bash
termex /path/to/script
```

### Access the filename of the script

Since the script is running as a subprocess the `$0` variable is the termex command.

To access the script file use the `${argv[0]}` environment variable.
