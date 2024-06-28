## Example Data Input
*Generelle Formulierung:*
*"Ich möchte [Objekt].."*

Kategorisierung ist von TimeModifier abhängig.
## Example Input Objekte
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
#### Input
"einen Antrag für eine Geburtsurkunde abgeben"
#### Output
```json
{
    "todoItems": [
	{
            "id": "todo1",
            "title": "Antrag abgeben",
	    "description": "Antrag für eine Geburtsurkunde abgeben",
            "scheduleable": true,
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
            "scheduleable": true,
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
