## API

### login

#### POST

| Testart | Ereignis                                 | Überprüfung                           | Ergebnis   | Testname                |
| ------- | ---------------------------------------- | ------------------------------------- | ---------- | ----------------------- |
| Positiv | Request entspricht der Dokumentation, Daten stimmen überein | Passwort passt zur E-Mail             | Status 200 | Login_Positiv_Correct   |
| Positiv | E-Mail existiert nicht                   | E-Mail steht nicht in DB              | Status 400 | Login_Positiv_NoEmail   |
| Positiv | Daten stimmen nicht überein              | Passwort passt nicht zur E-Mail       | Status 400 | Login_Positiv_Incorrect |
| Negativ | Request entspricht nicht der Dokumentation |                                       | Status 400 | Login_Negativ_Request   |
| I/O     | DB nicht erreichbar                      | Timeout bei Warten auf Antwort der DB | Status 500 | Login_IO_DB             |

### logout

#### DELETE

| Testart | Ereignis            | Überprüfung                           | Ergebnis                       | Testname               |
| ------- | ------------------- | ------------------------------------- | ------------------------------ | ---------------------- |
| Positiv | API Key gültig      | API Key existiert in DB               | User wird gelöscht, Status 200 | Logout_Positiv_Correct |
| Negativ | API Key ungültig    | API Key existiert nicht in DB         | Status 400                     | Logout_Negativ_Key     |
| I/O     | DB nicht erreichbar | Timeout bei Warten auf Antwort der DB | Status 500                     | Logout_IO_DB           |

### register

#### POST

| Testart | Ereignis                                 | Überprüfung                           | Ergebnis                       | Testname                 |
| ------- | ---------------------------------------- | ------------------------------------- | ------------------------------ | ------------------------ |
| Positiv | Request entspricht der Dokumentation     | E-Mail und Passwort sind gefüllt      | User wird angelegt, Status 200 | Register_Positiv_Correct |
| Positiv | Benutzer ist schon vorhanden             | E-Mail existiert in DB                | Status 400                     | Register_Positiv_User    |
| Negativ | Request entspricht nicht der Dokumentation |                                       | Status 400                     | Register_Negativ_Request |
| I/O     | DB nicht erreichbar                      | Timeout bei Warten auf Antwort der DB | Status 500                     | Register_IO_DB           |



### party

#### GET



#### POST



#### GET/{id}




#### PUT/{id}



#### DELETE/{id}



#### party/guest

##### POST

##### PUT

##### DELETE



####party/rating

##### POST



#### party/todo

##### POST

##### PUT

##### DELETE



#### party/task

##### POST

##### PUT

##### DELETE



### user

#### PUT/{id}

| Testart | Ereignis                                 | Überprüfung                           | Ergebnis                        | Testname                 |
| ------- | ---------------------------------------- | ------------------------------------- | ------------------------------- | ------------------------ |
| Positiv | API Key und ID gültig                    | API Key und ID existieren in DB       | User wird angepasst, Status 200 | User_PUT_Positiv_Correct |
| Negativ | Request entspricht nicht der Dokumentation |                                       | Status 400                      | User_PUT_Negativ_Request |
| Negativ | ID ungültig                              | ID existiert nicht in DB              | Status 400                      | User_PUT_Negativ_ID      |
| Negativ | API Key ungültig                         | API Key existiert nicht in DB         | Status 400                      | User_PUT_Negativ_Key     |
| Negativ | API Key gehört nicht zu User             | Abgleichen von API-Key und User       | Status 400                      | User_PUT_Negativ_        |
| I/O     | DB nicht erreichbar                      | Timeout bei Warten auf Antwort der DB | Status 500                      | User_PUT_IO_DB           |

#### GET



#### GET/{id}



#### user/contact

##### GET



##### POST



##### DELETE



#### PUT



### image

#### POST

#### GET/{id}

