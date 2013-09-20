## Repositories der Kursteilnehmer
[Akar Akyazi](https://github.com/canik77)  
[Waldemar Averin](https://github.com/Bob7419/vwanur)  
[Christian Engerling](https://github.com/cengerling/vwa)  
[Alexander Faber](https://github.com/faxel2201/vwa)  
[Sebastian Hauser](https://github.com/SH702/testvorlesung)  
[Tilman Korbacher](https://github.com/Avatar78/vwaproject)  
[Gabriel Susic](https://github.com/GS-VWA/VWA-01)  
[Joerg VWA ;-)](https://github.com/Joerg-vwa/ium-projekt)  
[Tobias Ziegler](https://github.com/froggy006/zt)  
  
## Links zu wichtigen Downloads  
[Pantheon Drupal Hosting](https://www.getpantheon.com/)  
[Drupal Quickstart](https://drupal.org/project/quickstart)  
  
## Beispielrepository von Dominik (vwadev)
[vwadev](https://github.com/dominikb1888/vwadev)
  
## Kurzanleitung Quickstart  
1. Download von Drupal Quickstart (Link siehe oben)  
2. Im Ordner /home/quickstart/websites eine neue Seite anlegen mit "drush qc --domain=<meineseite.dev> --makefile=d7.make"  
3. Herunterladen eines Templates (z.B. Bootstrap) per "drush dl bootstrap". Die Dateien sind unter "sites/all/themes/templates/bootstrap" zu finden.
4. Erstellen eines Subthemes durch kopieren des Beispielordners nach "sites/all/themes", der mit dem Bootstrap Theme kommt. Umbenennen des Ordners (z.B. in "vwa")
5. Erstellen eines git repository im Ordner "sites/all/themes/vwa" und pushen der Dateien per 
```
git init  
git add *  
git commit -am 'initial'  
git remote add origin <PFAD ZUM EIGENEN GIT REPOSITORY>  
git push origin master  
```
6. Original Makefile (/home/quickstart/websites/d7.make) kopieren und eigenes makefile erstellen, umbennen in "vwa.make". Folgende Zeilen einf�gen (L�dt Drupal 7 und Bootstrap + eigenes Sub-Theme herunter):
7. Eigenes Makefile testen durch das erstellen einer Testseite per "drush qc --domain=<meineseite.tst> --makefile=<meinmakefile.make>". Makefile kann dabei heruntergeladen oder direkt �ber http-URL im Befehl genutzt werden.
 
### Beispielcode f�r ein Makefile (eigene Repository-URL - in <> - ersetzen oder Adresse des Zip-Archivs komplett einsetzen)
```
core = 7.x
api = 2

projects[drupal][type] = "core"

projects[bootstrap][type] = "theme"

projects[vwa][download][type] = "get"
projects[vwa][download][url] = "<PFAD ZUM EIGENEN GIT REPOSITORY>/archive/master.zip"
projects[vwa][type] = "theme"
```


