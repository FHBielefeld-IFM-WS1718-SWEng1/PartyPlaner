## Clients

## Grundfunktionen

### Einloggen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                     | Testname                  |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------- | ------------------------- |
| Positiv | Korrekte Daten eingegeben                | API antwortet mit Status 200 und API-Key | Weiterleitung zur Hauptseite | Login_Positiv             |
| Negativ | E-Mail ungültig                          | Überprüfen ob @ und . enthalten sind     | Fehlermeldung anzeigen       | Login_Negativ_Email_1     |
| Negativ | E-Mail leer                              | Überprüfen ob E-Mail nicht leer ist      | Fehlermeldung anzeigen       | Login_Negativ_Email_2     |
| Negativ | Kennwort zu kurz                         | Länge prüfen                             | Fehlermeldung anzeigen       | Login_Negativ_Password_1  |
| Negativ | Kennwort leer                            | Überprüfen ob Passwort nicht leer ist    | Fehlermeldung anzeigen       | Login_Negativ_Password_2  |
| Negativ | Kombination stimmt nicht                 | API antwortet mit Status 400             | Fehlermeldung anzeigen       | Login_Negativ_Combination |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen       | Login_IO_API_1            |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen       | Login_IO_API_2            |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen       | Login_IO_API_3            |

### Ausloggen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                     | Testname        |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------- | --------------- |
| Positiv | User war angemeldet                      | API antwortet mit Status 200             | Weiterleitung zur Startseite | Logout_Positiv  |
| Negativ | Kombination stimmt nicht                 | API antwortet mit Status 400             | Fehlermeldung anzeigen       | Logout_Negativ  |
| I/O     | API nicht erreichbar                     | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen       | Logout_IO_API_1 |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus                    | Fehlermeldung anzeigen       | Logout_IO_API_2 |
| I/O     | Antwort-JSON ist fehlerhaft              | API antwortet weder mit Status 200 noch mit Status 400 | Fehlermeldung anzeigen       | Logout_IO_API_3 |