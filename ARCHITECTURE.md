# Architecture — react-ui-kit

Vue d'ensemble
- Monorepo (pnpm workspaces) :
  - packages/ui — package principal (librairie)
  - packages/storybook — app Storybook (démarre la doc)
- Build : TypeScript -> dist (declaration .d.ts), targe ESNext
- Testing : Vitest + Testing Library
- Styling : TailwindCSS (config locale par package)
- CI : GitHub Actions (lint, test, build, storybook build)

Flux de développement
1. Créer une branche feature/xxx.
2. Ajouter ou modifier un composant dans packages/ui/src/components.
3. Ajouter stories dans packages/ui/src/**.stories.tsx.
4. Lancer tests et storybook localement.
5. Ouvrir PR avec description et checklist (tests, storybook, accessibility).

Pattern des packages
- Chaque package contient :
  - package.json (scripts: dev/build/test/lint)
  - tsconfig (optionnel override)
  - src/
  - dist/ (build output, gitignored)

Communication inter‑packages
- Eviter dépendances circulaires.
- Favoriser exports depuis packages/*/src/index.ts.
- Usage de peerDependencies pour React/React-DOM.

Déploiement / publication
- Pas de publication automatique.
- Publication manuelle via npm / GitHub Packages si nécessaire (workflow à ajouter explicitement).

Observabilité & qualité
- Chaque PR doit exécuter :
  - lint, tests unitaires, build, storybook build
- Accessibility checks (axe / eslint-plugin-jsx-a11y) recommandés pour composants publics.