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
	    "group": 
		{
	            "id": "group1",
		    "title": "Haushalt",
		}
	}
}
```

Kategorisierung ist von TimeModifier abhängig.

## Beispiel Eingabe-Objekte
### Item
#### Input
"Auto waschen"
#### Output
```json
{	
    "item":
	{
            "title": "Auto waschen",
	    "description": "",
	}
}
```
### Gruppiertes Item
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
```
