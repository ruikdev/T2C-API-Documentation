<div align="center">
  <img src="/placeholder.png" width="110px" alt="API_Server logo"/>
  <br>
  <h1>API Server</h1>
</div>

::: warning WORK IN PROGRESS
**Ce serveur est en cours de documentation!**
:::

## Présentation

**API Server** est une backend qui gère les horaires, les actions, les notifications et les dernières informations du réseau T2C.

Elle remplace les anciennes backends de l'API "WinDev" *([OpenIT](/WinDev/OpenIT/readme), [T2C XML](/WinDev/T2C_XML/readme), [WD Push Server](/WinDev/WD_Push/readme), [Pegase](http://localhost:5173/T2C-API-Documentation/WinDev/pegase/readme))*, tout est centralisé sur une seule frontend.

L'API est accessible via plusieurs services :

| Service               | URL de Base                       | Description                                     |
|-----------------------|-----------------------------------|-------------------------------------------------|
| **SIV**               | `https://api.t2c.fr/siv`          | Données transport (arrêts, lignes, vélos, POI)  |
| **Editorial**         | `https://api.t2c.fr/editorial`    | Contenu éditorial (news, events, pages)         |
| **Notifications**     | `https://api.t2c.fr/notification` | Gestion des notifications push                  |
| **Status**            | `https://api.t2c.fr/status`       | État de l'application (maintenance, version)    |
| **Sites**             | `https://api.t2c.fr/sites`        | Pages statiques (Ressources, Images)            |

## Services

### SIV

Le SIV *(Système d'Information Voyageur)* est un service qui remplace essentiellement [OpenIT](/WinDev/OpenIT/readme), il permet d'obtenir des informations sur des arrêts, itinéraires, points d'intérêts, C.Vélos...

| Endpoint                                | Description                  |
|-----------------------------------------|------------------------------|
| [/stops](/Yoozly/API_Server/siv-stops)             | Liste de tous les arrêts     |
| [/stops/:id](/Yoozly/API_Server/siv-stops)         | Détails d'un arrêt           |
| [/stops/search](/Yoozly/API_Server/siv-stops)      | Recherche d'arrêts           |
| [/routes](/Yoozly/API_Server/siv-routes)           | Liste des lignes/itinéraires |
| [/routes/:id](/Yoozly/API_Server/siv-routes)       | Détails d'une ligne          |
| [/bike](/Yoozly/API_Server/siv-bike)               | Stations C.Vélo              |
| [/poi](/Yoozly/API_Server/siv-poi)                 | Points d'intérêt             |
| [/itineraries](/Yoozly/API_Server/siv-itineraries) | Calcul d'itinéraires         |

### Editorial (Contenu)

| Endpoint | Description |
|----------|-------------|
| [/news](/Yoozly/API_Server/editorial-news) | Actualités |
| [/events](/Yoozly/API_Server/editorial-events) | Événements |
| [/page/:slug](/Yoozly/API_Server/editorial-pages) | Pages statiques |

### Status

| Endpoint | Méthode | Description | Statut |
|----------|---------|-------------|--------|
| / | GET | État de l'application | Fonctionnel |


## Avertissement
::: danger Avertissement Légal
**Ceci est une documentation non-officielle de l'api utilisée dans l'appli T2C.**

Nous ne sommes pas associés à "*[T2C](https://www.t2c.fr/)*", la "*[Régie EPIC T2C](https://annuaire-entreprises.data.gouv.fr/entreprise/regie-des-transports-urbains-de-l-agglomeration-clermontoise-t2c-789515160)*", à "*[C.Vélo](https://www.c-velo.fr/)*", au "*[SMTC-AC](https://www.smtc-clermont-agglo.fr/)*" ou à tout autre service lié au réseau de transport de Clermont.

Les logos, marques et autres éléments associés à T2C sont la propriété de leurs détenteurs respectifs.
:::
