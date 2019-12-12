Warnung: Du verwendest diese Programm auf eigene Gefahr hin!
1) Wenn das Programm abst�rzt, wirst du wahrscheinlich keinen Support
    vom Spielehersteller bekommen. Aber du kannst den Fehler gerne
    angeben unter:  http://code.google.com/p/texmod/issues/list
2) Spiele k�nnen detektieren, ob sie ver�ndert werden, daher riskierst du
    einen Bann deines online Accounts.
3) Dies ist eine open-source Projekt. Der Code kann von jedem erhalten, ver�ndert
    und kompiliert werden. Lade Universal Modding Engine nur von offiziellen Quellen runter,
    denen du vertraust. Lade es selbst runter und verwende keine Versionen,
    die du von Team- oder Gildenmitgliedern geschickt bekommen hast.
    http://code.google.com/p/texmod/downloads/list

   
Universal Modding Engine verwendet die D3DX9_43.dll (32bit). Wegen den EULA kann
diese dll nicht mit Universal Modding Engine mit geliefert werden. Wenn diese dll auf
deinem System nicht installiert ist, wird dich Universal Modding Engine darauf hinweisen.


Was kann Universal Modding Engine (uMod) V1.0?

-einzelne Texturen aus einem Spiel extrahieren und speichern (Die Zieltextur kann im Spiel ge�ndert werden.)
-alle Texturen aus einem Spiel extrahieren und speichern
-Texturen in ein Spiel laden und Zieltexturen ersetzen
-Support einzelner dds Texturen
-Support von zip-Dateien
-Support der originalen TexMod *.tpf Datein

Alle diese Optionen k�nnen w�hrend des Spieles an und aus geschaltet werden!
Du kannst also nach einer Textur suchen, diese speichern, sie anschlie�end
editieren, sie in das Spiel laden, sie nach bearbeiten und wieder in das
Spiel laden, ... oder Mods aktivieren und deaktivieren
und das alles ohne das Spiel neu starten zu m�ssen.

Randbemerkung: Wenn alle Texturen gespeichert werden sollen, so geschieht das nur,
wenn die Texturen vom Spiel geladen werden und auch nur in dem Moment, wenn sie
geladen werden. Stellst du diese Option an, w�hrend die Map bereits geladen ist, wird
wahrscheinlich nichts geschehen, da alle Texturen f�r diese Map bereits geladen sind.
Wechsle also die Map oder lade erneut.

Zip Dateien k�nnen eine "texmod.def" Datei enthalten, welche die Hash-Werte und
Dateinamen enth�lt. Jede Zeile sollte dem Format "hash|filename.dds" entsprechen.
Wenn es keine "texmod.def" Datei enth�lt, wird jede Datei entpackt und jene, deren 
Namen auf das Wildcard  "*_hash.dds" zutrifft, werden benutzt.
Die Zip Datei kann eine "Comment.txt" Datei enthalten. Der Inhalte wird als Kommentar
in der GUI angezeigt.

Wenn du einzelne Dateien l�dst, sollten diese dem Wildcard  "*_hash.dds" entsprechen.


Wie interagiert Universal Modding Engine mit den Spielen?

Universal Modding Engine klingt sich zwischen die Verbindung vom Spiel und DirectX ein.
Das verlangt, dass Universal Modding Engine bereits vor dem Spiel gestartet wird.

Die GUI von Universal Modding Engine fungiert als Server. Ein Spiel, in das sich erfolgreich
eingeklingt wurde, verbindet sich beim Programmstart mit dem Server.
Die GUI von Universal Modding Engine kann mehrere Spiele gleichzeitig verwalten.
Jede Instanz eines Spieles wird auch separat gehandhabt (wenn ein Spiel
mehrfach gestartet wird).


Wie bekomme ich Universal Modding Engine zum laufen?

Es gibt drei Wege wie uMod sich in die DirectX Verbindung einklinken kann:
(Benutze NICHT mehrere Methoden gleichzeitig!)

1) F�ge die Spiel-exe �ber das Men� "Einstellungen->Spiel hinzuf�gen" hinzu.
    F�r Steam siehe unten.
    
    bekannte Probleme: Guild Wars (Win XP)
    
2) Starte das Spiel direkt durch OTM �ber das Men�
     "Einstellungen->Sarte Spiel durch OTM" oder
     "Einstellungen->Sarte Spiel durch OTM (mit Kommandozeile)".
     Das Spiel startet sofort.

3) Kopiere die d3d9.dll (vom uMod Verzeichnis) in das Spiele Verzeichnis.
    Einige Spiele laden eine dll zuerst aus dem eigenen Verzeichnis bevor sie im
    Systemverzeichnis suchen. Nur f�r diese Spiele wird diese Methode funktionieren.
    WARNUNG: Kopiere diese dll niemals in das Systemverzeichnis!!
    
    bekannte Probleme: Guild Wars
   
Wenn  du dich f�r die erste oder dritte Methode entschieden hast, starte einfach
Universal Modding Engine und danach das Spiel. Starte das Spiel in beiden F�llen NICHT �ber
Universal Modding Engine .

Wenn das Spiel startet und alles glatt l�uft, �ffnet sich sofort ein neuer Tab in uMod.
In diesem Tab kannst du nun das Spiel  modden. Dr�cke den "Update" Button um
die Einstellungen an das Spiel zu senden. Du kannst deine aktuellen Einstellungen auch
als ein Template speichern. Ein Template kann auch als Standard eingestellt werden.
Es wird dann automatisch geladen und an das Spiel gesendet, wenn
dieses Spiel das n�chste Mal gestartet wird.

Um einen Mod zu laden, musst du das H�kchen vor den Namen setzen. Wenn du
den Mod entladen willst, entferne das H�kchen und klicke auf "Update".

Der Update Button l�dt nur Ver�nderungen (wenn 1) Pakete aus der Liste entfernt
wurden, 2) du die H�kchen ver�ndert hast oder 3) sich die Reihenfolge ge�ndert hat)
Der "neu laden" Button erzwingt das Neuladen von Festplatte (z.B. wenn du die
Texturen ver�ndert hast).

Weil verschiedene Mods die gleiche Ziel-Textur ver�ndern k�nnten, wird nur die
Mod-Textur des ersten Mods ber�cksichtigt. Die Aktion dieses Mods (also Laden oder
Entladen) wird durchgef�hrt, ungeachtet dessen, was die restlichen Mods mit der
Ziel-Textur machen sollen.


Wie bekommt man Universal Modding Engine mit Steam zum Laufen?

uMod schaut auf den Namen und auf das Verzeichnis der ausgef�hrten Spiel-exe.
Daher solltest du nicht die steam.exe sondern die Spiel.exe hinzuf�gen.
z.B.: C:\Steam\SteamApps\acoount_name\portal\hl2.exe
Wenn du die entsprechende exe nicht findest, kannst du das Spiel normal starten und 
�ber den TaskManager die entsprechende exe suchen. �ber Rechstklick->Eigenschaften
erf�hrst du dann auch den Pfad der exe.