# Coding Rules / Conventions

Langage & style
- TypeScript strict (tsconfig "strict": true).
- Utiliser React 18 et le JSX transform moderne.
- Pas de any sauf justification documentée.
- Favoriser les types explicites pour props et fonctions publiques.

Naming
- Composants : PascalCase (Button, ModalDialog).
- Fichiers : ComponentName.tsx (et ComponentName.test.tsx, ComponentName.stories.tsx).
- Hooks : usePascalCase (useToggle, useDebouncedValue).
- Classes CSS utilitaires : Tailwind (éviter styles inline larges).

Structure d’un composant
- Dossier : src/components/ComponentName/
  - ComponentName.tsx
  - ComponentName.module.css (rare, si besoin)
  - ComponentName.stories.tsx
  - ComponentName.test.tsx
  - index.ts (export par défaut)

Accessibilité (a11y)
- Les composants interactifs doivent :
  - Supporter le keyboard navigation
  - Avoir attributs ARIA pertinents si nécessaire
  - Être testés avec @testing-library/user-event pour interactions

Tests
- Écrire tests unitaires pour comportements critiques.
- Coverage minimal recommandé : tests pour props publiques, events, et rendu conditionnel.
- Utiliser Vitest + @testing-library/react.

Lint / Formatting
- ESLint + Prettier configurés.
- Exécuter `pnpm -w run lint` avant push.

Commits & PRs
- Convention de commit (optionnel) : Conventional Commits (feat/fix/chore/docs)
- PR doit inclure :
  - Description courte
  - Liens vers stories/demo
  - Checklist : tests green, lint green, storybook build