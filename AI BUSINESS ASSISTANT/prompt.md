## Partie 1 — Anatomie d'un prompt

### Tâche 1.1
**Besoin de départ :** « Je souhaite analyser les retours de clients d'une entreprise. »

**Construction du prompt (les 6 blocs) :**

| Bloc | Contenu |
|---|---|
| Rôle | Tu es analyste en satisfaction client |
| Contexte | Une entreprise de livraison alimentaire reçoit des avis clients par WhatsApp |
| Tâche | Analyse les avis suivants et identifie les problèmes récurrents |
| Données d'entrée | [on colle ici une dizaine d'avis clients] |
| Contraintes | Classe uniquement sur 3 catégories : livraison, produit, service. Réponds en français |
| Format de sortie | Liste des problèmes classés du plus au moins fréquent |

Prompt final assemblé :

Tu es analyste en satisfaction client.
Une entreprise de livraison alimentaire reçoit des avis clients par WhatsApp.
Analyse les avis suivants et identifie les problèmes récurrents.
Avis : [on colle ici une dizaine d'avis clients]
Classe uniquement sur 3 catégories : livraison, produit, service. Réponds en français.
Présente le résultat sous forme de liste des problèmes classés du plus au moins fréquent.

## Partie 2 — Comparer les techniques de prompting

**Commentaire à classer (le même pour les 4 techniques) :**
« Le service est rapide mais l'application plante régulièrement. »
Classes possibles : positif, négatif, neutre.

---

### Tâche 2.1 — Zero-shot (0 exemple)

Prompt :

Classe le commentaire suivant : "Le service est rapide mais l'application plante régulièrement."
Classes possibles : positif, négatif, neutre.

Résultat :
![Résultat 2.1](captures/partie2_zeroshot.png)

### Tâche 2.2 — One-shot (1 exemple)

Prompt :

Exemple : "Livraison rapide, très satisfait" → positif

Classe le commentaire suivant : "Le service est rapide mais l'application plante régulièrement."
Classes possibles : positif, négatif, neutre.

Résultat :
![Résultat 2.2](captures/partie2_oneshot.png)

### Tâche 2.3 — Few-shot (plusieurs exemples)

Prompt :

Exemples :
"Livraison rapide, très satisfait" → positif
"Colis en retard, aucune excuse" → négatif
"Emballage correct mais produit un peu cher" → neutre

Classe le commentaire suivant : "Le service est rapide mais l'application plante régulièrement."
Classes possibles : positif, négatif, neutre.

Résultat meme fenetre :
![Résultat 2.3](captures/partie2_fewshot.png)

Résultat autre fenetre :

![Résultat 2.3](captures/partie2_fewshot_1.png)


### Tâche 2.4 — Prompt structuré (5 blocs)

Prompt :

Rôle : Tu es un analyste chargé de classifier des avis clients.
Tâche : Classe le commentaire suivant selon le sentiment exprimé.
Données d'entrée : "Le service est rapide mais l'application plante régulièrement."
Contraintes : Classes possibles uniquement : positif, négatif, neutre. Réponds par un seul mot.
Format de sortie : Le mot de la catégorie, sans explication.

Résultat :
![Résultat 2.4](captures/partie2_structure.png)
