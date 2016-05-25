Supports:

1. Vanilla game
2. Gods & Kings
3. Brave New World
4. Firaxis' Civ DLCs


## Manual installation via ZIP file

Locate your `Sid Meier's Civilization 5` user directory. Possible locations:

- Windows 7, 8, 10: `C:\Users\USERNAME\Documents\My Games\Sid Meier's Civilization 5`
- Windows 7, 8, 10: [Git Bash] `cd ~/Documents/My\ Games/Sid\ Meier's\ Civilization\ 5`
- Mac OS X: `Users/USERNAME/Library/Application Support/Sid Meier's Civilization 5`
- Mac OS X: `cd ~/Library/Application Support/Sid Meier's Civilization 5`

From there you can find `config.ini`. Locate line 66 which should state: `Language = en_US`.
Replace with `Language = fi_FI`.

Next you need to copy `Suomi*.xml` files from this repo to the Text directory within the same path as `config.ini`.

After this the game will boot in Finnish and you can play with other players with no additional DLC or MOD limitations!


## Installation using Git (Git Bash on Windows)

If you do not have Git installed then [go get your copy!](https://git-scm.com/download) (You can use default settings.)

1. Open command line / Git Bash
2. Move to the Civ 5 user directory: `cd ~/Documents/My\ Games/Sid\ Meier\'s\ Civilization\ 5/`
3. Set language to Finnish: `perl -pi -w -e 's/^Language = en_US/Language = fi_FI/;' config.ini`
4. Now we can copy the files. You can do this in two ways: simple copy, or as a fully working Git clone.

To copy only the files from Git:

	rm -f Text/* && git clone https://github.com/Merri/civ5suomeksi.git temp && cp -r temp/* ./ && rm -rf temp

To make it a fully functional Git clone:

	rm -f Text/* && git clone https://github.com/Merri/civ5suomeksi.git temp && mv temp/.git* ./ && cp -r temp/* ./ && rm -rf temp


Should anything go wrong you chould be able to recover by writing:

	rm -rf .git
	rm -rf temp

Those remove Git clone and the temp directory if it exists.
