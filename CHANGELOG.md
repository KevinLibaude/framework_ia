# Changelog

Toutes les évolutions notables de IA Development Framework sont documentées dans ce fichier.

Le format est inspiré de Keep a Changelog et le projet suit le versionnement sémantique.

## [1.0.0] - 2026-08-03

### Ajouté

#### Gouvernance générale

- Ajout du document `00-core.md`.
- Ajout de la hiérarchie des priorités.
- Ajout du principe de moindre modification.
- Ajout de la règle interdisant l'invention d'informations absentes.
- Ajout des règles de respect de l'architecture et des conventions existantes.

#### Modes de fonctionnement

- Ajout des modes `ANALYSE`, `CODE`, `TESTS`, `REVIEW` et `REVIEW+PATCH`.
- Ajout des responsabilités, autorisations et interdictions propres à chaque mode.
- Ajout des règles de changement de mode.

#### Processus de travail

- Ajout du workflow général de traitement des demandes.
- Ajout des règles de délimitation du périmètre.
- Ajout des critères déterminant quand répondre, demander une précision ou proposer un plan.
- Ajout des règles de validation avant modification significative.

#### Qualité

- Ajout de la méthodologie de review.
- Ajout de la stratégie de tests fondée sur le contrat observable.
- Ajout des règles de sécurité.
- Ajout de la méthode d'analyse des performances.
- Ajout des règles de maintenabilité.
- Ajout des principes d'architecture.

#### Communication et décision

- Ajout du format de réponse.
- Ajout du cadre de raisonnement.
- Ajout des règles de gestion du contexte.
- Ajout de la méthode de prise de décision.
- Ajout de la gestion des erreurs, limites et contradictions.

#### Règles projet

- Ajout du document de gouvernance des règles projet.
- Ajout d'un modèle standard de description de projet.
- Ajout des sections pour les décisions, contraintes, exclusions et références.

#### Technologies

- Ajout des règles générales PHP.
- Ajout des règles générales Symfony.
- Ajout des règles générales Doctrine ORM.

### Structure

- Définition d'une architecture modulaire séparant :
  - le noyau générique ;
  - les règles techniques ;
  - les règles projet ;
  - les intégrations propres aux agents IA.

### Notes

- Cette version constitue le premier MVP stable.
- Les documents restent volontairement généraux.
- Les futurs profils techniques pourront étendre le framework sans modifier le noyau.
