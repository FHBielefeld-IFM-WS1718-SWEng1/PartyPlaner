## API

### Login

| Testart | Ereignis                                 | Überprüfung                           | Ergebnis   | Testname                |
| ------- | ---------------------------------------- | ------------------------------------- | ---------- | ----------------------- |
| Positiv | Request entspricht der Dokumentation, Daten stimmen überein | Passwort passt zur E-Mail             | Status 200 | Login_Positiv_Correct   |
| Positiv | E-Mail existiert nicht                   | E-Mail steht nicht in DB              | Status 400 | Login_Positiv_NoEmail   |
| Positiv | Daten stimmen nicht überein              | Passwort passt nicht zur E-Mail       | Status 400 | Login_Positiv_          |
| Negativ | Request entspricht nicht der Dokumentation |                                       | Status 400 | Login_Negativ_Request_1 |
| I/O     | DB nicht erreichbar                      | Timeout bei Warten auf Antwort der DB | Status 500 | Login_IO_DB_1           |