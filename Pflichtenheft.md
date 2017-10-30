# Pflichtenheft

## Funktionale Anforderungen

### Grundfunktionen

- Einloggen
- "Passwort vergessen"-Funktion
- Ausloggen
- Impressum anzeigen
- Hilfeseite anzeigen

#### Kontaktformular

- Kontaktformular anzeigen
- Kontaktformular absenden

#### Benutzerverwaltung

- Benutzer erstellen
- E-Mail validieren
- Benutzerprofil verwalten/ändern
- Benutzerprofil löschen

#### Push-Nachrichten

- Push-Nachrichten automatisch versenden

### Veranstaltung

#### Allgemein

- Veranstaltung erstellen
- Veranstaltung verwalten
- Berechtigungen verwalten
- Veranstaltung ändern
- Veranstaltung anzeigen (Gast, Registriert, Organisator)

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

- Galerieübersicht (alle verfügbaren Galerien) anzeigen
- Startseite (einer bestimmten Galerie) anzeigen
- Fotos hochladen
- Fotos herunterladen
- Fotos anzeigen
- (Fotos kommentieren?)

#### Kommunikation

- Kommentar erstellen 
- Kommentar bearbeiten
- Kommentar löschen

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


## Nicht-Funktionale Anforderungen

### Server

### Datenbank

### App

### Webanwendung

## Systemarchitekturdiagramm

## Mock-Ups




## Must Have's

### Infrastruktur

#### Webanwendung

Die Anwendung soll von den gängigen Browsern korrekt dargestellt werden.  Design und Bedienung der Website entsprechen den aktuellen Technologien und sind intuitiv. Die Webanwendung ist für mobile Geräte optimiert.

#### App

Eine native Lösung für Android und iOS soll angeboten werden. Design und Bedienung sollen dabei ebenfalls zeitgemäß und den Technologien angepasst sein.

#### Datenbank

Die Verwaltung der Daten soll ein entsprechendes Datenbankmanagmentsystem übernehmen. Es muss ausreichend dimensioniert sein, damit ausreichend Daten gespeichert werden können, sowie das Abrufen und Schreiben von Daten zügig erfolgt.

#### Server

Die Hauptanwendung soll auf einem Server laufen. Auch der Server muss ausreichend Ressourcen bereitstellen, damit ein Betrieb von mehreren Clients  gleichzeitig möglich wird.

### Funktionen

#### Benutzersystem

Es soll zwei Möglichkeiten geben sich an dem System anzumelden. Einmal als registrierter Benutzer und einmal als Gast. Als registrierter Benutzer erhält man ein Benutzerprofil, über das man seine persönlichen Daten verwalten kann. Hierzu zählen Name,Adresse,Foto,vergangene Veranstaltungen, zukünftige Veranstaltungen... Als Gast hat man nur Zugriff auf eine Veranstaltung, muss dafür aber auch nur einen Namen angeben.

#### Rollen- / Rechtesystem

Der Organisator kann noch weiter User zu Organisatoren machen. Diese haben dann die gleichen Rechte.

#### Planungssystem

##### ToDo-Liste

Der Organisator kann eine ToDo-Liste anlegen, damit er die Party planen kann.

##### Kostenübersicht

Es können Ausnahmen und Einnahmen protokolliert werden. Diese können in Übersichten eingesehen werden. Die verschiedenen Ein- / Ausgaben werden am Ende der Übersicht zusammengerechnet. Auch steht eine Gesamtübersicht zur Verfügung.

#### Veranstaltung

Auf der Hauptseite der Veranstaltung müssen alle relevanten Informationen zur Verfügung stehen.

##### Name

Der Name der Veranstaltung.

##### Beschreibung

Der Organisator kann einen Beschreibungstext zu seiner Veranstaltung eingeben.

##### Gastgeber / Ansprechpartner

Der Gastgeber, bzw. die Ansprechpartner, sind zentral einsehbar.

##### Ort

Ort der Veranstaltung. Hier muss nicht zwingend eine gültige Adresse eingegeben werden, damit auch benutzereigene Beschreibungen möglich sind. Wenn eine gültige Adresse eingegeben wurde, muss diese von Google Maps (Web, Android) oder Maps(iOS) verarbeitet werden können.

##### Zeitpunkt

Datum und Uhrzeit der Veranstaltung. Es muss eine Verbindung zu den Systemkalendern (Android,iOS) bestehen, damit der Termin direkt übertragen werden kann. Auch sollten die Termine in einer Übersicht im Benutzerprofil angezeigt werden (Kalenderwidget).

##### Galerie

Hier können je nach Wunsch Medien hoch- oder runtergeladen werden.

##### Aufgaben

Liste mit Aufgaben, die noch erledigt werden müssen. Mit dieser Funktion sollen zum Beispiel Mitbring-Buffets organisiert werden. Die Aufgaben können vom Organisator zugeteilt oder freiwillig von einem Gast übernommen werden.

##### Kommunikation

In der Veranstaltung können Beiträge geschrieben und kommentiert werden.

##### Zu- / Absagen

Gäste können selbständig zu- oder absagen. 

##### Einladungen

Einladungen können sowohl über QR-Code, als auch über Link versendet werden. Die Einladungen können in Zeit und Menge beschränkt werden.

##### Gästeliste

Gäste können  die aktuelle Gästeliste einsehen.

##### Planungsystem -><- Veranstaltung

Es besteht die Möglichkeit, aus der Planungsübersicht Inhalte für die Veranstaltung zu erstellen.

## Optional

### Infrastruktur

#### App

Die Apps werden zusätzlich noch für Tablets optimiert.

### Funktionen

##### Kommunikation

Es können Gruppenchats innerhalb einer Veranstaltung erstellt werden. Auch können Mitglieder andere Mitglieder in Gruppenchats oder Beiträgen verlinken. Auch die Möglichkeit eines Privatchats wird angeboten.

##### Einchecken

Gäste können bei der Veranstaltung über das Einscannen eines QR-Codes einchecken. So kann man gucken, wer alles da ist, bzw. war, und wer noch erwartet wird.

##### Bewertung

Die Veranstaltung kann im Nachhinein von den Gästen bewertet werden. Hierfür kann entweder die Standardvorlage benutzt werden oder der Gastgeber kann eine eigene Umfrage erstellen.

##### Abstimmungen

In der Veranstaltung können Abstimmungen durchgeführt werden.

##### Social-Network

Es kann sich mit Social-Media-Plattformen verbunden werden.

##### Galerie

Medien können kommentiert werden. Die Medien können auf Social-Media-Plattformen geteilt werden.

##### Benachrichtigungssystem / Mail

User erhalten entweder per Mail oder Push-Nachricht Erinnerungen zu der Veranstaltung.