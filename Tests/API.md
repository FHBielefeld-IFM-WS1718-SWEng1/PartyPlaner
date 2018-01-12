## API

### Login

#### POST

| Testart | Ereignis                                 | Überprüfung                           | Ergebnis   | Testname                |
| ------- | ---------------------------------------- | ------------------------------------- | ---------- | ----------------------- |
| Positiv | Request entspricht der Dokumentation, Daten stimmen überein | Passwort passt zur E-Mail             | Status 200 | Login_Positiv_Correct   |
| Positiv | E-Mail existiert nicht                   | E-Mail steht nicht in DB              | Status 400 | Login_Positiv_NoEmail   |
| Positiv | Daten stimmen nicht überein              | Passwort passt nicht zur E-Mail       | Status 400 | Login_Positiv_Incorrect |
| Negativ | Request entspricht nicht der Dokumentation |                                       | Status 400 | Login_Negativ_Request_1 |
| I/O     | DB nicht erreichbar                      | Timeout bei Warten auf Antwort der DB | Status 500 | Login_IO_DB_1           |

### Logout

#### DELETE

| Testart | Ereignis            | Überprüfung                           | Ergebnis                       | Testname         |
| ------- | ------------------- | ------------------------------------- | ------------------------------ | ---------------- |
| Positiv | API Key gültig      | API Key existiert in DB               | User wird gelöscht, Status 200 | Logout_Positiv_1 |
| Negativ | API Key ungültig    | API Key existiert nicht in DB         | Status 400                     | Logout_Negativ_1 |
| I/O     | DB nicht erreichbar | Timeout bei Warten auf Antwort der DB | Status 500                     | Login_IO_DB_1    |

### Register

#### POST

| Testart | Ereignis                                 | Überprüfung                           | Ergebnis                       | Testname                 |
| ------- | ---------------------------------------- | ------------------------------------- | ------------------------------ | ------------------------ |
| Positiv | Request entspricht der Dokumentation     | E-Mail und Passwort sind gefüllt      | User wird angelegt, Status 200 | Register_Positiv_Correct |
| Positiv | Benutzer ist schon vorhanden             | E-Mail existiert in DB                | Status 400                     | Register_Positiv_User    |
| Negativ | Request entspricht nicht der Dokumentation |                                       | Status 400                     | Register_Negativ_1       |
| I/O     | DB nicht erreichbar                      | Timeout bei Warten auf Antwort der DB | Status 500                     | Register_IO_DB_1         |



### Party

####GET



####GET/{id}



####POST



#### PUT/{id}



#### DELETE/{id}



###User

#### PUT



#### GET



#### GET/{id}



### Contactlist

#### GET



#### POST



#### DELETE



#### PUT

