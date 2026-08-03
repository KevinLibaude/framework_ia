# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 04-review.md

# 1. Objectif

Définir la méthodologie de revue de code appliquée par un agent IA.

Une review a pour objectif d'identifier les problèmes, les risques et
les incohérences sans modifier directement le code.

------------------------------------------------------------------------

# 2. Principes

Une review doit être :

-   factuelle ;
-   reproductible ;
-   argumentée ;
-   limitée aux éléments observables.

Ne jamais formuler une remarque sans pouvoir la justifier.

------------------------------------------------------------------------

# 3. Ordre d'analyse

Toujours examiner les points suivants dans cet ordre :

1.  Respect du besoin fonctionnel.
2.  Respect du périmètre demandé.
3.  Risques de régression.
4.  Sécurité.
5.  Gestion des erreurs.
6.  Performance.
7.  Maintenabilité.
8.  Lisibilité.
9.  Conventions du projet.

------------------------------------------------------------------------

# 4. Classification

## Critique

Problème pouvant provoquer une faille de sécurité, une corruption de
données ou un comportement dangereux.

## Bloquant

Empêche le fonctionnement attendu ou le déploiement.

## Important

Fonctionne mais présente un risque significatif.

## Mineur

Amélioration souhaitable sans impact majeur.

## Style

Suggestion de cohérence ou de lisibilité.

------------------------------------------------------------------------

# 5. Contenu d'une remarque

Chaque remarque doit contenir :

-   Localisation (fichier, classe, méthode, bloc) ;
-   Description du problème ;
-   Impact ;
-   Justification ;
-   Piste de correction (sans code complet en mode REVIEW).

------------------------------------------------------------------------

# 6. Points de contrôle

## Fonctionnel

-   Le comportement respecte-t-il la demande ?

## Architecture

-   Les conventions du projet sont-elles respectées ?

## Sécurité

-   Validation des entrées
-   Contrôle des accès
-   Gestion des secrets
-   Injections

## Performance

-   Requêtes inutiles
-   Complexité excessive
-   Traitements redondants

## Robustesse

-   Gestion des erreurs
-   Cas limites
-   Valeurs nulles
-   Exceptions

## Lisibilité

-   Nommage
-   Découpage
-   Responsabilité des composants

------------------------------------------------------------------------

# 7. Ce qui est interdit

En mode REVIEW, ne jamais :

-   modifier le code ;
-   fournir un patch complet ;
-   réécrire une implémentation ;
-   élargir le périmètre de la review.

------------------------------------------------------------------------

# 8. Conclusion

La conclusion doit être l'une des suivantes :

-   Acceptable
-   Acceptable après corrections
-   À revoir avant intégration

La conclusion doit être cohérente avec les remarques formulées.

------------------------------------------------------------------------

# 9. Principe final

Une review doit aider à prendre une décision, pas à réécrire le projet.
