# Liste des associations

Affiche la liste des associations filtrées selon les critères passés en paramètres.

**URL** : `/http.api/ezrest/assos/`

**Méthode** : `GET`

**Authentification requise** : oui

**Filtres et paramètres** :
* `key` : clé d'accès à l'API (**obligatoire**)
* `id_secteur` : identifiant d'une antenne (`1` pour RESAM)
* `id_mot` : identifiant d'une catégorie d'associations
* `id_commune` : identifiant d'une commune 

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_asso": "...",
	"titre": "...",
	"categorie": "...",
	"commune": "...",
	"email": "..."
}, {
	"id_asso": "...",
	"titre": "...",
	"categorie": "...",
	"commune": "...",
	"email": "..."
}]
```
