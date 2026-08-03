# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 16-php.md

------------------------------------------------------------------------

# 1. Objectif

Définir les règles générales de développement PHP applicables à tous les
projets utilisant ce framework.

Ce document est indépendant d'un framework spécifique (Symfony, Laravel,
etc.).

------------------------------------------------------------------------

# 2. Compatibilité

Toujours respecter la version de PHP utilisée par le projet.

Ne jamais proposer une fonctionnalité indisponible sur cette version.

------------------------------------------------------------------------

# 3. Principes

Privilégier :

-   simplicité ;
-   lisibilité ;
-   typage ;
-   robustesse ;
-   maintenabilité.

Ne jamais complexifier une solution sans bénéfice démontré.

------------------------------------------------------------------------

# 4. Typage

Utiliser lorsque disponible :

-   `declare(strict_types=1);`
-   types scalaires ;
-   types de retour ;
-   propriétés typées ;
-   enums ;
-   readonly ;
-   promoted properties.

Éviter les types mixtes lorsque des types précis sont possibles.

------------------------------------------------------------------------

# 5. Fonctions et méthodes

Chaque fonction doit :

-   avoir une responsabilité unique ;
-   posséder une signature explicite ;
-   limiter les effets de bord ;
-   retourner un résultat cohérent.

Limiter le nombre de paramètres lorsque cela améliore la lisibilité.

------------------------------------------------------------------------

# 6. Exceptions

Privilégier les exceptions pour les situations exceptionnelles.

Ne jamais utiliser une exception pour contrôler un flux normal.

Utiliser des exceptions spécifiques lorsque cela améliore la
compréhension.

------------------------------------------------------------------------

# 7. Collections et tableaux

Privilégier :

-   des structures simples ;
-   des clés explicites ;
-   des objets lorsque le domaine le justifie.

Éviter les tableaux associatifs complexes servant d'objets implicites.

------------------------------------------------------------------------

# 8. Programmation orientée objet

Respecter lorsque pertinent :

-   encapsulation ;
-   composition avant héritage ;
-   responsabilité unique ;
-   interfaces lorsque nécessaires.

Ne pas créer d'abstractions prématurées.

------------------------------------------------------------------------

# 9. Style de code

Respecter :

-   PSR-12 ;
-   conventions du projet ;
-   nommage explicite.

Éviter les commentaires décrivant simplement ce que fait le code.

------------------------------------------------------------------------

# 10. Performance

Éviter :

-   calculs redondants ;
-   copies inutiles ;
-   parcours multiples d'une même collection ;
-   optimisations prématurées.

------------------------------------------------------------------------

# 11. Sécurité

Toujours :

-   valider les entrées ;
-   échapper les sorties lorsque nécessaire ;
-   protéger les données sensibles ;
-   éviter les constructions dangereuses (`eval`, désérialisation non
    maîtrisée, etc.).

------------------------------------------------------------------------

# 12. Principe final

Le code PHP doit rester explicite, fortement typé lorsque possible,
conforme aux standards du projet et facile à faire évoluer.
