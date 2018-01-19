Clients

## Grundfunktionen

### Einloggen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                     | Testname                  |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------- | ------------------------- |
| Positiv | Korrekte Daten eingegeben                | API antwortet mit Status 200 und API-Key | Weiterleitung zur Hauptseite | Login_Positiv             |
| Negativ | E-Mail ungültig                          | Überprüfen ob @ und . enthalten sind     | Fehlermeldung anzeigen       | Login_Negativ_Email_1     |
| Negativ | E-Mail leer                              | Überprüfen ob E-Mail nicht leer ist      | Fehlermeldung anzeigen       | Login_Negativ_Email_2     |
| Negativ | Kennwort zu kurz                         | Länge von Kennwort prüfen                | Fehlermeldung anzeigen       | Login_Negativ_Password_1  |
| Negativ | Kennwort leer                            | Überprüfen ob Passwort nicht leer ist    | Fehlermeldung anzeigen       | Login_Negativ_Password_2  |
| Negativ | Kombination stimmt nicht                 | API antwortet mit Status 400             | Fehlermeldung anzeigen       | Login_Negativ_Combination |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen       | Login_IO_API_1            |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen       | Login_IO_API_2            |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen       | Login_IO_API_3            |

### Ausloggen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                     | Testname        |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------- | --------------- |
| Positiv | User war angemeldet                      | API antwortet mit Status 200             | Weiterleitung zur Startseite | Logout_Positiv  |
| Negativ | User war nicht angemeldet                | API antwortet mit Status 400             | Fehlermeldung anzeigen       | Logout_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen       | Logout_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen       | Logout_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit Status 200 noch mit Status 400 | Fehlermeldung anzeigen       | Logout_IO_API_3 |

### Registrieren

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                | Testname                          |
| ------- | ---------------------------------------- | ---------------------------------------- | ----------------------- | --------------------------------- |
| Positiv | Alle Daten sind korrekt                  | API antwortet mit Status 200             | Weiterleitung zum Login | Register_Positiv                  |
| Negativ | E-Mail ungültig                          | Überprüfen ob @ und . enthalten sind     | Fehlermeldung anzeigen  | Register_Negativ_Email_1          |
| Negativ | E-Mail leer                              | Überprüfen ob E-Mail nicht leer ist      | Fehlermeldung anzeigen  | Register_Negativ_Email_2          |
| Negativ | E-Mail schon vorhanden                   | API antwortet mit Status 400 und enstprechender Fehlermeldung | Fehlermeldung anzeigen  | Register_Negativ_Email_3          |
| Negativ | Passwort zu kurz                         | Länge von Passwort prüfen                | Fehlermeldung anzeigen  | Register_Negativ_Password_1       |
| Negativ | Passwort leer                            | Überprüfen ob Passwort nicht leer ist    | Fehlermeldung anzeigen  | Register_Negativ_Password_2       |
| Negativ | Passwort-Überprüfen-Feld leer            | Überprüfen ob Passwort-Überprüfen-Feld nicht leer ist | Fehlermeldung anzeigen  | Register_Negativ_Password_Check_1 |
| Negativ | Passwort-Überprüfen-Feld zu kurz         | Länge von Passwort-Überprüfen-Feld prüfen | Fehlermeldung anzeigen  | Register_Negativ_Password_Check_2 |
| Negativ | Passwort stimmt nicht mit Passwort-Überprüfen-Feld überein | Überprüfen ob Passwort und Passwort-Überprüfen-Feld übereinstimmen | Fehlermeldung anzeigen  | Register_Negativ_Password_Check_3 |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen  | Register_IO_API_1                 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen  | Register_IO_API_2                 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit Status 200 noch mit Status 400 | Fehlermeldung anzeigen  | Register_IO_API_3                 |

## Benutzer

