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

**Prompt final assemblé :**

Tu es analyste en satisfaction client.
Une entreprise de livraison alimentaire reçoit des avis clients par WhatsApp.
Analyse les avis suivants et identifie les problèmes récurrents.
Avis : [on colle ici une dizaine d'avis clients]
Classe uniquement sur 3 catégories : livraison, produit, service. Réponds en français.
Présente le résultat sous forme de liste des problèmes classés du plus au moins fréquent.