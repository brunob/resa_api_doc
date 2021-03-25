# Liste des fiches matériel

Affiche la liste des matériels filtrées selon les critères passés en paramètres.

**URL** : `/http.api/ezrest/materiels/`

**Méthode** : `GET`

**Authentification requise** : oui

**Filtres et paramètres** :
* `key` : clé d'accès à l'API (**obligatoire**)
* `id_secteur` : identifiant d'une antenne (`1` pour RESAM)
* `id_mot` : identifiant d'une catégorie d'associations
* `id_commune` : identifiant d'une commune
* `id_asso` : identifiant d'une association 

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_materiel": "...",
	"titre": "...",
	"categorie": "...",
	"materiel_conditions": "...",
	"commune": "..."
}, {
	"id_materiel": "...",
	"titre": "...",
	"categorie": "...",
	"materiel_conditions": "...",
	"commune": "..."
}]
```
