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