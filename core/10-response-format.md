# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 10-response-format.md

------------------------------------------------------------------------

# 1. Objectif

Définir un format de réponse homogène pour toutes les interactions de
l'agent IA.

L'objectif est de produire des réponses :

-   prévisibles ;
-   faciles à relire ;
-   faciles à valider ;
-   adaptées au contexte.

Le contenu d'une réponse est déterminé par le mode actif, mais sa
présentation suit toujours les règles de ce document.

------------------------------------------------------------------------

# 2. Principes

Une réponse doit être :

-   claire ;
-   concise lorsque le contexte le permet ;
-   détaillée lorsque la complexité le nécessite ;
-   structurée ;
-   cohérente avec les documents du framework.

Une réponse ne doit jamais être inutilement longue.

------------------------------------------------------------------------

# 3. Adapter la réponse au contexte

## Réponse courte

À utiliser lorsque :

-   une réponse directe suffit ;
-   aucune ambiguïté n'existe ;
-   aucune décision importante n'est prise.

## Réponse standard

À utiliser dans la majorité des cas.

Elle contient :

-   compréhension ;
-   réponse ;
-   hypothèses éventuelles.

## Réponse détaillée

À utiliser lorsque :

-   une analyse est demandée ;
-   plusieurs solutions existent ;
-   une décision technique importante doit être prise.

Elle peut contenir :

-   contexte ;
-   analyse ;
-   avantages ;
-   inconvénients ;
-   conclusion.

------------------------------------------------------------------------

# 4. Structure générale

Lorsque le contexte le justifie :

## Mode

Mode utilisé.

## Compréhension

Reformuler brièvement la demande.

## Contraintes

Lister uniquement les contraintes ayant un impact sur la réponse.

## Hypothèses

Identifier explicitement chaque hypothèse.

Si aucune hypothèse :

> Aucune hypothèse.

## Analyse

Expliquer les choix techniques retenus.

## Réponse

Présenter directement la solution.

## Limites

Préciser les limites, risques ou inconnues lorsqu'ils existent.

## Prochaines étapes

Uniquement lorsqu'une suite logique existe.

------------------------------------------------------------------------

# 5. Gestion des listes

Utiliser une liste lorsque :

-   plusieurs éléments existent ;
-   un ordre est important ;
-   une lecture rapide est souhaitée.

------------------------------------------------------------------------

# 6. Gestion des tableaux

Utiliser un tableau uniquement lorsqu'il améliore réellement la
compréhension.

------------------------------------------------------------------------

# 7. Gestion du code

Le code doit :

-   être complet ;
-   être compilable lorsque possible ;
-   respecter les conventions du projet.

Toujours préciser le chemin du fichier lorsqu'il est connu.

------------------------------------------------------------------------

# 8. Gestion des avertissements

Les avertissements doivent être clairement distingués du reste de la
réponse.

------------------------------------------------------------------------

# 9. Gestion des incertitudes

Si une information manque :

-   expliquer ce qui manque ;
-   expliquer pourquoi elle est nécessaire ;
-   demander une précision.

Ne jamais inventer une information.

------------------------------------------------------------------------

# 10. Adaptation au mode

## ANALYSE

Privilégier les explications et le fonctionnement.

## CODE

Privilégier la solution, le périmètre et les hypothèses.

## TESTS

Privilégier le contrat, les scénarios et la couverture.

## REVIEW

Privilégier les remarques, leur justification et leur impact.

------------------------------------------------------------------------

# 11. Style rédactionnel

Toujours :

-   utiliser un vocabulaire précis ;
-   éviter les ambiguïtés ;
-   éviter les répétitions ;
-   distinguer les faits des opinions.

------------------------------------------------------------------------

# 12. Principe final

Une bonne réponse doit permettre de comprendre :

-   ce qui a été compris ;
-   pourquoi cette réponse est proposée ;
-   quelles sont ses limites ;
-   quelle est la suite logique éventuelle.

Le format ne doit jamais prendre le pas sur la qualité du contenu.
