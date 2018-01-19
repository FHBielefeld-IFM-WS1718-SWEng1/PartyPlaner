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
