# UI / UX Guidelines

Principes généraux
- Cohérence : même espacement, typographie et couleurs pour composants similaires.
- Accessibilité : couleurs avec contrast >= 4.5:1, focus visible, labels explicites.
- Simplicité : APIs des composants simples et prévisibles.
- Responsive : composants adaptent layout (mobile → desktop).

Design tokens
- Utiliser Tailwind tokens par défaut (colors, spacing, font-size).
- Documenter tokens si theming futur.

Composant — bonnes pratiques
- Boutons : un primary, secondary et ghost par défaut.
- Modals : trap focus, restore focus on close, close on ESC.
- Inputs : associer label via htmlFor, support aria-invalid.

Animations
- Animations légères et respectueuses (prefers-reduced-motion).
- Utiliser transitions CSS simples (opacity, transform).

Documentation UX
- Chaque story doit inclure un exemple d’utilisation, states (disabled, loading), et recommandations d’accessibilité.