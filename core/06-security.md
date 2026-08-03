# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 06-security.md

# 1. Objectif

Définir les contrôles de sécurité qu'un agent IA doit appliquer lors
d'une implémentation, d'une review ou d'une analyse.

La sécurité est une exigence transversale : elle ne doit jamais être
traitée comme une étape optionnelle.

------------------------------------------------------------------------

# 2. Principes

Toujours appliquer le principe du moindre privilège.

Valider toutes les entrées.

Ne jamais faire confiance aux données provenant d'une source externe.

Éviter toute fuite d'information sensible.

------------------------------------------------------------------------

# 3. Checklist générale

Avant de valider une proposition, vérifier lorsque c'est pertinent :

-   validation des entrées ;
-   authentification ;
-   autorisation ;
-   gestion des sessions ;
-   protection des secrets ;
-   journalisation adaptée ;
-   gestion des erreurs.

------------------------------------------------------------------------

# 4. Validation des entrées

Contrôler :

-   format ;
-   taille ;
-   type ;
-   plage de valeurs ;
-   caractères interdits.

Ne jamais supposer qu'une entrée est valide.

------------------------------------------------------------------------

# 5. Contrôle des accès

Vérifier :

-   authentification requise ;
-   permissions suffisantes ;
-   séparation des rôles ;
-   absence d'élévation de privilèges.

------------------------------------------------------------------------

# 6. Données sensibles

Ne jamais :

-   exposer un mot de passe ;
-   exposer une clé API ;
-   exposer un token ;
-   enregistrer des secrets dans le code source.

Privilégier les mécanismes de gestion des secrets du projet.

------------------------------------------------------------------------

# 7. Gestion des erreurs

Les messages d'erreur ne doivent pas révéler :

-   structure interne ;
-   chemins locaux ;
-   requêtes SQL ;
-   secrets ;
-   informations techniques inutiles.

------------------------------------------------------------------------

# 8. Journalisation

Les journaux doivent :

-   être utiles au diagnostic ;
-   éviter les données personnelles inutiles ;
-   éviter les secrets.

------------------------------------------------------------------------

# 9. Vulnérabilités courantes

Toujours rechercher lorsque le contexte s'y prête :

-   injections ;
-   XSS ;
-   CSRF ;
-   SSRF ;
-   désérialisation dangereuse ;
-   traversée de répertoires ;
-   téléversements non contrôlés ;
-   exposition d'informations.

------------------------------------------------------------------------

# 10. Dépendances

Avant de proposer une nouvelle dépendance :

-   vérifier qu'une solution existante ne répond pas déjà au besoin ;
-   privilégier les bibliothèques maintenues et reconnues ;
-   limiter les dépendances au strict nécessaire.

------------------------------------------------------------------------

# 11. Revue sécurité

Lors d'une review, distinguer :

-   vulnérabilité confirmée ;
-   risque potentiel ;
-   bonne pratique ;
-   recommandation.

Ne jamais présenter une hypothèse comme un fait.

------------------------------------------------------------------------

# 12. Principe final

Une fonctionnalité correcte mais vulnérable n'est pas une implémentation
acceptable.

La sécurité doit être prise en compte dès la conception et à chaque
étape du cycle de développement.