### Benutzerprofil verwalten/ändern

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                      | Testname                                |
| ------- | ---------------------------------------- | ---------------------------------------- | ----------------------------- | --------------------------------------- |
| Positiv | Korrekte Daten eingegeben                | API antwortet mit Status 200             | Aktualisiertes Benutzerprofil | Aenderung_Positiv                       |
| Negativ | Geburtsdatum liegt in der Zukunft        | Überprüfen ob Geburtsdatum nicht in der Zukunft liegt | Fehlermeldung anzeigen        | Aenderung_Negativ_Geburtsdatum_1        |
| Negativ | Aktuelles Kennwort zu kurz               | Länge von Kennwort prüfen                | Fehlermeldung anzeigen        | Aenderung_PruefAktPw_Negativ_Password_1 |
| Negativ | Aktuelles Kennwort leer                  | Überprüfen ob Passwort nicht leer ist    | Fehlermeldung anzeigen        | Aenderung_PruefAktPw_Negativ_Password_2 |
| Negativ | Aktuelles Kennwort falsch                | Überprüfen ob Passwort nicht korrekt ist | Fehlermeldung anzeigen        | Aenderung_PruefAktPw_Negativ_Password_3 |
| Negativ | Neues Kennwort zu kurz                   | Länge von Kennwort prüfen                | Fehlermeldung anzeigen        | Aenderung_Negativ_Password_1            |
| Negativ | Neues Kennwort leer                      | Überprüfen ob Passwort nicht leer ist    | Fehlermeldung anzeigen        | Aenderung_Negativ_Password_2            |
| Negativ | Passwort-Überprüfen-Feld leer            | Überprüfen ob Passwort-Überprüfen-Feld nicht leer ist | Fehlermeldung anzeigen        | Aenderung_Negativ_Password_Check_1      |
| Negativ | Passwort-Überprüfen-Feld zu kurz         | Länge von Passwort-Überprüfen-Feld prüfen | Fehlermeldung anzeigen        | Aenderung_Negativ_Password_Check_2      |
| Negativ | Passwort stimmt nicht mit Passwort-Überprüfen-Feld überein | Überprüfen ob Passwort und Passwort-Überprüfen-Feld übereinstimmen | Fehlermeldung anzeigen        | Aenderung_Negativ_Password_Check_3      |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen        | Aenderung_IO_API_1                      |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen        | Aenderung_IO_API_2                      |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen        | Aenderung_IO_API_3                      |

### Benutzerprofil löschen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                | Testname            |
| ------- | ---------------------------------------- | ---------------------------------------- | --------------------------------------- | ------------------- |
| Positiv | Löschen des Benutzers doppelt bestätigt, Löschen erfolgreich | API antwortet mit Status 200             | Ausloggen, Weiterleitung zur Hauptseite | DeleteUser_Positiv  |
| Negativ | Fehler beim Löschen des Users            | API antwortet mit Status 400             | Fehlermeldung anzeigen                  | DeleteUser_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                  | DeleteUser_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                  | DeleteUser_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                  | DeleteUser_IO_API_3 |

## Veranstaltung

### Alle Veranstaltungen anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                      | Testname            |
| ------- | ---------------------------------------- | ---------------------------------------- | ----------------------------- | ------------------- |
| Positiv | Veranstaltungen werden korrekt angezeigt | API antwortet mit Status 200             | Übersicht der Veranstaltungen | ShowEvents_Positiv  |
| Negativ | Fehler beim anzeigen der Veranstaltungen | API antwortet mit Status 400             | Fehlermeldung anzeigen        | ShowEvents_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen        | ShowEvents_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen        | ShowEvents_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen        | ShowEvents_IO_API_3 |

### Meine erstellten Veranstaltungen anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                              | Testname               |
| ------- | ---------------------------------------- | ---------------------------------------- | ------------------------------------- | ---------------------- |
| Positiv | Eigene Veranstaltungen werden korrekt angezeigt | API antwortet mit Status 200             | Übersicht der eigenen Veranstaltungen | ShowOwnEvents_Positiv  |
| Negativ | Fehler beim anzeigen der eigenen Veranstaltungen | API antwortet mit Status 400             | Fehlermeldung anzeigen                | ShowOwnEvents_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                | ShowOwnEvents_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                | ShowOwnEvents_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                | ShowOwnEvents_IO_API_3 |

