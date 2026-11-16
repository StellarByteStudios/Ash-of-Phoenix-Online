# Promt für Springanwendung



## Grobe Idee
Ich habe selbst ein Pen and Paper Regelwerk erfunden. Dieses wurde in Word (später libreOffice) verfasst. Es sind verschiedene Dokumente und Listen wie Grundregeln, Kampfmechaniken, Klassen, Rassen, Gegenstandslisten und vieles mehr. Ich möchte jetzt eine Spring Anwendung schreiben, mit welcher ich diese Informationen online als Webseite bereitstellen kann. Diese Anwendung soll heißen "Ash of Phoenix Online" kurz "AoP-Online"



## Hardware und System
Ich habe bereits einen Server (Raspberry Pi mit RasperianOS). Auf diesem läuft bereits eine Anwendung, sowie ein NGinx Dienst, durch welchen ich den Zugriff von außen regele. Alles davon läuft in separaten Docker Container. Die neue Anwendung (AOP-Online) soll als Spring ebenfalls als ein Docker-Container starten.


## Inhalt und Darstellung
Die Inhalte sind einerseits Texte und andererseits auch viele Tabellen. Die bisherigen Dokumente wurden hauptsächlich in Word und LibreOffice erstellt. (Im Repository [AoP Repo](https://github.com/StellarByteStudios/Ash-of-Phoenix-Online/tree/main/Vorlagen-Dokumente) liegen in einem Ordner die Dokumente die ich bereits erstellt habe. Nutze diese als eine Basis um die Struktur aufzubauen) Ich möchte jetzt eine Onlinedarstellung dieser Dokumente haben. Das Design soll schlicht und wenig aufregend sein. Die Seite sollte sich am Design von Wikipedia orientieren. Das bedeutet vorallem Die Navigationsleiste an der linken Seite, bzw. oben für Handydarstellung. Jedoch soll nicht alles auf einer Seite geladen werden, sondern die Kapitel (Gesteuert durch die Navigationsleiste) sollen eigene Unterseiten bekommen. So soll zum Beispiel eine Unterseite Existieren, welche die Klassen und Klassenwahl beschreibt und dann soll es für jede Klasse nochmal eine eigene Unterseite geben. Im Textkörper möchte ich wie Wikipedia Text, Tabellen und ggf. Bilder verwenden.
Für bestimmte Tags möchte ich Icons verwenden:
* Flamme für Verbrennung
* Grüne Flasche für Vergiftung
* Kettenhemd für Rüstung
* Hände für einhand, oder zweihandwaffen
* usw.

### Tabellenfilter
Wenn man Tabellen hat soll es möglich sein nach Werte in einer Spalte zu sortieren und zu filtern. Wenn ich z.b. die Liste aller Waffen habe möchte ich mir nur die einhändigen Waffen, oder die Stangenwaffen anzeigen lassen.

### Dungeon-Master-View
Man soll die Möglichkeit haben von der Player-View auf die Dungeon-Master-View umzuschalten. In der Player-View sollen einige Kapitel nicht angezeigt werden, welche für diese nicht relevant sind. Man soll beim anlegen und bearbeiten jeder Seite einfach angeben können, ob diese auch in Player-View gesehen werden kann oder nur im Dungeon-Master-View.

### Optik
Erzeuge das Grundlegende CSS Mobile-first und gebe mir die Möglichkeit die Farben zu ändern, indem du für alle Farben die Verwendet werden Konstanten verwendest, die am Anfang definiert werden.

### Sprache
Ich werde alle Texte auf Deutsch verfassen, möchte mir aber offen halten sie später noch zu überseten. Man soll dann später auch auf der Webseite die Sprache einstellen können. Jede Unterseite soll dann in der entsprechenden Sprache angezeigt werden. Füge die Möglichkeit dieser Erweiterung ein, auch wenn noch keine andersprachigen Texte bisher existieren.



## Navigation auf der Seite
Ich möchte die Seite in unterseiten Einteilen, durch welche man übersichtlich Navigieren kann. Dazu soll eine Navigationsleiste eingefügt werden, mit welcher man durch die einzelnen Kapitel und Unterkapitel navigieren kann. Auch soll es möglich sein, die Seiten im Text untereinander zu verlinken. Wenn ich z.b. bei einem Zauber einen Effekt wie Verbrennung erwähne soll das über ein Link mit der Seite zur Erklärung von Verbrennung verlinkt sein.
Ich möchte auch eine Suche haben, sodass ich nach bestimmten Themen suchen kann und dann auf die entsprechende seite komme. Z.b. möchte ich in der Suche Feuerball eingeben können und werde dann auf die Seite des Zaubers geleitet.


### Aufbau der Kapitel
Auch wenn du dich an die Struktur in den eingelesenen Dokumenten richtest, die nun folgende Struktur soll stärker berücksichtigt werden beim Aufbau der Webseite:
* Grundmechaniken
    * Geld
    * Kampfsystem
        * Aktionen
        * Trefferwürfe
        * Schaden
        * Waffenloser Angriff
    * Waffen-Grundlagen
    * Resistenten und Immunitäten
    * Ohnmacht und Tod
    * Zusatzeffekte
        * Rettungswürfe
        * Verbrennung
        * Gift
        * Blutung
        * Gefrieren
        * Lähmung
        * Stun
    * Skillthrows
        * Vor- und Nachteilswürfe
    * Reisen
        * Schlaf
        * Essen
    * Leveln
    * Inventar
* Attribute
* Charaktererstellung
* Charakterbogen
    * Zauberbuch
    * Kräutersäckchen
* Rassen
    * (Seite für jede Rasse)
        * (Mögliche Unterseite bsp: Elfen -> Mondelfen)
* Klassen
    * (Seite für jede Klasse)
       * (Mögliche Sub-Klassen bsp: Krieger -> Kämpfer/Wächter) 
* Lore
    * Sprachen
    * Astralebenen
    * Magie und Mana
    * Zusätzliche Lore
        * Götter
        * Mythologien
            * Menschen
        * Weltenaufbau und Natur
* Tränke
* Gegenstände
    * Waffen
    * Rüstung
    * Fallen
    * Ausrüstung und sonstige Gegenstände
* Kreaturen und sonstige Wesen
    * Humanoide
        * (Unterseite für jedes Wesen)
    * Tiere
        * (Unterseite für jedes Wesen)
    * Mystische Geschöpfe
        * (Unterseite für jedes Wesen)
    * Astrale Gestalten
        * (Unterseite für jedes Wesen) 
    * Drachenartige
        * Drachen
            * (Unterseite für jedes Wesen) 
        * Drachenverwante
            * (Unterseite für jedes Wesen) 
* NPCs




## Editierung
Ich möchte eine Möglichkeit einbauen die Texte direkt auf der Webseite zu editiern, ähnlich wie in Wikipedia. Dazu soll man sich als Editor ausgeben können (mithilfe von Passwort). Das Editieren soll in rich-text wie Markdown möglich sein. Vorzugsweiße sollen auch LaTeX Befehle gerendert werden. Die Änderungen sollten persistent gegenüber einem Neustart der Anwendung sein. Man soll auch neue Unterkapitel anlegen können.


### Editierung Charakterbögen
Die Charakterbögen haben eine sehr aufwendige Formatierung. Um diese zu editieren ist vermutlich Latex als grundbasis sinnvol. Baue den Bogeneditor so, dass ich Latex-Code angeben kann, der dann so gerendert wird, sodass man online dann das fertige PDF herunterladen kann.



## Technische Entscheidungen
* Speichern von Bildern in lokalem File-System
* Nutze als Editor den CKEditor