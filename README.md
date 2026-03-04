# Client — Personal Finance Manager

Frontend construido con Next.js (App Router) para la gestión de finanzas personales. Consume la API REST de NestJS y ofrece dashboard, cuentas, movimientos, metas de ahorro y notificaciones.

## Requisitos

- [Bun](https://bun.sh)

## Inicialización

### 1. Variables de entorno

```bash
cp .env.example .env.local
```

| Variable       | Descripción             |
| -------------- | ----------------------- |
| `PORT`         | Puerto del servidor dev |
| `NEXTAUTH_URL` | URL base de la app      |
| `NEXTAUTH_SECRET` | Secret de NextAuth   |
| `API_URL`      | URL de la API NestJS    |

### 2. Dependencias

```bash
bun install
```

### 3. Correr en desarrollo

```bash
bun run dev
```

La app queda disponible en `http://localhost:3001`.

## Scripts

| Comando          | Descripción                    |
| ---------------- | ------------------------------ |
| `bun run dev`    | Modo desarrollo (puerto 3001)  |
| `bun run build`  | Build de producción            |
| `bun run start`  | Servidor de producción         |
| `bun run lint`   | Lint del código                |

## Estructura de carpetas

```
client/
├── app/                     # App Router de Next.js
│   ├── (auth)/              # Rutas de autenticación
│   ├── (dashboard)/         # Rutas protegidas
│   ├── layout.tsx           # Layout raíz
│   └── page.tsx             # Página de inicio
├── components/              # Componentes reutilizables
│   ├── ui/                  # Componentes base (shadcn-like)
│   └── shared/              # Componentes del dominio
├── lib/                     # Utilidades, helpers, validaciones Zod
├── hooks/                   # Custom hooks
├── services/                # Llamadas a la API
├── types/                   # Tipos TypeScript globales
└── public/                  # Assets estáticos
```