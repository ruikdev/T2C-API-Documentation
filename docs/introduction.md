<div align="center">
  <img src="/apilogo2.png" width="250" alt="API logo"/>
  <br>
  <h1>Documentation non-officielle de l'API T2C</h1>
</div>

::: info Mise à jour Décembre 2025
Cette documentation a été mise à jour pour inclure la nouvelle API "Yoozly" utilisée par l'application T2C v3.x.
:::

## API "Yoozly" (Actuelle - v3.x)

"Yoozly" est la nouvelle API utilisée par l'application T2C depuis la version `3.0` (Décembre 2025).

| Service | URL de Base | Description | Statut |
| :------ | :---------- | :---------- | :----- |
| [SIV](/Yoozly/readme) | `https://api.t2c.fr/siv` | Arrêts, Lignes, C.Vélo, POI, Itinéraires | Documenté |
| [Editorial](/Yoozly/readme) | `https://api.t2c.fr/editorial` | News, Events, Pages statiques | Documenté |
| [Status](/Yoozly/status) | `https://api.t2c.fr/status` | État de l'application | Documenté |
| Notifications | `https://api.t2c.fr/notification` | Push notifications | À documenter |

### Endpoints SIV testés et fonctionnels

| Endpoint | Statut |
| :------- | :----- |
| `/siv/stops` | Fonctionnel |
| `/siv/stops/:id` | Fonctionnel |
| `/siv/stops/search` | Fonctionnel |
| `/siv/routes` | Fonctionnel |
| `/siv/routes/:id` | Fonctionnel |
| `/siv/bike` | Fonctionnel |
| `/siv/poi` | Fonctionnel |
| `/siv/itineraries` | Fonctionnel (params requis) |

### Endpoints Editorial testés et fonctionnels

| Endpoint | Statut |
| :------- | :----- |
| `/editorial/news` | Fonctionnel |
| `/editorial/events` | Fonctionnel |
| `/editorial/page/:slug` | Fonctionnel |

### Services Externes

| Service | URL | Statut |
| :------ | :-- | :----- |
| HubUp LiveMap | `https://livemap.v2.hubup.cloud/network/56988460` | Fonctionnel |
| E-Boutique SMTC | `https://eboutique.smtc-clermont.fr/fr/billetterie` | Fonctionnel |
| IGN Géocodage | `https://data.geopf.fr/geocodage/completion` | Fonctionnel |
| Réseau Avant/Après | `https://reseauavantapres.t2c.fr` | Fonctionnel |
| Umami Analytics | `https://analytics.t2c.fr/api/send` | POST uniquement |

---

## APIs Obsolètes (v2.x)

Les APIs suivantes étaient utilisées par l'application T2C v2.5 et antérieures. Elles ont été remplacées par l'API "Yoozly" le 20 Décembre 2025.

::: warning APIs Obsolètes
Ces APIs ne sont plus utilisées par l'application actuelle mais peuvent encore être accessibles.
:::

| Backends | Description | Statut Doc |
| :------- | :---------- | :--------- |
| [OpenIT](/OpenIT/readme) | Table des Horaires, Prochains passages et Itinéraires | 99% |
| [T2C XML](/T2C_XML/readme) | Alertes, Brèves, Évènements et Infos Trafic | 100% |
| [WinDev Push Server](/WD_Push/readme) | Informations du Réseau et Actions Push | 50% |
| [Pegase](/pegase/readme) | Notifications | 100% |

---

## Informations Techniques

### Version de l'application

| Champ | Valeur |
| :---- | :----- |
| Package | `fr.t2c.t2c` |
| Version | `3.1.0` |
| Version Code | `4128` |
| Min SDK | Android 7.0 (API 24) |
| Target SDK | Android 16 (API 36) |

### Environnements

| Environnement | SIV | Editorial |
| :------------ | :-- | :-------- |
| **Production** | `https://api.t2c.fr/siv` | `https://api.t2c.fr/editorial` |
| **Staging** | `https://api-staging.t2c.fr/siv` | `https://api-staging.t2c.fr/editorial` |

---

## Contribuer

::: tip Contribution
Si vous souhaitez contribuer à cette documentation, merci d'ouvrir une [pull-request](https://github.com/dumb-software/T2C-API-Documentation/pulls).
:::

## Avertissement

::: danger Avertissement Légal
**Ceci est une documentation non-officielle de l'api utilisée dans l'appli T2C.**

Nous ne sommes pas associés à "*[T2C](https://www.t2c.fr/)*", la "*[Régie EPIC T2C](https://annuaire-entreprises.data.gouv.fr/entreprise/regie-des-transports-urbains-de-l-agglomeration-clermontoise-t2c-789515160)*", à "*[C.Vélo](https://www.c-velo.fr/)*", au "*[SMTC-AC](https://www.smtc-clermont-agglo.fr/)*" ou à tout autre service lié au réseau de transport de Clermont.

Les logos, marques et autres éléments associés à T2C sont la propriété de leurs détenteurs respectifs.
:::
