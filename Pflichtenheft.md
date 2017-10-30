# Pflichtenheft

## Funktionale Anforderungen

### Grundfunktionen

#### Allgemein

- Einloggen
- "Passwort vergessen"-Funktion
- Ausloggen

#### Impressum

- Impressum anzeigen

#### Hilfe

- Hilfe anzeigen

#### Kontaktformular

- Kontaktformular anzeigen
- Kontaktformular absenden

#### Benutzerverwaltung

- Benutzer erstellen
- Benutzerprofil verwalten/ändern
- Benutzerprofil löschen

#### Push-Nachrichten

- Push-Nachrichten automatisch versenden

### Veranstaltung

#### Allgemein

- Veranstaltung erstellen
- Veranstaltung verwalten
- Veranstaltung ändern
- Veranstaltung anzeigen (Gast, Registriert, Organisator)
- Gästeliste

#### Berechtigungen

- Berechtigungen erteilen
- Berechtigungen entziehen
- Berechtigungen anzeigen

#### Einladungen

- Einladen via QR-Code
- Einladen via Weblink
- (Einladungen zurücknehmen?)
- Zu- und Absagen (Gast, Registriert)
- Gästeliste anzeigen

#### Aufgaben

- Aufgaben anzeigen
- Aufgaben verwalten
- Aufgaben verteilen
- Aufgaben übernehmen

#### ToDo-Liste

- ToDo-Liste anzeigen
- ToDo-Liste verwalten

#### Kostenübersicht

- Kostenübersicht anzeigen
- Kostenübersicht bearbeiten

#### Galerie

- Startseite (einer bestimmten Galerie) anzeigen
- Fotos hochladen
- Fotos herunterladen
- Fotos anzeigen
- (Galerieübersicht (alle verfügbaren Galerien) anzeigen)
- (Fotos kommentieren?)

#### Kommunikation

- Kommentar erstellen 
- Kommentar bearbeiten
- Kommentar löschen
- (Privatchats)
- (Gruppenchats)

#### Abstimmungen

- Abstimmung erstellen
- Abstimmung bearbeiten
- Abstimmung anzeigen
- Abstimmen

#### Bewertung

- Bewertung anzeigen
- Bewertung abgeben
- Bewertung ändern

#### Einchecken

- Übersicht anzeigen
- Gast-QR-Code anzeigen
- QR-Code scannen
- Gast einchecken


#### (Social-Media)

- Über Social-Media-Profil anmelden
- Bilder / Veranstaltung per Social-Media teilen

## Nicht-Funktionale Anforderungen

### Server

### Datenbank

### App

- Android
- iOS
- (für Tablets optimiert)

### Webanwendung

- Desktopversion
- mobile Version

## Systemarchitekturdiagramm


## Detailbeschreibung

### Nicht-Funktionale Anforderungen

#### Webanwendung

Die Anwendung soll von den gängigen Browsern korrekt dargestellt werden.  Design und Bedienung der Website entsprechen den aktuellen Technologien und sind intuitiv. Die Webanwendung ist für mobile Geräte optimiert.

#### App

Eine native Lösung für Android und iOS soll angeboten werden. Design und Bedienung sollen dabei ebenfalls zeitgemäß und den Technologien angepasst sein.

Optional sind die Apps auch für Tablets optimiert.

#### Datenbank

Die Verwaltung der Daten soll ein entsprechendes Datenbankmanagmentsystem übernehmen. Es muss ausreichend dimensioniert sein, damit ausreichend Daten gespeichert werden können, sowie das Abrufen und Schreiben von Daten zügig erfolgt.

#### Server

Die Hauptanwendung soll auf einem Server laufen. Auch der Server muss ausreichend Ressourcen bereitstellen, damit ein Betrieb von mehreren Clients  gleichzeitig möglich wird.

### Funktionale Anforderungen

#### Grundfunktionen

##### Allgemein

###### Einloggen

Es ist möglich sich zum Beginn als Gastuser oder registrierter User anzumelden. Bei der Anmeldung als registrierter Benutzer gibt es einen Dialog, falls man sein Passwort vergessen hat.

###### Ausloggen

Es ist zu jeder Zeit möglich sich aus der Anwendung auszuloggen.

##### Impressum

Das Impressum muss jeder Zeit erreichbar sein.

##### Hilfe

Die Hilfe zur Anwendung muss jederzeit erreichbar sein.

##### Kontaktformular

Zusammenfassung der Kontaktdaten des Entwicklers. Hierzu gehören Firmenname, E-Mail, Adresse, Telefon und Angaben zur Erreichbarkeit.

##### Benutzerverwaltung

Es soll zwei Möglichkeiten geben sich an dem System anzumelden. Einmal als registrierter Benutzer und einmal als Gast. Als registrierter Benutzer erhält man ein Benutzerprofil, über das man seine persönlichen Daten verwalten kann. Hierzu zählen Name,Adresse,Foto,vergangene Veranstaltungen, zukünftige Veranstaltungen... Auch muss man hier die Möglichkeit haben, den Benutzer zu löschen.

Für die Erstellung eines Profiles muss ein entsprechender Dialog existieren, in dem die oben genannten Daten abgefragt werden. 

