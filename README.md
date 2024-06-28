## Beispiel Daten-Eingabe
*Generelle Formulierung:*
*"Ich möchte [Objekt].."*

Formattierung:
```json
{
    "input": "Wäsche waschen und als Haushalt tracken",
    "output": {
	    "item": 
		{
	            "title": "Wäsche waschen",
		    "description": "",
	            "groupId": "group1"
		},
	    "groups": 
		{
	            "id": "group1",
		    "title": "Haushalt",
		}
	}
}
```

Kategorisierung ist von TimeModifier abhängig.

## Beispiel Eingabe-Objekte
### Tägliches Item
#### Input
"Wäsche waschen und als Haushalt tracken"
#### Output
```json
{	
    "item":
	{
            "title": "Wäsche waschen",
	    "description": "",
            "groupId": "group1"
	}
}
```
### Gruppiertes, tägliches Item
#### Input
"Wäsche waschen und als Haushalt tracken"
#### Output
```json
{	
    "item":
	{
            "title": "Wäsche waschen",
	    "description": "",
            "groupId": "group1"
	},
    "groups":
	{
            "id": "group1",
	    "title": "Haushalt",
	}
}
```


### Todo-Item
#### Input
"einen Antrag für eine Geburtsurkunde abgeben"
#### Output
```json
{
    "item":
	{
            "title": "Antrag abgeben",
	    "description": "Antrag für eine Geburtsurkunde abgeben",
	}
}	
```


### Gruppiertes Todo-Item
#### Input
"eine Fahrradtour machen und sie als Sport tracken"
#### Output
```json
{
    "item":
	{
	    "title": "Fahrradtour",
	    "description": "Fahrradtour machen",
	    "groupId": "group1"
	}
    "groups":
        {
            "id": "group1",
            "title": "Sport",
        }
}	
```
