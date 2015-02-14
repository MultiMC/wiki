## Requirements

### Xcode

Go [here](https://developer.apple.com/) -> Xcode -> Other downloads, find the one that contains _Snow Leopard_ in the name.

### Git

Download zip from github, unzip, `make NO_GETTEXT=YesPlease` and then `sudo make install NO_GETTEXT=YesPlease`

### Clang

The clang/gcc included in xcode are to old, install it from http://llvm.org/releases/download.html (3.1 works). Symlink everything into the correct positions.

### Qt

Build from source (google for instructions). Change `10.7` to `10.6` in `qtbase/mkspecs/macx-clang/qmake.conf`. Configure arguments: `-opensource -confirm-license -no-cups -no-dbus -nomake examples -no-sql-odbc -no-sql-sqlite -platform macx-clang`

### CMake

Install using installer

## Paths for @02JanDal's MacMini

/User/kalle/libexec/git-core/git
/Applications/CMake.app/Contents/bin/cmake