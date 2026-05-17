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

# public class ClickableArea #

- Repräsentiert einen anklickbaren Bereich

- Eigenschaften:
    Id: ID des Bereichs
    X,Y(int): Startkoordinaten
    Width,Height(int): Breite und Höhe

- Methoden:
    CreateNew(...) : ClickableArea (static): Erzeugt einen komplett neuen Bereich
    Reconstruct(...) : ClickableArea (static): Rekonstruiert einen bestehenden Bereich


