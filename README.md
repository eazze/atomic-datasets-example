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
            "title": "Wäsche waschen",
	    "description": "",
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
            "title": "Antrag abgeben",
	    "description": "Antrag für eine Geburtsurkunde abgeben",
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
