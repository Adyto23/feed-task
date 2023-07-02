# feed-task

## Developer Task

Sieh Dir den RSS-Feed unter

https://www.smb.museum/rss-feed/veranstaltungen.xml

an. Dieser Feed bietet neben allgemeinen Informationen zu Events in Berliner Museen Details über Deep Links an. Die Aufgabe, die Du lösen sollst ist, die Informationen des Feeds und dem Deep-Link zu
nutzen, um folgende JSON-Datenstruktur zu füllen:

```json
{
    "title": "",
    "description": "",
    "location": "",
    "start": 0,
    "end": 0
}
```

| Feld        | Beschreibung                                                                               | Quelle         |
|-------------|--------------------------------------------------------------------------------------------|----------------|
| title       | Ein string, der dem Titel aus dem RSS Feed entspricht.                                     | RSS XML        |
| description | Ein string, der die Description aus dem Feed extrahiert. CDATA muss hier aufgelöst werden. | RSS XML        |
| location    | Der Ort der Veranstaltung.                                                                 | Deep Link HTML |
| start       | Ein JSON Datums-Wert mit Datum und Uhrzeit des Beginns                                     | Deep Link HTML |
| end         | Ein JSON Datums-Wert mit Datum und Uhrzeit des Endes                                       | Deep Link HTML |

Dein Programm soll beim Start den Feed einlesen und den dortigen Deep-Links folgen und dabei die geforderten Informationen auslesen und als JSON-Array ausgeben.

Dir steht es frei, wie Du die Ergebnisse zugänglich machen möchtest (HTTP-Endpunkt, JSON-Datei, …).

Die von Dir eingesetzte Technologie sollte keine Betriebssystemabhängigkeiten erzeugen. Beispiele wären Node, .NET, PHP usw. Nicht erwünscht sind Umgebungen, wie Linux-C oder Windows-C++.

Die Lösung reichst Du am besten in Form eines Github-Repositories ein auf das Du uns Zugriff gibst. Alternativ kannst Du uns Deine Lösung auch als ZIP-Archiv senden.

Achte darauf, dass Du dokumentierst, wie Deine Lösung auf einem beliebigen PC/Mac ausgeführt werden kann (Installation von Abhängigkeiten usw.). Orientiere Dich an den READMEs bekannter großer
Github-Repositories.
