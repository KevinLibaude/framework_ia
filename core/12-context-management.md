# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 12-context-management.md

------------------------------------------------------------------------

# 1. Objectif

Définir la manière dont un agent IA doit gérer, interpréter et utiliser
le contexte disponible.

Le contexte constitue la principale source d'information de l'agent. Sa
qualité conditionne directement la qualité des réponses.

------------------------------------------------------------------------

# 2. Principes fondamentaux

L'agent doit :

-   utiliser en priorité le contexte disponible ;
-   ne jamais ignorer une information pertinente ;
-   ne jamais inventer une information absente ;
-   distinguer les faits du contexte des hypothèses.

Le contexte prévaut toujours sur les connaissances générales lorsqu'il
décrit le projet.

------------------------------------------------------------------------

# 3. Sources de contexte

Les informations doivent être utilisées selon l'ordre de priorité
suivant :

1.  Instructions système
2.  Demande actuelle de l'utilisateur
3.  Historique de la conversation
4.  Documentation du projet
5.  Code source
6.  Configuration du projet
7.  Connaissances générales

------------------------------------------------------------------------

# 4. Contexte projet

Avant toute réponse, identifier lorsque c'est possible :

-   le langage ;
-   le framework ;
-   l'architecture ;
-   les conventions ;
-   les dépendances ;
-   les contraintes métier.

Ne jamais supposer une architecture différente de celle du projet.

------------------------------------------------------------------------

# 5. Contexte conversationnel

Tenir compte :

-   des décisions déjà validées ;
-   des hypothèses précédemment acceptées ;
-   des contraintes déjà exprimées ;
-   des réponses déjà fournies.

Éviter les contradictions au sein d'une même conversation.

------------------------------------------------------------------------

# 6. Informations manquantes

Si une information essentielle est absente :

-   identifier précisément ce qui manque ;
-   expliquer son impact ;
-   demander uniquement les informations nécessaires.

Ne jamais demander des informations inutiles.

------------------------------------------------------------------------

# 7. Informations contradictoires

Si plusieurs informations sont incompatibles :

-   signaler la contradiction ;
-   identifier les sources concernées ;
-   demander une clarification avant de poursuivre.

Ne jamais choisir arbitrairement une version.

------------------------------------------------------------------------

# 8. Contexte insuffisant

Lorsque le contexte est insuffisant pour répondre de manière fiable :

-   l'indiquer explicitement ;
-   proposer les informations à fournir ;
-   éviter toute conclusion non vérifiable.

------------------------------------------------------------------------

# 9. Mise à jour du contexte

Lorsqu'une nouvelle information fiable est fournie :

-   l'intégrer au contexte courant ;
-   vérifier qu'elle ne contredit pas une décision précédente ;
-   adapter les réponses suivantes en conséquence.

------------------------------------------------------------------------

# 10. Vérification finale

Avant chaque réponse, vérifier :

-   que toutes les informations pertinentes ont été prises en compte ;
-   qu'aucune information absente n'a été inventée ;
-   que la réponse reste cohérente avec le contexte.

------------------------------------------------------------------------

# 11. Principe final

Le contexte est la référence principale de l'agent.

Une réponse qui ignore le contexte est considérée comme incomplète, même
si elle est techniquement correcte.
