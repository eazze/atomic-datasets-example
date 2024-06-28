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
    "item": [
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
    "item": [
	{
            "id": "todo1",
            "title": "Antrag abgeben",
	    "description": "Antrag für eine Geburtsurkunde abgeben",
	    "groupId": "group1"
	}
    ],
}	
```


### Gruppierte ScheduleTodoItems
#### Input
"eine Fahrradtour machen und sie als Sport tracken"
#### Output
```json
{
    "item": [
	{
	    "id": "todo1",
	    "title": "Fahrradtour",
	    "description": "Fahrradtour machen",
	    "groupId": "group1"
	}
    ],
    "groups": [
        {
            "id": "group1",
            "title": "Sport",
        }
    ],
}	
```
