# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 07-performance.md

# 1. Objectif

Définir la méthodologie d'analyse des performances qu'un agent IA doit
appliquer lors d'une implémentation, d'une review ou d'une analyse.

L'objectif est de produire un code suffisamment performant tout en
restant simple, lisible et maintenable.

------------------------------------------------------------------------

# 2. Principes fondamentaux

Les performances ne doivent jamais être optimisées au détriment :

-   de la fiabilité ;
-   de la sécurité ;
-   de la lisibilité ;
-   de la maintenabilité.

Appliquer le principe :

> Mesurer avant d'optimiser.

Ne jamais proposer une optimisation uniquement par intuition.

------------------------------------------------------------------------

# 3. Ordre d'analyse

Toujours analyser les performances dans l'ordre suivant :

1.  Algorithmes
2.  Accès aux données
3.  Entrées / Sorties (I/O)
4.  Réseau
5.  Mémoire
6.  Framework
7.  Infrastructure

Ne jamais commencer par des micro-optimisations.

------------------------------------------------------------------------

# 4. Algorithmes

Vérifier :

-   complexité temporelle ;
-   complexité mémoire ;
-   boucles imbriquées inutiles ;
-   calculs redondants.

Privilégier les algorithmes simples et adaptés au volume de données
attendu.

------------------------------------------------------------------------

# 5. Base de données

Contrôler lorsque c'est pertinent :

-   requêtes N+1 ;
-   requêtes répétées ;
-   index manquants ;
-   jointures inutiles ;
-   pagination ;
-   volume de données récupéré.

Ne jamais charger plus de données que nécessaire.

------------------------------------------------------------------------

# 6. Mémoire

Limiter :

-   les copies inutiles ;
-   les collections surdimensionnées ;
-   les objets temporaires inutiles ;
-   les chargements complets lorsque le traitement peut être réalisé par
    flux.

------------------------------------------------------------------------

# 7. Réseau

Réduire :

-   le nombre d'appels ;
-   les appels synchrones inutiles ;
-   les transferts de données inutiles.

Privilégier la mise en cache lorsque cela est pertinent.

------------------------------------------------------------------------

# 8. Cache

Avant de proposer un cache, vérifier :

-   que le calcul est réellement coûteux ;
-   que les données sont suffisamment stables ;
-   que la stratégie d'invalidation est définie.

Ne jamais utiliser un cache pour masquer un problème de conception.

------------------------------------------------------------------------

# 9. Scalabilité

Lorsque le contexte l'exige, analyser :

-   comportement avec une montée en charge ;
-   contention ;
-   concurrence ;
-   parallélisme ;
-   consommation des ressources.

------------------------------------------------------------------------

# 10. Mesures

Privilégier :

-   les profils d'exécution ;
-   les métriques ;
-   les benchmarks ;
-   les mesures reproductibles.

Ne jamais présenter une estimation comme une mesure réelle.

------------------------------------------------------------------------

# 11. Revue de performance

Lors d'une review, distinguer :

-   problème confirmé ;
-   risque potentiel ;
-   optimisation facultative.

Chaque remarque doit être justifiée.

------------------------------------------------------------------------

# 12. Principe final

Le meilleur code n'est pas le plus rapide.

Le meilleur code est celui qui offre le meilleur équilibre entre
performances, simplicité, sécurité et maintenabilité.
