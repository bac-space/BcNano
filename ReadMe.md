## Description

This project contains a file that provides the rules to inable syntax highlighting in the text editor [Gnu Nano](https://www.nano-editor.org/).
The syntax highlighting is for files written for the command line calculator called [Gnu bc](https://www.gnu.org/software/bc/).

## Installation

Copy the *bc.nanorc* file to the `/usr/share/nano` directory. Performing this action may require elevated user rights which can be done using sudo.


```Shell
$ sudo cp /where-it-was-downloaded/bc.nanorc /usr/share/nano
```

To turn on the syntax highlighting feature of Gnu nano add an include line in the `.nanorc` file in your home directory. If you do not have a `.nanorc` file, you 
can obtain the one from `/etc/nanorc` by copying the file to your home directory.


```Shell
$ cp /etc/nanorc ~/.nanorc
```

Or you can create an empty file in your home dirctory by using the `touch` command.

```Shell
$ touch .nanorc
```

Once the `.nanorc` file is created or already exist, open the file up in a text editor and add an include line.  If you went the copying route, there will be an 
area near the end with an include line commented out.  Uncommenting this line will enable all syntax highlighting files.  Or you can create a new include line 
that will only enable one syntax highlighting file.

```
## To include all existing syntax definitions, you can do:
include "/usr/share/nano/*.nanorc"
```

Or:

```
## To include only one file of syntax definitions, you can do:
include "/usr/share/nano/bc.nanorc"
```

The next time a Gnu bc file is opened with the Gnu nano editor, the syntax should be highlighted.

## License
[LGPL 3.0](lgpl-3.0.txt)
