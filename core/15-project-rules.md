# IA Development Framework

> **Version :** 1.0.0\
> **Document :** 15-project-rules.md

------------------------------------------------------------------------

# 1. Objectif

Définir un modèle standard permettant à un agent IA de comprendre
rapidement les spécificités d'un projet.

Chaque projet utilisant ce framework devrait disposer de son propre
document basé sur ce modèle.

------------------------------------------------------------------------

# 2. Identité du projet

Documenter :

-   nom du projet ;
-   objectif ;
-   domaine fonctionnel ;
-   public cible ;
-   état du projet (prototype, développement, production).

------------------------------------------------------------------------

# 3. Stack technique

Décrire notamment :

-   langage(s) ;
-   framework(s) ;
-   base(s) de données ;
-   outils principaux ;
-   dépendances majeures.

L'agent doit privilégier les technologies déjà utilisées.

------------------------------------------------------------------------

# 4. Architecture

Préciser :

-   architecture retenue ;
-   organisation des dossiers ;
-   conventions de nommage ;
-   responsabilités des couches ;
-   patterns utilisés.

Ne pas proposer une architecture différente sans demande explicite.

------------------------------------------------------------------------

# 5. Règles métier

Lister les règles métier structurantes.

Chaque règle doit être :

-   explicite ;
-   non ambiguë ;
-   vérifiable.

Ne jamais inventer une règle métier absente.

------------------------------------------------------------------------

# 6. Conventions de développement

Documenter notamment :

-   style de code ;
-   outils de qualité ;
-   stratégie de tests ;
-   politique de dépendances ;
-   règles de revue de code.

------------------------------------------------------------------------

# 7. Contraintes

Identifier les contraintes importantes :

-   techniques ;
-   fonctionnelles ;
-   réglementaires ;
-   performances ;
-   sécurité.

Ces contraintes priment sur les préférences de l'agent.

------------------------------------------------------------------------

# 8. Décisions validées

Conserver les décisions importantes déjà prises.

Chaque décision devrait contenir :

-   le sujet ;
-   la décision ;
-   la justification ;
-   la date si disponible.

Ces décisions font autorité tant qu'elles ne sont pas remplacées.

------------------------------------------------------------------------

# 9. Éléments exclus

Documenter explicitement ce qui est hors périmètre.

L'agent ne doit pas proposer spontanément ces éléments.

------------------------------------------------------------------------

# 10. Évolution

Toute nouvelle règle projet doit :

-   être compatible avec les règles existantes ;
-   être documentée ;
-   ne pas contredire une décision validée.

En cas de contradiction, demander une clarification.

------------------------------------------------------------------------

# 11. Vérification

Avant chaque réponse, vérifier que la proposition :

-   respecte les règles du projet ;
-   respecte les décisions validées ;
-   respecte les contraintes ;
-   ne sort pas du périmètre.

------------------------------------------------------------------------

# 12. Principe final

Le document de projet constitue la référence spécifique du dépôt.

En cas de conflit avec une préférence de l'agent, les règles du projet
prévalent, sous réserve des instructions de plus haute priorité.
