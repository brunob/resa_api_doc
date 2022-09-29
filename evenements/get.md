# Liste des fiches événements

Affiche la liste des événement filtrées selon les critères passés en paramètres.

**URL** : `/http.api/ezrest/evenements/`

**Méthode** : `GET`

**Authentification requise** : oui

**Filtres et paramètres** :
* `key` : clé d'accès à l'API (**obligatoire**)
* `id_secteur` : identifiant d'une antenne (`1` pour RESAM)
* `id_asso` : identifiant d'une association 
* `liste_limite` : nombre d'événements maximum à renvoyer
* `date_debut` : date de début de la période demandée au format date Y-m-d, date courante par défaut
* `liste_duree` : nombre de mois de la période demandée, 1 par défaut
* `liste_debut` : date de début de la liste des events demandés (date_jour par défaut pour renvoyer les events à partir de la date_debut passée en paramètre), accepte les valeurs suivantes : date_veille, date_semaine, date_semaine_prec, debut_mois, debut_mois_prec, debut_mois_X avec X allant de 1 à 12

## Retour

Exemple de retour accessible dans le bloc `donnees`.

```json
[{
	"id_evenement": "...",
	"titre": "...",
	"date_debut": "...",
	"date_fin": "...",
	"horaire": "...",
	"lieu": "...",
	"adresse": "...",
	"id_asso": "...",
	"nom_asso": "..."
}, {
	"id_evenement": "...",
	"titre": "...",
	"date_debut": "...",
	"date_fin": "...",
	"horaire": "...",
	"lieu": "...",
	"adresse": "...",
	"id_asso": "...",
	"nom_asso": "..."
}]
```
