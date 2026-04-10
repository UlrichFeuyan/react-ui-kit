# react-ui-kit

Scaffold pour la bibliothèque de composants UI (monorepo).

Résumé
- Monorepo avec pnpm workspaces
- packages/ui : composants React (TypeScript strict)
- packages/storybook : documentation interactive (Storybook)
- CI : GitHub Actions (lint, test, build, storybook build)
- Licence : MIT

Commencer localement
1. Installer pnpm via Corepack :
   - corepack enable
   - corepack prepare pnpm@latest --activate
2. Installer dépendances :
   - pnpm install
3. Démarrer Storybook :
   - pnpm storybook:dev
4. Lancer tests :
   - pnpm -w run test
5. Build :
   - pnpm -w run build
6. Construire Storybook statique :
   - pnpm storybook:build

Structure du repo
- Voir `DATA_STRUCTURE.md` et `ARCHITECTURE.md` pour la structure détaillée.
- Voir `COMPONENTS.md` pour la liste et l’API des composants.
- Voir `UI_UX_GUIDELINES.md` pour les règles de conception.

Utilisation des fichiers .md
- Ces fichiers servent d’input pour les agents et de guide pour les contributors :
  - `ARCHITECTURE.md` décrit la structure et le flux.
  - `COMPONENTS.md` décrit les APIs des composants.
  - `CODING_RULES.md` liste les conventions.
  - `TASKS.md` contient la roadmap et sprints.

Contributing
- Voir `CONTRIBUTING.md` (s’il existe) pour guidelines PR / issues.

Maintainers
- @UlrichFeuyan