# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 05-testing.md

# 1. Objectif

Définir la stratégie de tests qu'un agent IA doit appliquer
indépendamment du langage, du framework ou de l'outil de test.

Les tests doivent vérifier le comportement observable d'un système,
jamais son implémentation interne.

------------------------------------------------------------------------

# 2. Principes fondamentaux

Les tests doivent être :

-   fiables ;
-   reproductibles ;
-   indépendants ;
-   déterministes ;
-   lisibles.

Un test ne doit jamais dépendre de l'ordre d'exécution d'un autre test.

------------------------------------------------------------------------

# 3. Source de vérité

Les tests sont construits à partir de :

1.  la demande utilisateur ;
2.  le contrat fonctionnel ;
3.  les spécifications ;
4.  la documentation.

Ne jamais déduire une règle métier à partir de l'implémentation
existante.

------------------------------------------------------------------------

# 4. Ce qu'un test doit vérifier

Un test peut vérifier :

-   les entrées acceptées ;
-   les sorties attendues ;
-   les erreurs attendues ;
-   les permissions ;
-   les changements d'état observables ;
-   les événements publics ;
-   les effets visibles.

Ne jamais tester :

-   des méthodes privées ;
-   l'ordre interne des appels ;
-   des détails d'implémentation.

------------------------------------------------------------------------

# 5. Pyramide des tests

Privilégier :

1.  Tests unitaires
2.  Tests d'intégration
3.  Tests d'API ou composants
4.  Tests end-to-end

Choisir le niveau le plus bas permettant de valider le contrat.

------------------------------------------------------------------------

# 6. Cas à couvrir

Lorsque c'est pertinent, couvrir :

-   cas nominal ;
-   valeurs limites ;
-   entrées invalides ;
-   erreurs attendues ;
-   permissions ;
-   cas de non-régression.

Ne pas multiplier des scénarios redondants.

------------------------------------------------------------------------

# 7. Qualité des tests

Un bon test :

-   vérifie un comportement unique ;
-   possède un nom explicite ;
-   prépare uniquement les données nécessaires ;
-   ne dépend pas d'un état externe non maîtrisé.

------------------------------------------------------------------------

# 8. Interdictions

En mode TESTS, ne jamais :

-   modifier le code de production ;
-   corriger une fonctionnalité ;
-   inventer un comportement métier ;
-   écrire des tests basés sur les détails internes.

------------------------------------------------------------------------

# 9. Couverture

La couverture recherchée est fonctionnelle, pas uniquement quantitative.

Un pourcentage élevé de couverture ne garantit pas la qualité.

------------------------------------------------------------------------

# 10. Principe final

Chaque test doit répondre à une question simple :

> "Quel comportement observable ce test valide-t-il ?"

Si la réponse n'est pas claire, le test doit être repensé.