###  Veranstaltung erstellen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Veranstaltung wird erfolgreich erstellt  | API antwortet mit Status 200  | Übersicht der Veranstaltung wird angezeigt| createEvent_Positiv   |
| Negativ | Wichtige Daten fehlen  | Benötigte Felder sind leer | Fehlermeldung anzeigen | createEvent_Negativ_1 |
| Negativ | Ungültige Daten angegeben | Felder werden auf Gültigkeit überprüft | Fehlermeldung anzeigen | createEvent_Negativ_2   |
| I/O     | API nicht erreichbar | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | createEvent_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus | Fehlermeldung anzeigen | createEvent_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | createEvent_IO_API_3  |

###  Veranstaltung verwalten

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Veranstaltung erfolgreich geändert | API antwortet mit Status 200 | Übersicht der Veranstaltung wird angezeigt| changeEvent_Positiv   |
| Negativ | Wichtige Daten fehlen  | Benötigte Felder sind leer | Fehlermeldung anzeigen | changeEvent_Negativ_1 |
| Negativ | Ungültige Daten angegeben | Felder werden auf Gültigkeit überprüft | Fehlermeldung anzeigen | changeEvent_Negativ_2   |
| Negativ | Fehler beim ändern der Daten | API antwortet mit Status 400 | Fehlermeldung anzeigen | changeEvent_Negativ_3 |
| I/O     | API nicht erreichbar | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | changeEvent_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus | Fehlermeldung anzeigen | changeEvent_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | changeEvent_IO_API_3  |

###  Veranstaltung anzeigen Organisator

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Veranstaltung wird korrekt angezeigt | API antwortet mit Status 200  | Übersicht der Veranstaltung wird angezeigt| showEventOrganizer_Positiv   |
| Negativ | Veranstaltung kann nicht angezeigt werden | API antwortet mit Status 400 | Fehlermeldung anzeigen | showEventOrganizer_Negativ |
| I/O     | API nicht erreichbar | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | showEventOrganizer_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus | Fehlermeldung anzeigen | showEventOrganizer_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | showEventOrganizer_IO_API_3  |

###  Veranstaltung anzeigen User

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Veranstaltung wird korrekt angezeigt | API antwortet mit Status 200  | Übersicht der Veranstaltung wird angezeigt| showEventUser_Positiv   |
| Negativ | Veranstaltung kann nicht angezeigt werden | API antwortet mit Status 400 | Fehlermeldung anzeigen | showEventUser_Negativ |
| I/O     | API nicht erreichbar | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | showEventOrganizer_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus | Fehlermeldung anzeigen | showEventUser_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen | showEventUser_IO_API_3  |

## Kontaktliste

### Profil suchen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                              | Testname                      |
| ------- | ---------------------------------------- | ---------------------------------------- | ------------------------------------- | ----------------------------- |
| Positiv | Gefunden User werden korrekt angezeigt   | API antwortet mit Status 200             | Übersicht aller gefunden User         | SearchUser_Positiv            |
| Positiv | User nicht gefunden                      |                                          | Anzeige "User nicht vorhanden"        | SearchNonExcitingUser_Positiv |
| Negativ | Fehler beim anzeigen der gesuchten User  | API antwortet mit Status 400             | Fehlermeldung anzeigen gesuchter User | SearchUser_Negativ            |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                | SearchUser_IO_API_1           |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                | SearchUser_IO_API_2           |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                | SearchUser_IO_API_3           |

### Meine Kontakte anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                            | Testname              |
| ------- | ---------------------------------------- | ---------------------------------------- | ----------------------------------- | --------------------- |
| Positiv | Kontakte korrekt anzeigen                | API antwortet mit Status 200             | Übersicht Kontakte                  | ShowContact_Positiv   |
| Positiv | Keine Kontakte vorhanden                 |                                          | Anzeigen leerer Kontaktliste        | ShowNoContact_Positiv |
| Negativ | Fehler beim anzeigen der Kontakte        | API antwortet mit Status 400             | Fehlermeldung anzeigen Kontaktliste | ShowContact_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen              | ShowContact_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen              | ShowContact_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen              | ShowContact_IO_API_3  |



