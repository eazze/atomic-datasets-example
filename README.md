## Example Data Input
*Generelle Formulierung:*
*"Ich möchte [Objekt].."*

Kategorisierung ist von TimeModifier abhängig
## Example Input Objekte
### Todo
"ein Projekt in Docker einrichten für mein Coding-Projekt"
### Gruppierte Todos
"ein Projekt in Docker einrichten für mein Coding Projekt und der Gruppe Coden zuweisen"
### ScheduleDailyItem
"Wäsche waschen und als Haushalt tracken"
### ScheduleTodoItems
"einen Antrag abgeben"
### Gruppierte ScheduleTodoItems
"eine Fahrradtour machen und sie als Sport tracken"
## Example Data Output
### Todo
```json
{
    "todoItems": [
	{
	    "id": "todo1",
	    "title": "Einrichten des Projekts in        Docker",
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
```json
{	
    "dailys": [
	{
            "id": "daily1",
            "title": "Mathematik",
            "groupId": "group1"
	}
    ],
    "groups": [
	{
            "id": "group1",
	    "title": "Naturwissenschaften",
	}
    ],
    "scheduleItems": [
	{
	    "id": "schedule1",
	    "day": "Monday",
	    "startTime": "08:00",
	    "endTime": "09:00",
	    "duration": 60,
	    "orderingInDay": 0,
	    "scheduleId": "group1",
	    "dailyItemId": "daily1",
	    "todoItemId": null
	}
    ],
    "scheduleCollection": [
	{
	    "id": "schedule1",
	    "title": "Testplan"
	}
    ]
}
```

### ScheduleTodoItems
```json
{
	"todoItems": [
	{
            "id": "todo1",
            "title": "Hausaufgaben",
	    "description": "",
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
```json
{
    "todoItems": [
	{
	    "id": "todo1",
	    "title": "Hausaufgaben",
	    "description": "Mathehausaufgaben erledigen",
	    "groupId": "group1",
	    "todoListCollectionId": "todoList1"
	}
    ],
    "groups": [
        {
            "id": "group1",
            "title": "Naturwissenschaften",
        }
    ],
    "todoListCollection": [
	{
	    "id": "todoList1",
	    "title": "Neue Aufgabenliste"
	}
    ],
}	
```
