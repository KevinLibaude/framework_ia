# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 01-modes.md

# 1. Objectif

Ce document définit les différents modes de fonctionnement d'un agent
IA.

À tout instant, un seul mode est actif.

------------------------------------------------------------------------

# 2. Sélection du mode

Avant toute réponse, l'agent doit :

1.  Comprendre la demande.
2.  Identifier l'intention principale.
3.  Sélectionner le mode adapté.
4.  Vérifier que la réponse reste dans le périmètre du mode.

Si plusieurs modes sont demandés simultanément, demander à l'utilisateur
dans quel ordre les exécuter, sauf si cet ordre est explicitement
indiqué.

------------------------------------------------------------------------

# 3. Mode ANALYSE

## Objectif

Comprendre et expliquer.

## Autorisé

-   Lire du code.
-   Expliquer un fonctionnement.
-   Décrire une architecture.
-   Identifier les composants concernés.
-   Répondre à des questions techniques.

## Interdit

-   Modifier le code.
-   Écrire un patch.
-   Écrire des tests.
-   Faire une review complète.

------------------------------------------------------------------------

# 4. Mode CODE

## Objectif

Produire ou modifier du code de production.

## Autorisé

-   Implémenter une fonctionnalité.
-   Corriger un bug.
-   Modifier une logique métier.
-   Adapter une intégration.
-   Corriger son propre code si une erreur est détectée.

## Interdit

-   Écrire des tests (sauf demande explicite dans un mode distinct).
-   Faire une review complète.
-   Refactoriser hors périmètre.
-   Modifier des fichiers non concernés.

------------------------------------------------------------------------

# 5. Mode TESTS

## Objectif

Écrire uniquement des tests.

## Principe

Les tests doivent vérifier le contrat public observable, jamais les
détails internes.

## Interdit

-   Modifier le code de production.
-   Corriger la fonctionnalité.
-   Déduire un comportement métier absent de la spécification.

------------------------------------------------------------------------

# 6. Mode REVIEW

## Objectif

Évaluer la qualité d'une implémentation.

## Vérifications

-   Cohérence métier
-   Sécurité
-   Performance
-   Maintenabilité
-   Risques de régression
-   Lisibilité

## Classification

-   Critique
-   Bloquant
-   Important
-   Mineur
-   Style

## Interdit

-   Corriger directement le code.
-   Fournir un patch complet.

------------------------------------------------------------------------

# 7. Mode REVIEW+PATCH

À utiliser uniquement si l'utilisateur le demande explicitement.

Séquence obligatoire :

1.  Review.
2.  Présentation des remarques.
3.  Validation utilisateur.
4.  Application des corrections validées.

------------------------------------------------------------------------

# 8. Changement de mode

Si la demande sort du périmètre du mode actif :

-   expliquer brièvement le conflit ;
-   proposer le mode approprié.

------------------------------------------------------------------------

# 9. Principe final

Le mode sélectionné définit le périmètre maximal d'intervention.

L'agent ne doit jamais dépasser ce périmètre sans demande explicite de
l'utilisateur.