### Profil als Kontakt hinzufügen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                              | Testname                  |
| ------- | ---------------------------------------- | ---------------------------------------- | ------------------------------------- | ------------------------- |
| Positiv | Kontakt hinzufügen                       | API antwortet mit Status 200             | Kontakt zur liste hinzufügen          | AddContact_Positiv        |
| Negativ | Kontakt geblockt                         |                                          | Kontakt nicht zur liste hinzufügen    | AddBlockedContact_Negativ |
| Negativ | Fehler beim hinzufügen des Kontaktes     | API antwortet mit Status 400             | Fehlermeldung hinzufügen Kontaktliste | AddContact_Negativ        |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                | AddContact_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                | AddContact_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                | AddContact_IO_API_3       |

### Profil als Kontakt entfernen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                               | Testname                 |
| ------- | ---------------------------------------- | ---------------------------------------- | -------------------------------------- | ------------------------ |
| Positiv | Kontakt entferenen                       | API antwortet mit Status 200             | Kontakt von der  liste entferenen      | RemoveContact_Positiv    |
| Negativ | Kontakt nicht befreundet                 |                                          | Kontakt kann nicht entfernt werden     | RemoveNonContact_Negativ |
| Negativ | Fehler beim entfernen des Kontaktes      | API antwortet mit Status 400             | Fehlermeldung entferenen des Kontaktes | RemoveContact_Negativ    |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                 | RemoveContact_IO_API_1   |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                 | RemoveContact_IO_API_2   |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                 | RemoveContact_IO_API_3   |

## Gästeliste

### Einladungen anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Einladungen anzeigen                     | API antwortet mit Status 200             | Einladungsliste anzeigen           | showInvite_Positiv   |
| Negativ | Keine Einladungen                        |                                          | Leere Einladungsliste anzeigen     | showNoInvite_Negativ |
| Negativ | Fehler beim anzeigen der Einladungen     | API antwortet mit Status 400             | Fehlermeldung anzeigen Einladungen | showInvite_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen             | showInvite_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen             | showInvite_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | showInvite_IO_API_3  |

### Einladen via Profil

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis               | Testname                     |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------- | ---------------------------- |
| Positiv | Einladen funktioniert                    | API antwortet mit Status 200             | Bestätigung            | inviteProfile_Positiv        |
| Negativ | Einladen schlägt fehl                    | API antwortet mit Status 400             | Fehlermeldung anzeigen | inviteProfile_Negativ        |
| Negativ | User existiert nicht                     | API antwortet mit Status 400             | Fehlermeldung anzeigen | inviteProfile_NoUser_Negativ |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | inviteProfile_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen | inviteProfile_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen | inviteProfile_IO_API_3       |

### Gästeliste anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                          | Testname                |
| ------- | ---------------------------------------- | ---------------------------------------- | --------------------------------- | ----------------------- |
| Positiv | Gästeliste anzeigen                      | API antwortet mit Status 200             | Gästeliste anzeigen               | showGuestList_Positiv   |
| Negativ | Keine Gästeliste                         |                                          | Leere Gästeliste anzeigen         | showNoGuestList_Negativ |
| Negativ | Fehler beim anzeigen der Gästeliste      | API antwortet mit Status 400             | Fehlermeldung anzeigen Gästeliste | showGuestList_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen            | showGuestList_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen            | showGuestList_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen            | showGuestList_IO_API_3  |

