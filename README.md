# iSight Command-Line Disabler

Enable and disable a Mac's built-in iSight camera via the command line.

## Demo

![Disabling the iSight](https://raw.github.com/jessedoyle/isight-cli/master/isight_demo.gif)

## Installation

A simple install script is included in this repository. _This script will overwrite any file located at `/usr/local/bin/isight`_.

```bash
\curl -sSL https://raw.github.com/jessedoyle/isight-cli/master/installer.sh | bash
```

Alternatively, take the `isight` script from this repository and put it wherever you like!

## Usage

###### OS X <= 10.10

You must run the `isight` commands below with `sudo` privileges.

###### MacOS >= 10.11 (System Integrity Protection enabled)

There is no need for `sudo` privileges to enable/disable the camera because a different strategy (system profiles) is used.

Disable:

```bash
isight off
```

Enable:

```bash
isight on
```

Running the `isight` command without any arguments will display the camera's current status.

View a simple help page using:

```bash
isight help
```

## Caveats

The script simply restricts system access to the files that are required by the iSight drivers. Anyone with root access can re-enable the camera.

If the Disk Utility repair permissions tool is ran when the camera is disabled, the process will re-enable the camera.

## Contributing

Feel free to fork this repository, make your changes and generate a pull request!

## Acknowledgements

This script is based off of the work completed by [http://techslaves.org](http://techslaves.org) on their great AppleScript "iSight Disabler".

Please visit: [http://techslaves.org/isight-disabler/](http://techslaves.org/isight-disabler/) to see the original AppleScript implementation.

## License

iSight CLI Disabler is licensed under the MIT license. Please see LICENSE for details.
