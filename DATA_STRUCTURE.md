# Data Structure & Directory Layout

Structure racine (exemple)
- package.json
- pnpm-workspace.yaml
- packages/
  - ui/
    - package.json
    - src/
      - components/
        - Button/
          - Button.tsx
          - Button.test.tsx
          - Button.stories.tsx
        - Modal/
      - styles/
      - index.ts
    - tsconfig.build.json
  - storybook/
    - package.json
    - .storybook/

Fichiers TypeScript & Typage
- Types partagés : créer un dossier `packages/ui/src/types/` pour types réutilisés.
- Props publiques : toujours exporter l’interface `ComponentNameProps`.

State & data flow (composants)
- Eviter état global dans la librairie.
- Si besoin, exposer providers légers (ex: ToastProvider) mais garder la logique de stockage à l'app qui intègre la lib.

Naming des assets
- images/ svgs/ icons/ dans chaque package si nécessaire
- pas d’assets lourds : préférer CDNs ou usage par l’app