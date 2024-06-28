## Example Data Input
*Generelle Formulierung:*
*"Ich möchte [Objekt].."*

Kategorisierung ist von TimeModifier abhängig.
## Example Input Objekte
### Todo
#### Input
"ein Projekt in Docker einrichten für mein Coding-Projekt"
#### Output
```json
{
    "todoItems": [
	{
	    "id": "todo1",
	    "title": "Einrichten des Projekts in Docker",
	    "description": "Erzeugen der Entwicklungsumgebung und Konfiguration der Services",
	    "todoListCollectionId": "todoList1"
	}
    ],
    "todoListCollection": [
	{
	    "id": "todoList1",
	    "title": "Coding-Projekt"
	}
    ],
}
```


### Gruppierte Todos
#### Input
"ein Projekt in Docker einrichten für mein Coding Projekt und der Gruppe Coden zuweisen"
#### Output
```json
{
    "todoItems": [
	{
	    "id": "todo1",
	    "title": "Einrichten des Projekts in Docker",
	    "description": "Erzeugen der Entwicklungsumgebung und Konfiguration der Services",
	    "todoListCollectionId": "todoList1"
	}
    ],
    "todoListCollection": [
	{
	    "id": "todoList1",
	    "title": "Coding-Projekt"
	}
    ],
    "groups": [
	{
	    "id": "group1",
	    "title": "Coden",
	}
    ]
}
```


### ScheduleDailyItem
#### Input
"Wäsche waschen und als Haushalt tracken"
#### Output
```json
{	
    "dailys": [
	{
            "id": "daily1",
            "title": "Wäsche waschen",
            "groupId": "group1"
	}
    ],
    "groups": [
	{
            "id": "group1",
	    "title": "Haushalt",
	}
    ],
}
```


### ScheduleTodoItems
"einen Antrag für eine Geburtsurkunde abgeben"

```json
{
	"todoItems": [
	{
            "id": "todo1",
            "title": "Antrag abgeben",
	    "description": "Antrag für eine Geburtsurkunde abgeben",
	    "groupId": "group1",
	    "todoListCollectionId": "todoList1"
	}
    ],
    "todoListCollection": [
	{
	    "id": "todoList1",
	    "title": "Neue Aufgabenliste"
	}
    ]
}	
```


### Gruppierte ScheduleTodoItems
#### Input
"eine Fahrradtour machen und sie als Sport tracken"
#### Output
```json
{
    "todoItems": [
	{
	    "id": "todo1",
	    "title": "Fahrradtour",
	    "description": "Fahrradtour machen",
	    "groupId": "group1",
	    "todoListCollectionId": "todoList1"
	}
    ],
    "groups": [
        {
            "id": "group1",
            "title": "Sport",
        }
    ],
    "todoListCollection": [
	{
	    "id": "todoList1",
	    "title": "Unternehmungen"
	}
    ],
}	
```
