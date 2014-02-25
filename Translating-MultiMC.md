# How to translate

If you have any questions feel free to hop on IRC (#MultiMC on esper.net)

## Using Git

1. Create a fork of MultiMC (button on the top right)
2. Clone
3. Go into translations/ and copy one of the mmc_*.ts (take the one that's closest to the target language) and name it mmc_<language>.ts, where language is a two letter lowercase code for the language ([ISO 639-1](http://www.loc.gov/standards/iso639-2/php/English_list.php))
4. Download Qt Linguist (http://qt-project.org/downloads, sadly you'll have to download the entire Qt SDK)
5. Open the created .ts file with Qt Linguist and start translating ([manual for Qt Linguist](http://qt-project.org/doc/qt-5/linguist-translators.html))
6. Once you are done, create a branch named feature_<language>_translation (use the full english name of the language this time), add and commit the newly created .ts file and push to that branch.
7. Go to Github and create a pull request

## Without Git

1. Download one of the ts files from [here](https://github.com/MultiMC/MultiMC5/tree/develop/translations) (take the one that's closest to the target language)
2. Download Qt Linguist (http://qt-project.org/downloads, sadly you'll have to download the entire Qt SDK)
3. Open the created .ts file with Qt Linguist and start translating ([manual for Qt Linguist](http://qt-project.org/doc/qt-5/linguist-translators.html))
4. Once you are done, upload the .ts to somewhere ([paste.ee](http://paste.ee) or [pastebin.com](http://pastebin.com) for example) and open a new issue on github with a link to the .ts file