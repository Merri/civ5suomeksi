# Civilization V suomeksi!

This is Finnish language pack for Sid Meier's Civilization V.
[Installation instructions in English.](https://github.com/Merri/civ5suomeksi/blob/master/README.MD)

2010 - 2016 Vesa Piittinen


## Asennus ZIP-tiedostosta

Selvitä `Sid Meier's Civilization 5` käyttäjähakemisto. Esimerkkejä sijainnista:

- Windows 7, 8, 10: `C:\Users\KÄYTTÄJÄNIMI\Documents\My Games\Sid Meier's Civilization 5`
- Windows 7, 8, 10: [Git Bash] `cd ~/Documents/"My Games"/"Sid Meier's Civilization 5"`
- Mac OS X: `Users/KÄYTTÄJÄNIMI/Library/Application Support/Sid Meier's Civilization 5`
- Mac OS X: `cd ~/Library/Application Support/Sid Meier's Civilization 5`

Löydät `config.ini`-tiedoston kyseisestä hakemistosta. Rivillä 66 pitäisi lukea: `Language = en_US`.
Kirjoita tilalle `Language = fi_FI`.

Seuraavaksi `Suomi*.xml`-tiedostot tarvitsee kopioida samassa paikassa sijaitsevaan Text-hakemistoon.

Tämän jälkeen peli käynnistyy suomeksi ja voit pelata muiden pelaajien kanssa riippumatta heidän pelikielestään!


## Asennus käyttäen gittiä ja komentoriviä (Git Bash Windowsissa)

Jos et ole asentanut gittiä, niin [käy kipaisemassa se itsellesi!](https://git-scm.com/download) (Asennuksen voi tehdä oletusasetuksin.)

1. Avaa komentorivi (Git Bash)
2. Siirry Civ 5:n käyttäjähakemistoon: `cd ~/Documents/My\ Games/Sid\ Meier\'s\ Civilization\ 5/`
3. Vaihda kieli suomeksi: `perl -pi -w -e 's/^Language = en_US/Language = fi_FI/;' config.ini`
4. Nyt tiedostot voi kopioida. Tämän voi tehdä kahdella tavalla: yksinkertaisena kopiona tai täydellisenä Git-kloonina.

Jos haluat vain tiedostot:

	rm -f Text/* && git clone https://github.com/Merri/civ5suomeksi.git temp && cp -r temp/* ./ && rm -rf temp

Jos haluat täyden kloonin (eli tehdä itse muutoksia ja kirjata ne gitillä):

	rm -f Text/* && git clone https://github.com/Merri/civ5suomeksi.git temp && mv temp/.git* ./ && cp -r temp/* ./ && rm -rf temp


Asioiden mennessä pieleen pitäisi normaalitilanteeseen päästä tällä:

	rm -rf .git
	rm -rf temp

Nämä poistavat git-kloonin ja temp-hakemiston, mikäli se on jäänyt kummittelemaan.
