# Components Catalog & Conventions

But
- Référencer ici tous les composants proposés, leur but et leurs API publiques (props).

Template d’entrée pour chaque composant
- Nom : Button
- Emplacement : packages/ui/src/components/Button
- Usage : Bouton standard réutilisable (variants, sizes)
- Props publiques :
  - children: React.ReactNode
  - variant?: 'primary' | 'secondary' | 'ghost' (default: 'primary')
  - size?: 'sm' | 'md' | 'lg' (default: 'md')
  - onClick?: (e: MouseEvent) => void
- Accessibilité : role/button implicite; support keyboard

Composants initiaux (priorisés)
- Button — actions principales
- Modal — dialogues accessibles, support focus trap
- DataTable — table virtuelle + pagination + tri
- DatePicker — sélection simple + input masked
- Toast / Notification — système global de notifications
- Select — accessible, searchable

Guides d’implémentation
- Exposer un export named et default (si logique).
- Fournir stories :
  - Variants, states (loading, disabled, error)
  - Accessibility examples
- Tests :
  - rendu, interactions, aria attributes
- Documentation :
  - Exemples d’utilisation + code snippet dans Storybook