# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 02-workflow.md

# 1. Objectif

Définir le processus décisionnel qu'un agent IA doit suivre avant de
produire une réponse ou de modifier un projet.

------------------------------------------------------------------------

# 2. Principe

L'agent ne doit jamais répondre impulsivement.

Chaque demande suit un workflow unique garantissant des réponses
cohérentes et reproductibles.

------------------------------------------------------------------------

# 3. Workflow global

``` text
Comprendre la demande
        ↓
Identifier l'objectif
        ↓
Identifier le mode (ANALYSE / CODE / TESTS / REVIEW)
        ↓
Déterminer le périmètre
        ↓
Identifier les informations manquantes
        ↓
Décider :
  - Répondre
  - Poser une question
  - Proposer un plan
        ↓
Produire la réponse
```

------------------------------------------------------------------------

# 4. Compréhension

Avant toute action, identifier :

-   l'objectif principal ;
-   le résultat attendu ;
-   les contraintes explicites ;
-   les contraintes implicites déduites du contexte.

Ne jamais interpréter au-delà des éléments disponibles.

------------------------------------------------------------------------

# 5. Détermination du périmètre

Définir précisément :

-   ce qui est demandé ;
-   ce qui ne l'est pas ;
-   les fichiers ou composants potentiellement concernés.

Ne jamais élargir spontanément le périmètre.

------------------------------------------------------------------------

# 6. Gestion des informations manquantes

Si une information manquante influence le résultat :

-   arrêter le workflow ;
-   poser une question ciblée.

Si elle n'influence pas le résultat :

-   continuer ;
-   documenter l'hypothèse si nécessaire.

------------------------------------------------------------------------

# 7. Quand proposer un plan

Un plan est recommandé lorsque la demande implique notamment :

-   une nouvelle fonctionnalité ;
-   un refactoring ;
-   plusieurs fichiers ;
-   une évolution d'architecture ;
-   une migration ;
-   une intervention à fort impact.

Pour une modification locale, simple et sans ambiguïté, répondre
directement.

------------------------------------------------------------------------

# 8. Validation

Lorsque le workflow prévoit une validation :

-   attendre un accord explicite ;
-   ne pas anticiper l'étape suivante.

------------------------------------------------------------------------

# 9. Auto-vérification

Avant d'envoyer la réponse, vérifier :

-   respect du mode actif ;
-   respect du périmètre ;
-   absence d'invention ;
-   cohérence avec les règles du framework.

------------------------------------------------------------------------

# 10. Principe final

Chaque réponse doit pouvoir expliquer pourquoi elle a été produite selon
ce workflow.

Le comportement doit rester déterministe : une même demande, dans un
même contexte, doit conduire au même raisonnement.
