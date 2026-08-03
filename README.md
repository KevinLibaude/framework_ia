# IA Development Framework

> Framework modulaire de gouvernance pour agents IA de développement logiciel.

## Version

Version actuelle : **1.0.0**

## Licence

License: CC BY-NC-SA 4.0
Commercial use prohibited without prior written permission.

## Objectif

IA Development Framework définit un ensemble de règles permettant d'encadrer le comportement d'un agent IA intervenant sur un projet logiciel.

Le framework vise à produire des réponses et des modifications :

- fiables ;
- prévisibles ;
- limitées au périmètre demandé ;
- cohérentes avec l'architecture existante ;
- réutilisables entre plusieurs projets et plusieurs technologies.

Il ne dépend pas d'un modèle particulier. Il peut servir de base pour Codex, ChatGPT, Claude Code, Gemini ou tout autre agent capable de lire des instructions Markdown.

## Principes fondamentaux

Le framework impose notamment les règles suivantes :

- comprendre avant de modifier ;
- vérifier avant d'affirmer ;
- ne jamais inventer une information absente ;
- respecter les conventions et l'architecture existantes ;
- appliquer la modification minimale nécessaire ;
- distinguer clairement analyse, code, tests et review ;
- demander une validation avant les modifications significatives ;
- signaler explicitement les hypothèses, limites et incertitudes.

## Structure du dépôt

```text
ia-development-framework/
├── README.md
├── CHANGELOG.md
├── VERSION
│
├── core/
│   ├── 00-core.md
│   ├── 01-modes.md
│   ├── 02-workflow.md
│   ├── 03-planning.md
│   ├── 04-review.md
│   ├── 05-testing.md
│   ├── 06-security.md
│   ├── 07-performance.md
│   ├── 08-maintainability.md
│   ├── 09-architecture.md
│   ├── 10-response-format.md
│   ├── 11-reasoning.md
│   ├── 12-context-management.md
│   ├── 13-decision-making.md
│   ├── 14-error-handling.md
│   └── 15-project-rules.md
│
├── stacks/
│   ├── php.md
│   ├── symfony.md
│   └── doctrine.md
│
├── projects/
│   └── project-template.md
│
└── integrations/
    └── AGENTS-template.md
```

## Documents disponibles

### Noyau générique

| Document | Rôle |
|---|---|
| `00-core.md` | Principes fondamentaux et hiérarchie des priorités |
| `01-modes.md` | Modes ANALYSE, CODE, TESTS, REVIEW et REVIEW+PATCH |
| `02-workflow.md` | Processus décisionnel général |
| `03-planning.md` | Construction et validation des plans |
| `04-review.md` | Méthodologie de revue de code |
| `05-testing.md` | Stratégie de tests fondée sur le contrat observable |
| `06-security.md` | Contrôles de sécurité transversaux |
| `07-performance.md` | Méthode d'analyse des performances |
| `08-maintainability.md` | Lisibilité, cohésion, couplage et dette technique |
| `09-architecture.md` | Principes d'architecture et de dépendances |
| `10-response-format.md` | Format et structure des réponses |
| `11-reasoning.md` | Cadre d'analyse et de justification |
| `12-context-management.md` | Gestion des sources de contexte |
| `13-decision-making.md` | Critères de prise de décision |
| `14-error-handling.md` | Gestion des erreurs, limites et contradictions |
| `15-project-rules.md` | Règles de gouvernance propres aux projets |

### Règles techniques

| Document | Rôle |
|---|---|
| `php.md` | Règles générales de développement PHP |
| `symfony.md` | Règles générales de développement Symfony |
| `doctrine.md` | Règles générales d'utilisation de Doctrine ORM |

### Modèle projet

| Document | Rôle |
|---|---|
| `project-template.md` | Modèle permettant de documenter un projet |

## Ordre de chargement recommandé

Un agent doit charger les règles dans cet ordre :

1. documents du noyau `core/` ;
2. règles techniques nécessaires dans `stacks/` ;
3. règles spécifiques au projet ;
4. décisions et contraintes du projet ;
5. demande utilisateur.

Exemple pour un projet Symfony :

```text
core/*
+
stacks/php.md
+
stacks/symfony.md
+
stacks/doctrine.md
+
règles du projet
```

## Priorité des règles

En cas de conflit, appliquer l'ordre suivant :

1. instructions système de l'outil ;
2. demande explicite de l'utilisateur ;
3. décisions validées du projet ;
4. contraintes du projet ;
5. règles du projet ;
6. règles techniques ;
7. règles génériques du framework ;
8. préférences générales de l'agent.

Une règle spécifique peut préciser une règle générique. Elle ne doit pas la contredire silencieusement.

## Utilisation avec Git

Le framework peut être conservé dans un dépôt Git indépendant puis ajouté aux projets comme sous-module.

Exemple :

```bash
git submodule add git@github.com:VOTRE_COMPTE/ia-development-framework.git .ai/framework
```

Dans le projet principal :

```text
mon-projet/
├── .ai/
│   ├── framework/    # sous-module Git
│   └── project/      # règles propres au projet
├── AGENTS.md
├── src/
└── tests/
```

Pour cloner un projet avec ses sous-modules :

```bash
git clone --recurse-submodules git@github.com:VOTRE_COMPTE/mon-projet.git
```

Pour initialiser les sous-modules après un clone classique :

```bash
git submodule update --init --recursive
```

## Fichier d'intégration

Chaque projet devrait contenir un fichier court tel que `AGENTS.md`.

Son rôle est uniquement d'indiquer :

- où se trouve le framework ;
- quels documents doivent être lus ;
- dans quel ordre ;
- où se trouvent les règles spécifiques du projet.

Il ne doit pas recopier l'intégralité des règles.

## Versionnement

Le framework suit le versionnement sémantique :

```text
MAJEURE.MINEURE.CORRECTIF
```

- **MAJEURE** : changement incompatible ou modification importante de gouvernance ;
- **MINEURE** : ajout compatible de règles ou de capacités ;
- **CORRECTIF** : correction, clarification ou amélioration sans changement de comportement majeur.

La version courante est stockée dans le fichier `VERSION`.

## Contribution

Toute nouvelle règle doit être placée au bon niveau :

- dans `core/` si elle est universelle ;
- dans `stacks/` si elle dépend d'une technologie ;
- dans les règles projet si elle dépend du métier ou du dépôt ;
- dans `integrations/` si elle dépend de l'outil IA.

La même règle ne doit pas être dupliquée dans plusieurs niveaux.

## Statut

Cette version constitue le **MVP 1.0.0** du framework.

Elle fournit :

- un noyau générique complet ;
- un profil PHP ;
- un profil Symfony ;
- un profil Doctrine ;
- un modèle de règles projet.

## Licence

La licence du projet doit être définie dans un fichier `LICENSE` avant publication publique.
