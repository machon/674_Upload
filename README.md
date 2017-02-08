			***Konzept 674 App***
			*********************
Eine App zum Download für PC und Mac. Über diese App werden Mixe hochgeladen, später auch eventuell runtergeladen. 
Bevor ein Mix hochgeladen wird, werden folgende Dinge überprüft:
1. Namenskonvention (Name des Uploaders/Datum)
2. Konvertierung
3. mp3 tags


Klassen:
1. Klasse die mit FTP Server verbindet und Daten editiert
2. Klasse die mp3 tags handhaben kann

Schritte:
1. Klassen erstellen
2. Formular zum Upload erstellen
3. Verbindung mit FTP herstellen und Methode für Upload umsetzen
5. Regeln für das Formular erstellen
6. Fehlermeldungen/Exceptions
7. Taglib einbinden
8. Testcases erstellen

Auszug aus 674 wiki für Upload der Automationsmixe:
Vorproduzierte Sendungen
Audioformat und FTP-Upload

Audioformat: MP3, 192kb/s
Andere Formate oder andere Bitraten werden nicht akzeptiert.

Dateiname: Sendungsname_YY.MM.TT.mp3
Der komplette Dateiname könnte dann so aussehen: somethingforyourears_170101.mp3

Länge: Sendezeit minus 30-60 Sekunden
damit noch Platz für einen Jingle bleibt. FIXME

    1-stündige-Sendung: zwischen 0:59:00 und 0:59:30
    2-Stunden-Sendung: zwischen 1:59:00 und 1:59:30
    3-Stunden-Sendung: zwischen 2:59:00 und 2:59:30

ID3-Tag: Titel = Showname, Artist = DJ-Name, Genre, Jahr

Die meisten Programme fragen schon beim abspeichern die Metadaten bzw. ID-Tags ab. Ansonsten kann man diese unter Windows auch in den Datei-Eigenschaften nachträglich ändern
Zeitplan und Vorgehensweise
Vorproduzierte Shows müssen 3 Tage vor Sendebeginn auf den FTP-Server hochgeladen sein!

Vorproduzierte Shows können nur per FTP (file transfer protocoll) auf den Server geladen werden.
Hierfür benötigst du ein kleines Programm, bzw. einen ftp-client wie z.B. www.filezilla.de , https://cyberduck.io oder www.leechftp.de

Sendungen, die sich nicht auf dem FTP Server befinden, können nicht in die Automation aufgenommen werden und werden nicht gesendet !
Downloadlinks wie dropbox, sendspace, wetransfer, soundloud, etc. werden ignoriert

Auf dem FTP Server hast du nur das Recht hochzuladen. Du kannst weder löschen noch andere Dateien downloaden. Du kannst die Datei mit drag&drop direkt ein-stellen oder einen Ordner anlegen.

Sollte ein Upload abbrechen, musst du den Upload erneut starten. Da du die “kaputte” Datei nicht löschen könnt, musst du die neue Datei umbenennen:
Stelle dem Dateinamen eine NULL voran.

    Sendung_YY.MM.TT.mp3 - abgebrochen oder fehlerhaft
    0Sendung_YY.MM.TT.mp3 - neuer, vollständiger oder korrigierter Upload
    00Sendung_YY.MM.TT.mp3 - falls du es ein drittes Mal versuchen musst, usw…

Bescheid geben

Um sicherzugehen, dass die Sendung rechtzeitig eingeschleift wird, sendet nach erfolgreichem Upload eine kurze Mail an programm@674.fm 
