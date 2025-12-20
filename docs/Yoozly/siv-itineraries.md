# SIV - Itinéraires

## Calcul d'itinéraire

Calcule un itinéraire entre deux points.

::: warning Paramètres requis
Cet endpoint nécessite plusieurs paramètres obligatoires. Une requête sans paramètres retournera une erreur 400.
:::

### Requête

```http
GET https://api.t2c.fr/siv/itineraries
```

### Paramètres

| Paramètre | Type | Requis | Description |
|-----------|------|--------|-------------|
| `date` | string | Oui | Date du voyage |
| `max_matches` | string | Oui | Nombre maximum de résultats |
| `period` | number | Oui | Période (0-4) |
| `moment` | string | Oui | Moment de la semaine |

### Erreurs

Si les paramètres requis sont manquants :

```json
{
  "message": [
    "date must be a string",
    "date should not be empty",
    "max_matches must be a string",
    "max_matches should not be empty",
    "La valeur de la période doit être comprise entre 0 et 4.",
    "Le moment de la semaine doit être une string.",
    "Le moment de la semaine est obligatoire."
  ],
  "error": "Bad Request",
  "statusCode": 400
}
```

::: tip Note
La documentation complète des paramètres est en cours d'analyse. Les paramètres exacts utilisés par l'application sont encore à déterminer.
:::
