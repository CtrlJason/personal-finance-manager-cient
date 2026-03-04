# Arquitectura del Proyecto

## Frontend — Next.js

```
src/
├── app/
│   ├── layout.tsx
│   ├── page.tsx                  ← login
│   └── dashboard/
│       ├── layout.tsx            ← navbar + sidebar
│       ├── page.tsx              ← resumen general
│       ├── accounts/
│       │   └── page.tsx
│       ├── movements/
│       │   └── page.tsx
│       ├── savings/
│       │   └── page.tsx
│       └── recurring/
│           └── page.tsx
├── components/
│   ├── ui/                       ← componentes genéricos
│   │   ├── Button.tsx
│   │   ├── Input.tsx
│   │   ├── Modal.tsx
│   │   └── Card.tsx
│   ├── modules/                  ← componentes específicos por sección
│   │   ├── accounts/
│   │   ├── movements/
│   │   ├── savings/
│   │   └── recurring/
│   └── layout/
│       ├── Navbar.tsx            ← incluye notificaciones
│       └── Sidebar.tsx
├── services/                     ← llamadas a la API
│   ├── auth.service.ts
│   ├── accounts.service.ts
│   ├── categories.service.ts
│   ├── movements.service.ts
│   ├── savings.service.ts
│   ├── recurring.service.ts
│   └── notifications.service.ts
├── hooks/                        ← custom hooks
│   ├── useAuth.ts
│   ├── useAccounts.ts
│   └── useNotifications.ts
├── lib/
│   ├── auth.ts                   ← configuración NextAuth
│   └── axios.ts                  ← instancia de axios
├── types/                        ← interfaces y tipos compartidos
│   ├── account.types.ts
│   ├── movement.types.ts
│   ├── saving.types.ts
│   └── recurring.types.ts
├── utils/
│   └── formatters.ts
└── constants/
    ├── account-types.ts
    └── movement-types.ts
```
