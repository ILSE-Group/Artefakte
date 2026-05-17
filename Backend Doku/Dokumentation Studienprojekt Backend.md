# Dokumentation Studienprojekt Backend

### Klassen ###

# public abstract class Exercise #

- Abstrakte Basisklasse für alle Aufgabentypen im System

- Eigenschaften:
    Id: Eindeutige ID
    Title: Titel der Aufgabe
    Description: Beschreibung 
    ExperiencePoints: XP-Belohnung der Übung

- Methoden: 
    ValidateAnswer(object answer) : Exercise
    Muss von Kindklassen implementiert werden, um die übergebene Antwort zu prüfen



