## Clients

### Grundfunktionen

#### Einloggen

| Testart | Ereignis                    | Überprüfung                              | Ergebnis                     | Testname                 |
| ------- | --------------------------- | ---------------------------------------- | ---------------------------- | ------------------------ |
| Negativ | E-Mail ohne @               | Überprüfen ob @ enthalten ist            | Fehlermeldung anzeigen       | Login_Negativ_Email_1    |
| Negativ | Kennwort zu kurz            | Länge prüfen                             | Fehlermeldung anzeigen       | Login_Negativ_Password_1 |
| Negativ | Beides falsch eingegeben    | API antwortet mit Status 400             | Fehlermeldung anzeigen       | Login_Negativ_All        |
| Positiv | Korrekte Daten eingegeben   | API antwortet mit Status 200 und API-Key | Weiterleitung zur Hauptseite | Login_Positiv            |
| I/O     | API nicht erreichbar        | Timeout bei Warten auf Antwort der API   | Fehlermeldung anzeigen       | Login_IO_API_1           |
| I/O     | Antwort-JSON ist fehlerhaft | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen       | Login_IO_API_2           |