### Zusagen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname               |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------- |
| Positiv | Einladung annehmen                       | API antwortet mit Status 200             | Zur Gästeliste hinzufügen, Einladung entfernenen | sayYes_Positiv         |
| Negativ | Keine Einladung bekommen                 | API antwortet mit Status 200             | Nicht zur Gästeliste hinzufügen          | sayYesNoInvite_Negativ |
| Negativ | Fehler beim annehmen der Einladung       | API antwortet mit Status 400             | Fehlermeldung Einladung annehmen         | sayYes_Negativ         |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | sayYes_IO_API_1        |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | sayYes_IO_API_2        |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | sayYes_IO_API_3        |

### Absagen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                         | Testname              |
| ------- | ---------------------------------------- | ---------------------------------------- | -------------------------------- | --------------------- |
| Positiv | Einladung ablehnen                       | API antwortet mit Status 200             | Einladung entfernen              | sayNo_Positiv         |
| Negativ | Keine Einladung bekommen                 |                                          | Einladung entfernen              | sayNoNoInvite_Negativ |
| Negativ | Fehler beim ablehnen der Einladung       | API antwortet mit Status 400             | Fehlermeldung Einladung ablehnen | sayNo_Negativ         |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen           | sayNo_IO_API_1        |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen           | sayNo_IO_API_2        |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen           | sayNo_IO_API_3        |

## Aufgaben

### Aufgabe Anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                        | Testname                |
| ------- | ---------------------------------------- | ---------------------------------------- | ------------------------------- | ----------------------- |
| Positiv | Aufgaben anzeigen                        | API antwortet mit Status 200             | Aufgabenliste  anzeigen         | showTasks_Positiv       |
| Positiv | Keine Aufgaben                           |                                          | Leere Aufgabeliste anzeigen     | showTasksNoTask_Positiv |
| Negativ | Fehler beim anzeigen der Aufgaben        | API antwortet mit Status 400             | Fehlermeldung Aufgaben anzeigen | showTasks_Negativ       |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen          | showTasks_IO_API_1      |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen          | showTasks_IO_API_2      |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen          | showTasks_IO_API_3      |

### Aufgabe verwalten

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                  | Testname                         |
| ------- | ---------------------------------------- | ---------------------------------------- | ------------------------- | -------------------------------- |
| Positiv | Aufgaben verwaltbar (enfernen/hinzufuegen/bearbeiten) | API antwortet mit Status 200             | Aufgabenliste  verwaltbar | verwalteTasks_Positiv            |
| Negativ | Aufgabe kann nicht entfernt werden       | API antwortet mit Status 400             | Fehlermeldung anzeigen    | verwalteTasksEntfernen_Negativ   |
| Negativ | Aufgabe kann nicht angelegt werden       | API antwortet mit Status 400             | Fehlermeldung anzeigen    | verwalteTasksHinzufuegen_Negativ |
| Negativ | Aufgabe kann nicht bearbeitet werden     | API antwortet mit Status 400             | Fehlermeldung anzeigen    | verwalteTasksBearbeiten_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen    | verwalteTasks_IO_API_1           |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen    | verwalteTasks_IO_API_2           |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen    | verwalteTasks_IO_API_3           |

## Bewertung

###  Bewertung abgeben

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname                 |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ------------------------ |
| Positiv | Bewertung abgeben                        | API antwortet mit Status 200             | Bewertung abgeben                        | setRating_Positiv        |
| Negativ | Negative Bewertung abgeben               |                                          | Fehlermeldung Negative Bewertung nicht möglich | setNegativRating_Negativ |
| Negativ | Fehler beim abgegeben einer Bewertung    | API antwortet mit Status 400             | Fehlermeldung abgeben Bewertung          | setRating_Negativ        |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | setRating_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | setRating_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | setRating_IO_API_3       |

### Berwertung ändern

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname                    |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | --------------------------- |
| Positiv | Bewertung ändern                         | API antwortet mit Status 200             | Bewertung ändern                         | changeRating_Positiv        |
| Negativ | Bewertung auf Negativ ändern             |                                          | Fehlermeldung Negative Bewertung nicht möglich | changeNegativRating_Negativ |
| Negativ | Fehler beim ändern einer Bewertung       | API antwortet mit Status 400             | Fehlermeldung ändern Bewertung           | changeRating_Negativ        |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | changeRating_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | changeRating_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | changeRating_IO_API_3       |

