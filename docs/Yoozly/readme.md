<div align="center">
  <h1>API Yoozly</h1>
</div>

::: tip Nouvelle API
Cette API est utilisée par l'application T2C à partir de la version `3.0` (Décembre 2025).
:::

## Présentation

**Yoozly** est la nouvelle infrastructure utilisée par T2C depuis la refonte du réseau en Décembre 2025. Elle remplace les anciennes APIs (OpenIT, WinDev Push Server, T2C XML, Pegase).

L'API est accessible via plusieurs services :

| Service | URL de Base | Description |
|---------|-------------|-------------|
| **SIV** | `https://api.t2c.fr/siv` | Données transport (arrêts, lignes, vélos, POI) |
| **Editorial** | `https://api.t2c.fr/editorial` | Contenu éditorial (news, events, pages) |
| **Notifications** | `https://api.t2c.fr/notification` | Gestion des notifications push |
| **Status** | `https://api.t2c.fr/status` | État de l'application (maintenance, version) |

### Environnements

| Environnement | URL SIV | URL Editorial |
|---------------|---------|---------------|
| **Production** | `https://api.t2c.fr/siv` | `https://api.t2c.fr/editorial` |
| **Staging** | `https://api-staging.t2c.fr/siv` | `https://api-staging.t2c.fr/editorial` |

## Endpoints

### SIV (Système d'Information Voyageur)

| Endpoint | Méthode | Description | Statut |
|----------|---------|-------------|--------|
| [/stops](/Yoozly/siv-stops) | GET | Liste de tous les arrêts | Fonctionnel |
| [/stops/:id](/Yoozly/siv-stops) | GET | Détails d'un arrêt | Fonctionnel |
| [/stops/search](/Yoozly/siv-stops) | GET | Recherche d'arrêts | Fonctionnel |
| [/routes](/Yoozly/siv-routes) | GET | Liste des lignes/itinéraires | Fonctionnel |
| [/routes/:id](/Yoozly/siv-routes) | GET | Détails d'une ligne | Fonctionnel |
| [/bike](/Yoozly/siv-bike) | GET | Stations C.Vélo | Fonctionnel |
| [/poi](/Yoozly/siv-poi) | GET | Points d'intérêt | Fonctionnel |
| [/itineraries](/Yoozly/siv-itineraries) | GET | Calcul d'itinéraires | Fonctionnel |

### Editorial (Contenu)

| Endpoint | Méthode | Description | Statut |
|----------|---------|-------------|--------|
| [/news](/Yoozly/editorial-news) | GET | Actualités | Fonctionnel |
| [/events](/Yoozly/editorial-events) | GET | Événements | Fonctionnel |
| [/page/:slug](/Yoozly/editorial-pages) | GET | Pages statiques | Fonctionnel |

### Status

| Endpoint | Méthode | Description | Statut |
|----------|---------|-------------|--------|
| / | GET | État de l'application | Fonctionnel |

## Services Externes

L'application utilise également ces services externes :

| Service | URL | Description |
|---------|-----|-------------|
| **HubUp LiveMap** | `https://livemap.v2.hubup.cloud/network/56988460` | Carte temps réel des véhicules |
| **E-Boutique SMTC** | `https://eboutique.smtc-clermont.fr/fr/billetterie` | Billetterie en ligne |
| **IGN Géocodage** | `https://data.geopf.fr/geocodage/completion` | Autocomplétion d'adresses |
| **Réseau Avant/Après** | `https://reseauavantapres.t2c.fr` | Comparaison ancien/nouveau réseau |
| **Umami Analytics** | `https://analytics.t2c.fr` | Analytics (POST /api/send) |

## Avertissement

::: danger Avertissement Légal
**Ceci est une documentation non-officielle de l'API utilisée dans l'appli T2C.**

Nous ne sommes pas associés à "*[T2C](https://www.t2c.fr/)*", la "*[Régie EPIC T2C](https://annuaire-entreprises.data.gouv.fr/entreprise/regie-des-transports-urbains-de-l-agglomeration-clermontoise-t2c-789515160)*", à "*[C.Vélo](https://www.c-velo.fr/)*", au "*[SMTC-AC](https://www.smtc-clermont-agglo.fr/)*" ou à tout autre service lié au réseau de transport de Clermont.

Les logos, marques et autres éléments associés à T2C sont la propriété de leurs détenteurs respectifs.
:::
