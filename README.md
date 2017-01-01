# Termex

## Requirements

- Git (only for installation and update)
- Bash
- Python 2+

## How to install

``` bash
curl -o- https://raw.githubusercontent.com/stefanwimmer128/termex/master/install | bash
# or
wget -qO- https://raw.githubusercontent.com/stefanwimmer128/termex/master/install | bash
```

## How to update

``` bash
"$TERMEX_DIR/update"
```

## How to use

### Using Termex CLI

``` bash
termex
```

This opens a command line that accepts any commands Termex includes.

### Running script from file

Either add a shebang line on the top of your script:

``` bash
#!/usr/bin/env termex
```

or run script in commandline

``` bash
termex /path/to/script
```

### Running code vom /dev/stdin

``` bash
termex << eof
echo \$TERMEX
eof
```

This prints out the installed version.

### Access the filename of the script

Since the script is running as a subprocess the `$0` variable is the termex command.

To access the script file use the `${argv[0]}` environment variable.

### Additional configuration

Use the .termexrc file in the Termex installation directory like the .bashrc file.
