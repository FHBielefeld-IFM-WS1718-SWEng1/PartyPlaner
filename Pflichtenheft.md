# Pflichtenheft

## Funktionale Anforderungen

### Grundfunktionen

#### Allgemein

- Einloggen
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

#### Benutzerprofil

- Alle Veranstaltungen anzeigen
- Meine erstellten Veranstaltungen anzeigen
- Meine Einladungen anzeigen
- Meine Kontakte anzeigen
- Profil als Kontakt hinzufügen / entfreunden
- Profil suchen

#### Push-Nachrichten

- Push-Nachrichten automatisch versenden

### Veranstaltung

#### Allgemein

- Veranstaltung erstellen
- Veranstaltung verwalten
- Veranstaltung ändern
- Veranstaltung anzeigen --> Gast, Organisator
- Gästeliste

#### Berechtigungen

- Berechtigungen erteilen
- Berechtigungen entziehen
- Berechtigungen anzeigen

#### Einladungen

- Einladen via QR-Code
- Einladen via Weblink
- Einladen via Profil
- (Einladungen zurücknehmen?)
- Zu- und Absagen --> User, (Gast)
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

- (Über Social-Media-Profil anmelden)
- (Bilder / Veranstaltung per Social-Media teilen)

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

![Systemarchitektur](img/sysarch/Systemarchitektur.jpg)


## Detailbeschreibung

### Nicht-Funktionale Anforderungen

#### Webanwendung

Die Anwendung muss von den gängigen Browsern korrekt dargestellt werden.  Design und Bedienung der Website entsprechen den aktuellen Technologien und sind intuitiv. Die Webanwendung ist für mobile Geräte optimiert.

#### App

Eine native Lösung für Android und iOS muss angeboten werden. Design und Bedienung müssen dabei ebenfalls zeitgemäß und den Technologien angepasst sein.

Optional sind die Apps auch für Tablets optimiert.

#### Datenbank

Die Verwaltung der Daten muss ein entsprechendes Datenbankmanagmentsystem übernehmen. Es muss ausreichend dimensioniert sein, damit ausreichend Daten gespeichert werden können, sowie das Abrufen und Schreiben von Daten zügig erfolgt.

#### Server

Die Hauptanwendung muss auf einem Server laufen. Auch der Server muss ausreichend Ressourcen bereitstellen, damit ein Betrieb von mehreren Clients  gleichzeitig möglich wird.

### Funktionale Anforderungen

#### Grundfunktionen

##### Allgemein

###### Einloggen

Es ist möglich sich als registrierter Benutzer einzuloggen. Zusätzlich kann ein Einloggen als Gastuser möglich sein.

###### Ausloggen

Es ist zu jeder Zeit möglich sich aus der Anwendung auszuloggen.

##### Impressum

Das Impressum muss jeder Zeit erreichbar sein.

##### Hilfe

Die Hilfe zur Anwendung muss jederzeit erreichbar sein.

##### Kontaktformular

Zusammenfassung der Kontaktdaten des Entwicklers. Hierzu gehören Firmenname, E-Mail, Adresse, Telefon und Angaben zur Erreichbarkeit.

##### Benutzerverwaltung

Man muss sich registrieren können. Als registrierter Benutzer erhält man ein Benutzerprofil, über das man seine persönlichen Daten verwalten kann. Hierzu zählen Name,Adresse,Foto,vergangene Veranstaltungen, zukünftige Veranstaltungen... Auch muss man hier die Möglichkeit haben, den Benutzer zu löschen.

Für die Erstellung eines Profiles muss ein entsprechender Dialog existieren, in dem die oben genannten Daten abgefragt werden. 

Zusätzlich kann man auch die Anmeldung als Gast umsetzen. Als Gast hat man nur Zugriff auf eine Veranstaltung, muss dafür aber auch nur einen Namen angeben.

Wie man sich einloggen möchte, muss auf der Anmeldeseite abgefragt werden. Auf dieser Seite muss auch einen Dialog geben, falls ein registrierter Benutzer sein Passwort vergessen hat.

Es muss jeder Zeit möglich sein sich auszuloggen.

##### Benutzerprofil

Es muss eine Übersicht geben, wo der User all seine Veranstaltungen auf denen er war oder auch Kommende sehen kann. Auch muss es eine Übersicht aller aktuellen Einladungen und der Veranstaltungen, die man selber erstellt hat, geben.

Ebenfalls kann man sich all seine Kontakte anzeigen lassen. Um einen Kontakt hinzuzufügen, hat man auf fremden Profilen die Möglichkeit, diesen als Kontakt zu markieren oder demarkieren. Damit man fremde Kontakte finden kann, muss es eine Suchfunktion geben.

##### Push-Nachrichten

User erhalten per Push-Nachricht Erinnerungen zu ihren Veranstaltungen auf das Smartphone.

#### Veranstaltung

##### Allgemein

In der Veranstalung müssen die folgenden Informationen jederzeit jedem Gast/ Organisator zur Verfügung stehen. Auch müssen diese Informationen von den Organisatoren erstell- bzw. änderbar sein.

###### Name

Der Name der Veranstaltung. 

###### Beschreibung

Ein freier Beschreibungstext zur Veranstaltung.

###### Gastgeber / Ansprechpartner

Hier stehen der Gastgeber, bzw. die Organisatoren.

###### Ort

Ort der Veranstaltung. Hier muss nicht zwingend eine gültige Adresse eingegeben werden, damit auch benutzereigene Beschreibungen möglich sind. Wenn eine gültige Adresse eingegeben wurde, muss diese von Google Maps (Web, Android) oder Maps(iOS) verarbeitet werden können.

###### Zeitpunkt

