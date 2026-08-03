# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 17-symfony.md

------------------------------------------------------------------------

# 1. Objectif

Définir les règles de développement applicables aux projets Symfony.

Ce document complète `16-php.md` et s'applique à toute implémentation
utilisant Symfony.

------------------------------------------------------------------------

# 2. Principes fondamentaux

Toujours privilégier :

-   les composants natifs de Symfony ;
-   les conventions du framework ;
-   l'injection de dépendances ;
-   une architecture cohérente avec le projet.

Ne jamais réimplémenter une fonctionnalité déjà fournie par Symfony sans
justification.

------------------------------------------------------------------------

# 3. Services

Les services doivent :

-   être injectés, jamais instanciés directement ;
-   avoir une responsabilité unique ;
-   contenir la logique métier.

Éviter les services "fourre-tout".

------------------------------------------------------------------------

# 4. Contrôleurs

Les contrôleurs doivent :

-   rester légers ;
-   orchestrer les traitements ;
-   déléguer la logique métier aux services ;
-   retourner une réponse adaptée.

Ne jamais déplacer la logique métier dans un contrôleur.

------------------------------------------------------------------------

# 5. Routage

Respecter les conventions du projet.

Définir des routes explicites.

Éviter les doublons et les comportements implicites.

------------------------------------------------------------------------

# 6. Validation

Utiliser le composant Validator lorsque cela est pertinent.

Centraliser les règles de validation.

Ne pas dupliquer les validations métier.

------------------------------------------------------------------------

# 7. Doctrine

Utiliser Doctrine conformément aux conventions du projet.

Éviter :

-   les requêtes N+1 ;
-   les flush inutiles ;
-   les accès directs à la base depuis les contrôleurs.

La logique métier ne doit pas être portée par les entités.

------------------------------------------------------------------------

# 8. Sécurité

Utiliser les composants Symfony Security.

Respecter :

-   authentification ;
-   autorisation ;
-   rôles ;
-   voters lorsque le projet les utilise.

Ne jamais contourner les mécanismes de sécurité du framework.

------------------------------------------------------------------------

# 9. Événements

Utiliser EventDispatcher uniquement lorsqu'un découplage apporte une
réelle valeur.

Éviter les événements pour des traitements simples.

------------------------------------------------------------------------

# 10. Messenger

Utiliser Messenger pour les traitements asynchrones lorsque le projet le
prévoit.

Ne pas transformer tous les traitements en messages.

------------------------------------------------------------------------

# 11. Configuration

Privilégier :

-   les paramètres ;
-   les variables d'environnement ;
-   la configuration Symfony.

Ne jamais coder en dur des informations de configuration.

------------------------------------------------------------------------

# 12. Console

Les commandes Console doivent :

-   avoir une responsabilité claire ;
-   produire des messages explicites ;
-   déléguer la logique métier aux services.

------------------------------------------------------------------------

# 13. Cache

Utiliser le composant Cache uniquement lorsqu'il apporte un bénéfice
démontré.

Prévoir une stratégie d'invalidation.

------------------------------------------------------------------------

# 14. Bonnes pratiques

Respecter :

-   autowiring ;
-   autoconfiguration ;
-   conventions de nommage ;
-   structure du projet.

Avant de créer un nouveau composant, vérifier qu'un composant Symfony
existant ne répond pas déjà au besoin.

------------------------------------------------------------------------

# 15. Principe final

L'agent doit développer en s'appuyant sur les conventions et les
composants officiels de Symfony.

Le code proposé doit s'intégrer naturellement au projet sans introduire
de complexité inutile.