Als Gast hat man nur Zugriff auf eine Veranstaltung, muss dafür aber auch nur einen Namen angeben.

Wie man sich einloggen möchte, muss auf der Anmeldeseite abgefragt werden. Auf dieser Seite muss auch einen Dialog geben, falls ein registrierter Benutzer sein Passwort vergessen hat.

Es muss jeder Zeit möglich sein sich auszuloggen.

##### Push-Nachrichten

User erhalten per Push-Nachricht Erinnerungen zu ihren Veranstaltungen auf das Smartphone.

#### Veranstaltung

##### Allgemein

In der Veranstalung müssen die folgenden Informationen jederzeit jedem Gast/ Organisator zu jeder Zeit zur Verfügung stehen. Auch müssen diese Informationen von den Organisatoren erstell- bzw. änderbar sein.

###### Name

Der Name der Veranstaltung. 

###### Beschreibung

Ein freier Beschreibungstext zur Veranstaltung.

###### Gastgeber / Ansprechpartner

Hier stehen der Gastgeber, bzw. die Organisatoren.

###### Ort

Ort der Veranstaltung. Hier muss nicht zwingend eine gültige Adresse eingegeben werden, damit auch benutzereigene Beschreibungen möglich sind. Wenn eine gültige Adresse eingegeben wurde, muss diese von Google Maps (Web, Android) oder Maps(iOS) verarbeitet werden können.

###### Zeitpunkt

Datum und Uhrzeit der Veranstaltung. Es muss eine Verbindung zu den Systemkalendern (Android,iOS) bestehen, damit der Termin direkt übertragen werden kann. Auch sollten die Termine in einer Übersicht im Benutzerprofil angezeigt werden (Kalenderwidget).

###### Gästeliste

Es gibt eine Übersicht, in der die Gästeliste für alle einsehbar angezeigt wird.

##### Berechtigungen

Der Organisator kann andere Gäste zu Organisatoren machen oder andere auf den Status eines normalen Gastes zurücksetzen.

Auch muss es eine Ansicht geben, in der alle Berechtigungen aufgelistet sind.

##### Einladungen

Einladungen können sowohl über QR-Code, als auch über Link versendet werden. Die Einladungen können in Zeit und Menge der Zusagen beschränkt werden.

Es gibt ein Menü, in dem die Gäste Zu- oder Absagen können. Auch eine Übersicht über den aktuellen Status der Gästeliste muss es geben.

Optional kann implementiert werden, dass Einladungen auch wieder zurückgenommen werden können.

##### Aufgaben

Liste mit Aufgaben, die noch erledigt werden müssen. Mit dieser Funktion sollen zum Beispiel Mitbring-Buffets organisiert werden. Die Aufgaben können vom Organisator zugeteilt oder freiwillig von einem Gast übernommen werden.

##### ToDo-Liste

Die ToDo-Liste ist nur von dem Organisator einsehbar. Dieser kann die ToDo-Liste verwalten und Punkte hinzufügen oder löschen. Auch können bereits nortierte Punkte als erledigt markiert werden.

##### Kostenübersicht

Die Kostenübersicht ist nur von dem Organisator einsehbar. Dieser kann hier jede Ausgabe und Einnahme mitprotokollieren und erhält eine Gesamtsumme der Ein- oder Ausgaben.

##### Galerie

Pro Veranstaltung gibt es eine Galerie.  Diese besitzt einen Startbildschirm, in dem alle Bilder als Vorschau angezeigt werden. Die Bilder können dann ausgewählt werden und in groß angeguckt werden.

Auch werden hier Aktionen zum Up- oder Download von Bildern angeboten.

Optional kann auch eine Übersicht aller Galerien für einen Benutzer implementiert werden. Auch das Kommentieren von Fotos ist optional.

##### Kommunikation

In der Veranstaltung können Beiträge geschrieben, verändert oder kommentiert werden.

Optional können auch Chats unter registrierten Usern oder Gruppenchat implementiert werden.

##### Abstimmung

Es gibt eine Übersicht aller laufenden und vergangenen Abstimmungen zur Veranstaltung. Bei Auswahl einer Abstimmung, kann hier jeder Gast abstimmen.

Der Organisator kann Abstimmungen erstellen. Dazu kann er eine Fragestellung eingeben und die Laufzeit der Abstimmung auswählen. Nach Ablauf der Laufzeit wird automatisch eine Auswertung erstellt und angezeigt. Auch hat der Organisator hier die Möglichkeit die Abstimmung nachträglich zu verändern oder zu löschen.

##### Bewertung

Nach der Veranstaltung können die Gäste eine Bewertung der Veranstaltung abgeben. Diese Bewertung kann nachträglich verändert werden.

##### Einchecken

Das Einchecken kann ebenfalls von der Anwendung übernommen werden. Hierfür können Gäste sich auf dem Smartphone einen QR-Code anzeigen lassen. Dieser kann dann von dem Gastgeber per Smartphone eingelesen werden.

Auch eine Übersicht zu allen Gästen wird angezeigt.

##### Social-Network

Dieser Menüpunkt kann optional implementiert werden.

Es gibt die Möglichkeit über ein Social-Network-Profil anzumelden. Auch können Bilder oder Veranstaltungen in Social-Media-Plattformen geteilt werden.


