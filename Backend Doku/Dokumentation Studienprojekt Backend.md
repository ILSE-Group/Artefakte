# Dokumentation Studienprojekt Backend

# Klassen #

# BaseExcercises #

### public abstract class Exercise ###

- Abstrakte Basisklasse für alle Aufgabentypen im System

- Eigenschaften:
    Id: Eindeutige ID
    Title: Titel der Aufgabe
    Description: Beschreibung 
    ExperiencePoints: XP-Belohnung der Übung

- Methoden: 
    ValidateAnswer(object answer) : Exercise
    Muss von Kindklassen implementiert werden, um die übergebene Antwort zu prüfen

 # ExcerciseHelper #    

### public class ClickableArea ###

- Repräsentiert einen anklickbaren Bereich

- Eigenschaften:
    Id: ID des Bereichs
    X,Y(int): Startkoordinaten
    Width,Height(int): Breite und Höhe

- Methoden:
    CreateNew(...) : ClickableArea (static): Erzeugt einen komplett neuen Bereich
    Reconstruct(...) : ClickableArea (static): Rekonstruiert einen bestehenden Bereich

### public class DragAndDropMapping ###

- Verknüpft ein ziehlbares Element mit seiner konkreten Zielzone

- Eigenschaften:
    Id: ID des Mappings
    ItemId: ID des Elements, das bewegt wird
    DropZoneId: ID der korrekten Zielzone

- Methoden:
    CreateNew(...) : DragAndDropMapping (static): Erzeugt ein neues Mapping
    Reconstruct(...) : DragAndDropMapping (static): Rekonstruiert ein bestehendes Mapping

### public class DraggableItem ###

- Repräsentiert ein ziehbares Element innerhalb einer Übung

- Eigenschaften:
    Id: ID des Elements
    Content: Der Inhalt des Elements 

- Methoden:
    CreateNew(...) : DraggableItem (static): Erzeugt ein neues Element
    Reconstruct(...) : DraggableItem (static): Rekonstruiert ein bestehendes Element anhand seiner ID

### public class DropZone ###

- Repräsentiert eine Zone, auf die ein Element gezogen werden kann

- Eigenschaften:
    Id: ID der Zielzone
    Label: Die Beschriftung der Zone 

- Methoden:
    CreateNew(...) : DropZone (static): Erzeugt eine neue Zielzone 
    Reconstruct(...) : DropZone (static): Rekonstruiert eine bestehende Zielzone anhand ihrer ID

### public class Link ###

- Verknüpft zwei zusammengehörige Elemente links und rechts miteinander

- Eigenschaften:
    Id: ID der Verknüpfung 
    LeftItem: Der Inhalt des linken Elements
    RightItem: Der Inhalt des rechten Elements

- Methoden:
    CreateNew(...) : Link (static): Erzeugt eine neue Verknüpfung 
    Reconstruct(...) : Link (static): Rekonstruiert eine bestehende Verknüpfung 

### public class MCOption ###

- Repräsentiert eine Antwortoption innerhalb einer Multiple-Choice-Aufgabe

- Eigenschaften:
    Id: ID der Option
    OptionText: Der Text der Antwortoption

- Methoden:
    CreateNew(...) : MCOption (static): Erzeugt eine neue Antwortoption
    Reconstruct(...) : MCOption (static): Rekonstruiert eine bestehende Antwortoption

### public class ClickableImageExercise ###

- Repräsentiert eineBild-Übung bei der bestimmte Bereiche des Bildes anklickbar sind

- Eigenschaften:
    ImageUrl: Die URL des anzuzeigenden Bildes
    ClickableAreas: Eine Liste der anklickbaren Bereiche 

- Methoden:
    CreateNew(...) : ClickableImageExercise (static): Erzeugt eine neue Bild-Übung
    Reconstruct(...) : ClickableImageExercise (static): Rekonstruiert eine bestehende Bild-Übung
    ValidateAnswer(...) : Exercise (override): Validiert die abgegebene Antwort

### public class LinkingExercise ###

- Repräsentiert eine Zuordnungsaufgabe, bei der Elemente der linken Seite mit Elementen der rechten Seite verknüpft werden müssen (erbt von Exercise)

- Eigenschaften:
    LeftItems: Liste der linken Zuordnungselemente 
    RightItems: Liste der rechten Zuordnungselemente 
    CorrectLinks: Liste der korrekten Verknüpfungen 

- Methoden:
    CreateNew(...) : LinkingExercise (static): Erzeugt eine neue Zuordnungsaufgabe
    Reconstruct(...) : LinkingExercise (static): Rekonstruiert eine bestehende Zuordnungsaufgabe
    ValidateAnswer(...) : Exercise (override): Validiert die abgegebene Antwort

### public class Room ###

- Repräsentiert einen Raum, der eine Sammlung von Übungen enthält

- Eigenschaften:
    Id: ID des Raums
    Name: Der Name des Raums
    UnlockLevel: Das benötigte Level, um diesen Raum freizuschalten
    CompletionExperiencePoints: Die Erfahrungspunkte, die man beim Abschluss des Raums erhält 
    Exercises: Eine Liste der im Raum enthaltenen Übungen

- Methoden:
    CreateNew(...) : Room: Erzeugt einen neuen Raum 
    Reconstruct(...) : Room: Rekonstruiert einen bestehenden Raum