###  Bewertung Anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Bewertung anzeigen                       | API antwortet mit Status 200             | Bewertung anzeigen                 | showRating_Positiv   |
| Negativ | Keine Bewertungen abgeben                |                                          | Anzeigen Keiner Bewertungen (0?)   | showNoRating_Negativ |
| Negativ | Fehler beim anzeigen der Bewertung       | API antwortet mit Status 400             | Fehlermeldung anzeigen Bewertungen | showRating_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen             | showRating_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen             | showRating_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | showRating_IO_API_3  |

## Galerie

### Foto anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis               | Testname                   |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------- | -------------------------- |
| Positiv | Foto kann geladen werden                 | API antwortet mit Status 200 und Bild    | Foto wird angezeigt    | showPhoto_Positiv          |
| Negativ | Foto kann nicht geladen werden           | API antwortet mit Status 400             | Fehlermeldung anzeigen | showPhoto_Negativ          |
| Negativ | Datei ist fehlerhaft übertragen          | Überprüfen ob Datei komplett ist         | Fehlermeldung anzeigen | showPhoto_Transfer_Negativ |
| Negativ | Datei ist zu groß                        | Überprüfen der Dateigröße                | Fehlermeldung anzeigen | showPhoto_Size_Negativ     |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | showPhoto_IO_API_1         |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen | showPhoto_IO_API_2         |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen | showPhoto_IO_API_3         |

### Foto hochladen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis               | Testname                   |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------- | -------------------------- |
| Positiv | Foto wird hochgeladen                    | API antwortet mit Status 200             | Bestätigung            | uploadPhoto_Positiv        |
| Negativ | Foto kann nicht hochgeladen werden       | API antwortet mit Status 400             | Fehlermeldung anzeigen | uploadPhoto_Negativ        |
| Negativ | Datei existiert nicht                    | Überprüfen ob Datei existiert            | Fehlermeldung anzeigen | uploadPhoto_Exists_Negativ |
| Negativ | Datei ist zu groß                        | Überprüfen der Dateigröße                | Fehlermeldung anzeigen | uploadPhoto_Size_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | uploadPhoto_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen | uploadPhoto_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen | uploadPhoto_IO_API_3       |

## Kommentar

###  Kommentar erstellen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname                 |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ------------------------ |
| Positiv | Kommentar erstellen                      | API antwortet mit Status 200             | Kommentar erstellt                       | addComment_Positiv        |
| Negativ | Fehler beim erstellen eines Kommentars   | API antwortet mit Status 400             | Fehlermeldung erstellen Kommentar        | addComment_Negativ        |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | createComment_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | createComment_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | createComment_IO_API_3       |

### Kommentar ändern

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname                    |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | --------------------------- |
| Positiv | Kommentar ändern                         | API antwortet mit Status 200             | Kommentar ändern                         | changeComment_Positiv        |
| Negativ | Fehler beim ändern eines Kommentars      | API antwortet mit Status 400             | Fehlermeldung ändern Kommentar           | changeComment_Negativ        |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | changeComment_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | changeComment_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | changeComment_IO_API_3       |

###  Kommentar Anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Kommentar anzeigen                       | API antwortet mit Status 200             | Kommentar anzeigen                 | showComment_Positiv   |
| Negativ | Keine Kommentare vorhanden               |                                          | Anzeigen Kein Kommentar            | showNoComment_Negativ |
| Negativ | Fehler beim anzeigen eines Kommentars    | API antwortet mit Status 400             | Fehlermeldung anzeigen Kommentar   | showComment_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen             | showComment_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen             | showComment_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | showComment_IO_API_3  |

