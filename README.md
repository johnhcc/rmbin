# rmbin

### About rmbin

_rmbin_ is a simple command line trash bin that provides an alternative to rm when you're not really sure you want to _rm_.

_rmbin_ sends files and/or directories to a trash bin (a directory whose name is the current date, YYYY-MM-DD, unless otherwise specified) within a customizable trash directory.

_rmbin_ keeps your trashed files and directories organized, and prevents them from clobbering each other.

### Examples

Let's trash junk.txt and then see where it went:
```
> rmbin junk.txt
junk.txt --> /Users/abc/.rmbin/2015-02-04/WB40P8AIJX_junk.txt 
```

The file has been moved to a bin named `2015-02-04` (the current date in this example), and its name has been prepended by some random characters so that multiple versions of the file can happily coexist in the same bin. Want the file back? Just mv it elsewhere.

If you would like to use a custom-named bin instead of the default:
```
> rmbin --bin proposals important.doc
```

You can view all rmbin'd items (and determine if they are a 'F'ile or 'D'irectory) with:
```
> rmbin -l
D /Users/abc/.rmbin/2015-02-03/CIJ587R82A_my_directory
F /Users/abc/.rmbin/2015-02-04/WB40P8AIJX_junk.txt
F /Users/abc/.rmbin/proposals/QM5ELRL4VC_important.doc
```

When you're sure you don't need the items in a bin anymore, empty it out:
```
rmbin --empty-bin proposals
```

For more options use `rmbin --help`.

### Installation

Either clone this repository with
```
git clone https://github.com/johnhcc/rmbin.git
```
or [download](https://github.com/johnhcc/rmbin/releases) a zip or tarball and extract the contents.

Then simply place the `rmbin` file somewhere in your path.

Requires Perl. Run it by simply typing `rmbin` (or `perl rmbin` if you prefer).

Run without any arguments for usage.

### Contact information

John M. Haynes<br/>
Website: https://github.com/johnhcc<br/>
Email: johnhcc@vorticity.cc
