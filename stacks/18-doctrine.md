# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 18-doctrine.md

------------------------------------------------------------------------

# 1. Objectif

Définir les règles d'utilisation de Doctrine ORM dans les projets
utilisant ce framework.

Ce document complète `16-php.md` et `17-symfony.md`.

------------------------------------------------------------------------

# 2. Principes fondamentaux

Doctrine est un ORM.

L'agent doit :

-   respecter les conventions du projet ;
-   privilégier la lisibilité des requêtes ;
-   limiter les accès inutiles à la base de données ;
-   préserver la cohérence du modèle de données.

Ne jamais utiliser Doctrine comme une simple couche SQL.

------------------------------------------------------------------------

# 3. Entités

Les entités représentent le domaine métier.

Elles doivent :

-   rester cohérentes ;
-   éviter la logique d'infrastructure ;
-   limiter les effets de bord.

Ne pas transformer une entité en service.

------------------------------------------------------------------------

# 4. Repositories

Les repositories sont responsables de l'accès aux données.

Ils doivent :

-   centraliser les requêtes complexes ;
-   éviter la duplication ;
-   retourner uniquement les données nécessaires.

Ne pas déplacer la logique métier dans les repositories.

------------------------------------------------------------------------

# 5. QueryBuilder

Privilégier QueryBuilder lorsque :

-   la requête est dynamique ;
-   la lisibilité est améliorée.

Éviter les requêtes inutilement complexes.

------------------------------------------------------------------------

# 6. Performances

Toujours vérifier :

-   les requêtes N+1 ;
-   les jointures inutiles ;
-   le volume de données chargé ;
-   la pagination lorsque nécessaire.

Ne jamais charger des collections complètes sans justification.

------------------------------------------------------------------------

# 7. Transactions

Utiliser une transaction lorsque plusieurs opérations doivent rester
atomiques.

Éviter les transactions trop longues.

------------------------------------------------------------------------

# 8. Persist et Flush

Appeler :

-   `persist()` uniquement pour les nouvelles entités lorsque nécessaire
    ;
-   `flush()` uniquement lorsque les modifications doivent être
    synchronisées.

Éviter les appels répétés à `flush()` dans une même unité de travail.

------------------------------------------------------------------------

# 9. Relations

Définir des relations cohérentes.

Vérifier :

-   cardinalité ;
-   propriétaire de la relation ;
-   chargement (lazy/eager) adapté au besoin.

------------------------------------------------------------------------

# 10. Migrations

Toute évolution du schéma doit être réalisée via les migrations du
projet.

Ne jamais modifier directement le schéma en production.

------------------------------------------------------------------------

# 11. Bonnes pratiques

Respecter :

-   conventions de nommage ;
-   mapping du projet ;
-   contraintes d'intégrité ;
-   responsabilités de chaque couche.

------------------------------------------------------------------------

# 12. Principe final

Doctrine doit être utilisé pour représenter et manipuler le modèle de
données du projet avec simplicité, cohérence et efficacité.

L'agent doit toujours privilégier une solution lisible, performante et
conforme aux conventions existantes.
