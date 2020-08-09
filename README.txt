gitforwindows-perl5.32.0core-missing


This is a collection of missing perl core modules from git for windows 64bit bundled perl(I extracted these files from git for windows sdk), make and cpanm.

So you can install pure perl modules with cpanm or cpan with this.
Check your perl version with "perl -v" command in your git bash prompt.
If your perl version is 5.32.0, this will work.

If you want fully perfect build enviroment with compiler, consider strawberry perl or git for windows sdk( https://github.com/git-for-windows/build-extra ).


SYNOPSIS

Clone this repo.

$ tar zxvf perl5missing.tar.gz -C ~


Make .bash_profile file at home directory.

$ cat << "EOF" > ~/.bash_profile
export PATH=~/perl5missing/bin:$PATH
export PERL5LIB=~/perl5missing
EOF


Restart git bash again.

Install local::lib module

$ cd ~
$ cpanm -L perl5 -v -n local::lib


Add local::lib config. to .bash_profile

$ echo 'eval "$(perl -I$HOME/perl5/lib/perl5 -Mlocal::lib)"' >>~/.bash_profile


Restart git bash

Install Mojolicious or other modules with cpanm

$ cpanm -v -n Mojolicious


Check if Mojolicious works.

$ perl -e 'use Mojolicious'