Datum und Uhrzeit der Veranstaltung. Es muss eine Verbindung zu den Systemkalendern (Android,iOS) bestehen, damit der Termin direkt übertragen werden kann. Auch müssen die Termine in einer Übersicht im Benutzerprofil angezeigt werden (Kalenderwidget).

###### Gästeliste

Es gibt eine Übersicht, in der die Gästeliste für alle einsehbar angezeigt wird.

##### Berechtigungen

Der Organisator kann andere Gäste zu Organisatoren machen oder andere auf den Status eines normalen Gastes zurücksetzen.

Auch muss es eine Ansicht geben, in der alle Berechtigungen aufgelistet sind.

##### Einladungen

Einladungen können sowohl über QR-Code, als auch über Link versendet werden. Die Einladungen können in Zeit und Menge der Zusagen beschränkt werden. Ebenfalls muss man direkt Benutzerprofile einladen können.

Es gibt ein Menü, in dem die Gäste Zu- oder Absagen können. Auch eine Übersicht über den aktuellen Status der Gästeliste muss es geben.

Optional kann implementiert werden, dass Einladungen auch wieder zurückgenommen werden können.

##### Aufgaben

Liste mit Aufgaben, die noch erledigt werden müssen. Mit dieser Funktion können zum Beispiel Mitbring-Buffets organisiert werden. Die Aufgaben können vom Organisator zugeteilt oder freiwillig von einem Gast übernommen werden.

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

## Mockups

### Website

####Startseite

##### Index

![Index](img/mockup/Website/Index.png)

##### Einloggen

![Einloggen](img/mockup/Website/Einloggen.png)

##### Registrieren

![Registrieren](img/mockup/Website/Registrieren.png)

##### Einladung Login

![Einladung Login](img/mockup/Website/Einladung Login.png)

##### Einladung annehmen

![Einladung annehmen](img/mockup/Website/Einladung annehmen.png)

#### Home

#####Hauptseite

![Hauptseite](img/mockup/Website/Home.png)

##### Glocke offen

![Glocke offen](img/mockup/Website/Glocke offen.png)

#### Profil

##### Hauptseite

![Hauptseite](img/mockup/Website/Profil.png)

##### Kontakt hinzufügen

![Kontakt hinzufügen](img/mockup/Website/Profil Kontakt hinzufügen.png)

#### Veranstaltung

##### Übersicht

![Übersicht](img/mockup/Website/Eigene Veranstaltungen.png)

##### Galerie

![Galerie](img/mockup/Website/Party Galerie.png)

##### Bild ansehen

![Bild ansehen](img/mockup/Website/Galerie Bild.png)

##### Kommentare

![Kommentare](img/mockup/Website/Party Kommentare.png)

##### Aufgabenliste

![Aufgabenliste](img/mockup/Website/Party Aufgabenliste.png)

##### Gästeliste

![Gästeliste](img/mockup/Website/Party Gästeliste.png)

##### Abstimmungen

![Abstimmungen](img/mockup/Website/Party Abstimmungen.png)

##### Abstimmung ansehen

![Abstimmung ansehen](img/mockup/Website/Party Abstimmung ansehen.png)

##### Bewertung

![Bewertung](img/mockup/Website/Party Bewertung.png)

#### Eigene Veranstaltung 

##### Gäste einladen

![Gäste einladen](img/mockup/Website/Party EV Gäste einladen.png)

##### Kommentare

![Kommentare](img/mockup/Website/Party EV Kommentare.png)

##### Aufgabenliste

![Aufgabenliste](img/mockup/Website/Party EV Aufgabenliste.png)

##### Kostenübersicht

![Kostenübersicht](img/mockup/Website/Party EV ToDoListe_Kostenübersicht.png)

##### Gästeliste

![Gästeliste](img/mockup/Website/Party EV Gästeliste.png)

##### Gästeliste einchecken

![Gästeliste einchecken](img/mockup/Website/Party EV Gästeliste einchecken.png)

##### Abstimmungen

![Abstimmungen](img/mockup/Website/Party EV Abstimmungen.png)

##### Abstimmung erstellen

![Abstimmung erstellen](img/mockup/Website/Party EV Abstimmung erstellen.png)

##### Abstimmung ansehen

![Abstimmung ansehen](img/mockup/Website/Party EV Abstimmung ansehen.png)

### App

#### Startseite

##### Index

![Index](img/mockup/App/Index.png)

##### Registrieren

![Registrieren](img/mockup/App/Registrieren.png)

##### Home

![Home](img/mockup/App/Home.png)

##### Menü

![Menü](img/mockup/App/Menü geöffnet.png)

##### Impressum

![Impresssum](img/mockup/App/Über uns.png)

#### Profil

##### Eigenes Profil

![Profil](img/mockup/App/Eigenes Profil.png)

##### Fremdes Profil

![fremdes Profil](img/mockup/App/Profil von wem anderes.png)

##### Kontakte

![Kontakte](img/mockup/App/Kontakte.png)

##### Kontaktformular

![Kontaktformular](img/mockup/App/Kontaktformular.png)

#### Veranstaltung

##### Übersicht

![Übersicht](img/mockup/App/Eigene Veranstaltungen.png)

##### Veranstaltung anschauen

![Veranstaltung](img/mockup/App/Veranstaltung anschauen.png)

##### Veranstaltung bearbeiten

![Veranstaltung bearbeiten](img/mockup/App/Veranstaltung bearbeiten.png)

##### Abstimmung ansehen

![Abstimmung](img/mockup/App/Veranstaltung Abstimmung ansehen.png)

##### Abstimmung erstellen

![Abstimmung erstellen](img/mockup/App/Veranstaltung Abstimmung erstellen.png)