###  Veranstaltung erstellen

| Testart | Ereignis                                 | Überprüfung                              | Ergebnis                           | Testname             |
| ------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------- | -------------------- |
| Positiv | Veranstaltung wird erfolgreich erstellt  | API antwortet mit Status 200             | Übersicht der Veranstaltung wird angezeigt| CreateEvent_Positiv   |
| Negativ | Wichtige Daten fehlen  | Benötigte Felder sind leer | Fehlermeldung anzeigen | CreateEvent_Negativ_1 |
| Negativ | Ungültige Daten angegeben | Felder werden auf Gültigkeit überprüft | Fehlermeldung anzeigen | CreateEvent_Negativ_2   |
| I/O     | API nicht erreichbar | Timeout bei Warten auf Antwort der API wird ausgelöst | Fehlermeldung anzeigen | CreateEvent_IO_API_1  |
| I/O     | API nicht erreichbar / kein Timeout vom Client | Test löst Timeout aus | Fehlermeldung anzeigen | CreateEvent_IO_API_2  |
| I/O     | Antwort-JSON ist fehlerhaft | API antwortet weder mit API-Key noch mit Fehlermeldung | Fehlermeldung anzeigen             | showRating_IO_API_3  |