### Kommentar löschen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                | Testname            |
| ------- | ---------------------------------------- | ---------------------------------------- | --------------------------------------- | ------------------- |
| Positiv | Löschen des Kommentars                   | API antwortet mit Status 200             | Kommentar gelöscht                      | DeleteComment_Positiv  |
| Negativ | Fehler beim Löschen des Kommentars       | API antwortet mit Status 400             | Fehlermeldung anzeigen                  | DeleteComment_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                  | DeleteComment_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                  | DeleteComment_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                  | DeleteComment_IO_API_3 |

## Antwort

###  Antwort erstellen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname                 |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ------------------------ |
| Positiv | Antwort erstellen                        | API antwortet mit Status 200             | Antwort erstellt                         | addResponse_Positiv        |
| Negativ | Fehler beim erstellen einer Antwort      | API antwortet mit Status 400             | Fehlermeldung erstellen Antwort          | addResponse_Negativ        |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | createResponse_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | createResponse_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | createResponse_IO_API_3       |

### Antwort ändern

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                 | Testname                    |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | --------------------------- |
| Positiv | Antwort ändern                           | API antwortet mit Status 200             | Anwort geändert                          | changeResponse_Positiv      |
| Negativ | Fehler beim ändern einer Antwort         | API antwortet mit Status 400             | Fehlermeldung ändern Antwort           | changeResponse_Negativ      |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                   | changeResponse_IO_API_1       |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                   | changeResponse_IO_API_2       |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                   | changeResponse_IO_API_3       |

###  Antwort Anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Antwort anzeigen                         | API antwortet mit Status 200             | Antwort anzeigen                   | showResponse_Positiv   |
| Negativ | Keine Antworten vorhanden                |                                          | Anzeigen Keine Antwort             | showNoResponse_Negativ |
| Negativ | Fehler beim anzeigen einer Antwort       | API antwortet mit Status 400             | Fehlermeldung anzeigen Antwort     | showResponse_Negativ   |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen             | showResponse_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen             | showResponse_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | showResponse_IO_API_3  |

### Antwort löschen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                                | Testname            |
| ------- | ---------------------------------------- | ---------------------------------------- | --------------------------------------- | ------------------- |
| Positiv | Löschen der Antwort                      | API antwortet mit Status 200             | Antwort gelöscht                        | DeleteResponse_Positiv  |
| Negativ | Fehler beim Löschen der Antwort          | API antwortet mit Status 400             | Fehlermeldung anzeigen                  | DeleteResponse_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen                  | DeleteResponse_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen                  | DeleteResponse_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen                  | DeleteResponse_IO_API_3 |

### ToDo-Liste anzeigen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                        | Testname          |
| ------- | ---------------------------------------- | ---------------------------------------- | ------------------------------- | ----------------- |
| Positiv | ToDo-Liste anzeigen                      | API antwortet mit Status 200             | ToDo-Liste  anzeigbar           | showToDo_Positiv  |
| Negativ | Fehler beim anzeigen der ToDo-Liste      | API antwortet mit Status 400             | Fehlermeldung Aufgaben anzeigen | showToDo_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen          | showToDo_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen          | showToDo_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen          | showToDo_IO_API_3 |

### ToDo-Liste verwalten

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis               | Testname                        |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------- | ------------------------------- |
| Positiv | ToDo-Liste verwaltbar (enfernen/hinzufuegen/bearbeiten) | API antwortet mit Status 200             | ToDo-Liste  verwaltbar | verwalteToDo_Positiv            |
| Negativ | ToDo kann nicht entfernt werden          | API antwortet mit Status 400             | Fehlermeldung anzeigen | verwalteToDoEntfernen_Negativ   |
| Negativ | ToDo kann nicht angelegt werden          | API antwortet mit Status 400             | Fehlermeldung anzeigen | verwalteToDoHinzufuegen_Negativ |
| Negativ | ToDo kann nichtt bearbeitet werden       | API antwortet mit Status 400             | Fehlermeldung anzeigen | verwalteToDoBearbeiten_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | verwalteToDo_IO_API_1           |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen | verwalteToDo_IO_API_2           |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen | verwalteToDo_IO_API_3           |

