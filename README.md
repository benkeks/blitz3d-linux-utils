# Using Blitz3d on Linux

This is a small collection of stuff for using Blitz3d with Wine on Linux.

## Blitz3d Syntax Highlighting for Kate

 * Copy `blitzbasic.xml` to `~.kde/share/apps/katepart/syntax/`.
 * Restart Kate.

## Make Blitz3d Compiler usable from terminal

 * Install `wine`.
 * Put your `Blitz3d` directory into `~/.wine/drive_c/Program Files/` (or create a link).
   * If you have not got a Blitz3d installation: You can download the executables for free from <http://blitzbasic.com>.
 * Set `blitzcc.sh` to be executable.
 
You can now use `blitzcc.sh` to access the Blitz3d-Compiler from the linux terminal.
 
    $ ./blitzcc -h
      Usage: blitzcc [-h|-q|+q|-c|-d|-k|+k|-v|-o exefile] [sourcefile.bb]
      -h         : show this help
      -q         : quiet mode
      +q                : very quiet mode
      -c         : compile only
      -d         : debug compile
      -k         : dump keywords
      +k         : dump keywords and syntax
      -v                : version info
      -o exefile : generate executable

In order to run `blitzcc` like a command, you can add an alias to your `.bashrc`:
 
 * Copy `blitzcc.sh` into the same directory `~/.wine/drive_c/Program Files/Blitz3d/`.
 * Extend `~/.bashrc` by `alias blitzcc='~/.wine/drive_c/Program Files/Blitz3d/launchBlitz.sh'`.
 * Open new terminal window.
