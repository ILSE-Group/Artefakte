# Studienprojekt

![ILSE Otter](ILSE_Otter.png)

ILSE - Interactive Learning System Entertainments

Offizieller Studienprojektname für Anmeldung: Gefahren im Internet - Implementierung einer interaktiven Lernplattform

Kooperation mit Karl-Ritter-von-Frisch Gymnasium Moosburg

Themen: 
> Passwortsicherheit
> Cybermobbing
> Phishing

Frontend:
> React
> TypeScript
> REST API

Backend:
> C#
> Postgres?
> Docker
> EF Core

Techytechy:
* Frontend: Sarah, Lukas P.
* Backend: Anna, Fenja, Lukas F.

Verantwortlichkeiten:
* Kommunikation: Fenja 
(Projektmanagement: Termine (Zeitplan), Moderation, Teamprobleme, generelle Infos, Kontakt zu Externen)
* Dokumentation: Lukas F.
(technische Dokumentation, Soll-/Ist-Vergleich)
* Architektur: Anna
(Artefakte für Anfang, Diagramme, Entwicklungsprozess, Pipeline, DevOps)
* Design: Sarah
(UX-/UI-Design, altersgerecht, Maskottchen, Gestaltung)
* Fachlich/Pädagogik: Lukas P.
(altersgerechte Aufbereitung der Inhalte, Wissensübermittlung)
* ALLE: persönliche Dokumentation

### Generelle Information

* Web Application
* Raum oder Roadmap -> Raum
* Für Schüler der 7.Jahrgangsstufe (arbeiten mit PCs und IPads)
* 2-wöchentliches Jour Fixe mit Herr Auer (Donnerstag 12.15 Uhr, ungerade KW)
* 2-wöchentliches Team-Meeting nur wir (Donnerstag 19.00 Uhr, gerade KW)

## Termine (Zeitplan)
* 15.06.2026: Haupt-Entwicklungsprozess abgeschlossen (Testphase beginnt)
* 02.07.2026: Poster-Präsentation (ab 15.06. Poster vorbereiten)
* 06.07.-10.07.2026: Test-Workshop an Schule

### Anforderungen

* Userverwaltung: Lehreraccounts für Auswertungen (mit Passwort), Schüleraccounts mit random Tiernamen und OTP (Einmalpasswort, durch den Lehrer freigegeben)

### Aktuelle Infos zu Implementierung

![Klassendiagramm](classdiagram_domain.pdf)

Naming:
* Topic: Überthema mit Anzahl an Räumen
* Room: logisches Abteil von Übungen
* Exercises: Übungen an sich
