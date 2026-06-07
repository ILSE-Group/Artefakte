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

# public class DragAndDropMapping #

- Verknüpft ein ziehlbares Element mit seiner konkreten Zielzone

- Eigenschaften:
    Id: ID des Mappings
    ItemId: ID des Elements, das bewegt wird
    DropZoneId: ID der korrekten Zielzone

- Methoden:
    CreateNew(...) : DragAndDropMapping (static): Erzeugt ein neues Mapping
    Reconstruct(...) : DragAndDropMapping (static): Rekonstruiert ein bestehendes Mapping

# public class DraggableItem #

- Repräsentiert ein ziehbares Element innerhalb einer Übung

- Eigenschaften:
    Id: ID des Elements
    Content: Der Inhalt des Elements 

- Methoden:
    CreateNew(...) : DraggableItem (static): Erzeugt ein neues Element
    Reconstruct(...) : DraggableItem (static): Rekonstruiert ein bestehendes Element anhand seiner ID

# public class DropZone #

- Repräsentiert eine Zone, auf die ein Element gezogen werden kann

- Eigenschaften:
    Id: ID der Zielzone
    Label: Die Beschriftung der Zone 

- Methoden:
    CreateNew(...) : DropZone (static): Erzeugt eine neue Zielzone 
    Reconstruct(...) : DropZone (static): Rekonstruiert eine bestehende Zielzone anhand ihrer ID