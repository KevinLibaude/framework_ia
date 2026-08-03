# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 03-planning.md

# 1. Objectif

Définir la manière dont un agent IA construit, présente et exécute un
plan d'action.

Un plan a pour but de réduire les risques, de rendre les actions
explicites et de permettre à l'utilisateur de valider l'approche avant
toute modification importante.

------------------------------------------------------------------------

# 2. Quand un plan est requis

Un plan est requis notamment pour :

-   une nouvelle fonctionnalité ;
-   une modification touchant plusieurs fichiers ;
-   un refactoring ;
-   une migration ;
-   une évolution d'architecture ;
-   une intervention dont les impacts sont difficiles à évaluer.

Un plan n'est généralement pas nécessaire pour une correction locale,
évidente et sans ambiguïté.

------------------------------------------------------------------------

# 3. Objectifs d'un plan

Un plan doit :

-   définir le périmètre ;
-   limiter les modifications ;
-   identifier les dépendances ;
-   mettre en évidence les risques ;
-   permettre une validation utilisateur.

------------------------------------------------------------------------

# 4. Structure minimale

Chaque plan contient :

## Mode

Le mode actif (ANALYSE, CODE, TESTS, REVIEW ou REVIEW+PATCH).

## Objectif

Le résultat attendu.

## Périmètre

Les composants ou fichiers susceptibles d'être concernés.

## Étapes

Découpage en étapes indépendantes et vérifiables.

## Risques

Les principaux impacts ou incertitudes.

## Validation

L'action attendue de l'utilisateur avant l'exécution.

------------------------------------------------------------------------

# 5. Types de plans

## Correction

Corriger un comportement existant avec un impact minimal.

## Feature

Ajouter une fonctionnalité sans modifier les comportements non
concernés.

## Refactoring

Améliorer la structure sans modifier le comportement observable.

## Migration

Faire évoluer une technologie, une API ou une architecture tout en
limitant les régressions.

## Review

Présenter la méthode d'analyse avant la revue complète.

------------------------------------------------------------------------

# 6. Découpage

Chaque étape doit :

-   avoir un objectif unique ;
-   pouvoir être comprise indépendamment ;
-   limiter les effets de bord.

Éviter les étapes trop larges.

------------------------------------------------------------------------

# 7. Gestion des risques

Identifier lorsque c'est pertinent :

-   les régressions possibles ;
-   les dépendances concernées ;
-   les impacts sur les performances ;
-   les impacts sur la sécurité ;
-   les incompatibilités potentielles.

------------------------------------------------------------------------

# 8. Exécution

Après validation :

-   exécuter les étapes dans l'ordre ;
-   ne pas sortir du périmètre validé ;
-   signaler immédiatement toute découverte remettant le plan en cause.

Dans ce cas, suspendre l'exécution et proposer un nouveau plan.

------------------------------------------------------------------------

# 9. Principe final

Le plan constitue un contrat de travail entre l'utilisateur et l'agent
IA.

Toute modification importante doit rester conforme au plan validé.
