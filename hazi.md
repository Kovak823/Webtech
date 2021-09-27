# R Markdown feladat

## Leírás

A dokumentum tartalma az lesz, hogy lépésről lépésre leírja a szoftver infrastruktúrájához való telepítést, mely majd ahhoz szükséges, hogy a make parancs sikeresen végrehajtható legyen a később klónozott tárolóból, amit a feladat leírásából megtudunk, mely két állományt tartalmaz.

===================================================================================

## Visual Studio Code

Létre hoztunk egy visual studio code-ban egy Markdown állományt, de előtte le kellett tölteni a megfelelő pluginokat, ilyenek például a Markdown All in one, Markdown+math és a live servert is. Segítségképpen ha a "hazi.md" fülre kattintuk jobb klikkel és kiválasztjük az "Open Preview" és jobb fent található "Split editor"-t is kiválasztjuk és átteszük jobb oldalra a "Preview hazi.md" fájlt akkor láthatjuk a jobb oldalt a Markdown állomány böngészőbeli mását és változtatás esetén frissül. A fenti fülek közül ki tudjuk választani a "Terminal" fület és azon belül a "New Terminal"-t, ami egy parancssort nyit meg, ami által könnyebb lesz a prancsokat írni.

===================================================================================

## Terminal

A Terminálban létre kell hoznunk egy conda környezetet vagy használni egy meglévő környezetet és ennek megtekintéséhez a ```conda env list``` parancsot tudjuk használni, hogy megnézzük milyen környezetek vannak. Új környezet létrehozásához a ```conda create --name (környezet neve)``` parancsot kell kiadnunk. A meglévő conda környezetet a ```conda activate (név)``` parancsal tudjuk aktiválni(és majd a ```conda deactivate``` prancsal tudunk kilépni). Amint ezek megvannak le kell, hogy töltsük a git-et a conda segítségével a következő parancs segítségével, ami a 
```conda install git ```https://git-scm.com. Következőképpen a git clone https://github.com/jeszy75/rmarkdown-examples kell kiadnunk a parancssorban, hogy le tudjuk klónozni a tárolót. A továbbiakbanki ki kell adni a ```conda install make parancsot``` https://www.gnu.org/software/make/ és a ```conda install pandoc``` parancsot https://pandoc.org, hogy a későbbiekben tudjuk használni a make parancsot. A csomagok telepítéséhez engedélyeznünk kell a conda-forge-, amit a következő parancsokkal tudunk megtenni https://conda-forge.org:
```
conda config --add channels conda-forge

conda config --set channel_priority strict
```
A ```conda search r-base``` parancs kiadásával megtekinthetjük, hogy éppen milyen verziói vannak az r-base-nek.
Ezek melletki kell adni a következő parancsokat:
```
conda install r-markdown
conda install r-gyplot2
conda install readr
conda install rgdol r-sf r-curl
```
Ezek után a parancsosorba be kell írnunk az R parancsot, ami segítségével majd az ```install.packages("ggspatial")``` csomagot le tudjuk tölteni.

Végezetül majd még a 
```
conda install r-reticukate
 és
conda install r-dbi r-eqlite
```
prancsot kell kiadnunk. Legvégezetül pedig a make parancsot.

===================================================================================

## Neptun

Neptun kód: IN1CVX