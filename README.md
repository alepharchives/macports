# jvalduvieco macports

This is my development repository for my local macports.

## Erlang

* Added parallel build as R15B01 supports it.
* Added a variant called wxgtk to use wxwidgets on Mountain Lion. This way I can use Observer and other goods. wxwidgets 2.8 do not play nice with mountain lion.

## wxgtk-opengl

* Exported this variant of wxgtk as macports does not support variant dependency as far as I know.
* Enabled 64bits support.

## ccze

* ccze is a log colorizer written in C. Depends on ncurses and pcre.
* Created my macport of this tool.



# Using my macports repo
To use my macports repo you must create a local macports repo as follows:

1. Clone this repository: `git clone https://github.com/Jvalduvieco/macports.git`
2. cd into cloned dir
3. run `portindex`
4. run `(echo "file:/$PWD [nosync]" && cat /opt/local/etc/macports/sources.conf) > sources.conf && sudo mv sources.conf /opt/local/etc/macports/sources.conf`.  This weird line is to assure that my repo has priority over official repos, this way I can override some packages.
5. run `port sync`. Add`-v` if you wanna check.
 
 Remember to run `portindex`afer every pull.
 
 More info can be found at [Official documentation](http://guide.macports.org/#development.local-repositories).	
