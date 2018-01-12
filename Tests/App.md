## Clients

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

### Benutzerprofil verwalten/ändern

| Testart | Ereignis | Überprüfung | Ergebnis | Testname |
| ------- | -------- | ----------- | -------- | -------- |
| Positiv | Korrekte Daten eingegeben | API antwortet mit Status 200 | Aktualisiertes Benutzerprofil | Aenderung_Positiv  |
| Negativ | Geburtsdatum liegt in der Zukunft | Überprüfen ob Geburtsdatum nicht in der Zukunft liegt | Fehlermeldung anzeigen | | Aenderung__Negativ_Geburtsdatum_1 |
| Negativ | Aktuelles Kennwort zu kurz | Länge von Kennwort prüfen | Fehlermeldung anzeigen | Aenderung_PruefAktPw_Negativ_Password_1  |
| Negativ | Aktuelles Kennwort leer | Überprüfen ob Passwort nicht leer ist | Fehlermeldung anzeigen | Aenderung_PruefAktPw_Negativ_Password_2 |
| Negativ | Aktuelles Kennwort falsch | Überprüfen ob Passwort nicht korrekt ist | Fehlermeldung anzeigen | Aenderung_PruefAktPw_Negativ_Password_3 |
| Negativ | Neues Kennwort zu kurz | Länge von Kennwort prüfen  | Fehlermeldung anzeigen  | Aenderung_Negativ_Password_1  |
| Negativ | Neues Kennwort leer | Überprüfen ob Passwort nicht leer ist  | Fehlermeldung anzeigen  | Aenderung_Negativ_Password_2  |
| Negativ | Passwort-Überprüfen-Feld leer | Überprüfen ob Passwort-Überprüfen-Feld nicht leer ist | Fehlermeldung anzeigen | Aenderung_Negativ_Password_Check_1 |
| Negativ | Passwort-Überprüfen-Feld zu kurz | Länge von Passwort-Überprüfen-Feld prüfen | Fehlermeldung anzeigen | Aenderung_Negativ_Password_Check_2 |
| Negativ | Passwort stimmt nicht mit Passwort-Überprüfen-Feld überein | Überprüfen ob Passwort und Passwort-Überprüfen-Feld übereinstimmen | Fehlermeldung anzeigen  | Aenderung_Negativ_Password_Check_3 |
| I/O     | API nicht erreichbar  | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen  | Aenderung_IO_API_1    |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus  | Fehlermeldung anzeigen | Aenderung_IO_API_2            |
| I/O     | Antwort-JSON ist fehlerhaft  | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen  | Aenderung_IO_API_3    |
