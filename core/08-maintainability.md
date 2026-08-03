# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 08-maintainability.md

# 1. Objectif

Définir les règles garantissant qu'un logiciel reste simple à
comprendre, à modifier et à faire évoluer.

La maintenabilité est une qualité de conception, pas une étape finale.

------------------------------------------------------------------------

# 2. Principes

Privilégier :

-   simplicité ;
-   cohérence ;
-   faible couplage ;
-   forte cohésion ;
-   responsabilités clairement définies.

Une solution légèrement moins optimisée mais nettement plus
compréhensible est généralement préférable.

------------------------------------------------------------------------

# 3. Responsabilité unique

Chaque composant doit avoir une responsabilité principale identifiable.

Éviter les classes, fonctions ou modules qui cumulent plusieurs rôles.

------------------------------------------------------------------------

# 4. Lisibilité

Favoriser :

-   noms explicites ;
-   fonctions courtes ;
-   structure régulière ;
-   flux d'exécution simple.

Le code doit être compréhensible sans commentaire excessif.

------------------------------------------------------------------------

# 5. Couplage

Limiter les dépendances entre composants.

Éviter :

-   dépendances circulaires ;
-   dépendances inutiles ;
-   accès directs à des composants internes lorsque des abstractions
    existent.

------------------------------------------------------------------------

# 6. Cohésion

Regrouper les éléments ayant la même responsabilité.

Ne pas mélanger logique métier, accès aux données, présentation et
infrastructure.

------------------------------------------------------------------------

# 7. Duplication

Éliminer la duplication métier lorsque celle-ci augmente le coût de
maintenance.

Ne pas factoriser prématurément quelques lignes si cela nuit à la
compréhension.

------------------------------------------------------------------------

# 8. Dette technique

Classer la dette :

-   Critique
-   Importante
-   Modérée
-   Mineure

Toujours distinguer un bug d'une dette technique.

------------------------------------------------------------------------

# 9. Évolutivité

Avant une modification, vérifier :

-   son impact sur les composants voisins ;
-   sa compatibilité avec l'architecture existante ;
-   la facilité des évolutions futures.

Éviter les solutions qui résolvent uniquement le besoin immédiat au prix
d'une complexité durable.

------------------------------------------------------------------------

# 10. Refactoring

Un refactoring doit :

-   préserver le comportement observable ;
-   réduire la complexité ;
-   améliorer la lisibilité.

Ne jamais effectuer un refactoring hors périmètre sans demande
explicite.

------------------------------------------------------------------------

# 11. Documentation

Documenter :

-   les décisions non évidentes ;
-   les choix d'architecture ;
-   les contraintes importantes.

Éviter les commentaires décrivant simplement ce que le code fait.

------------------------------------------------------------------------

# 12. Revue de maintenabilité

Évaluer notamment :

-   lisibilité ;
-   découpage ;
-   nommage ;
-   responsabilités ;
-   couplage ;
-   duplication ;
-   évolutivité.

------------------------------------------------------------------------

# 13. Principe final

Le meilleur code est celui qu'un autre développeur peut comprendre,
corriger et faire évoluer avec un minimum d'effort, sans introduire de
régressions.
