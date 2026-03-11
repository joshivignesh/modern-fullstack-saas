# Modern FullStack SaaS - Frontend

React 18 + TypeScript Frontend with modern tooling

## Tech Stack
- **Framework**: React 18
- **Language**: TypeScript
- **Bundler**: Vite
- **Routing**: React Router v6
- **State Management**: Zustand
- **Data Fetching**: TanStack Query (React Query)
- **Styling**: Tailwind CSS
- **Form Handling**: React Hook Form + Zod
- **HTTP Client**: Axios
- **UI Components**: Headless UI
- **Icons**: Lucide React
- **Testing**: Vitest + jsdom
- **Linting**: ESLint

## Project Structure
\`\`\`
frontend/
├── src/
│   ├── components/          # Reusable UI components
│   ├── pages/              # Page components
│   ├── hooks/              # Custom React hooks
│   ├── store/              # Zustand stores
│   ├── services/           # API services
│   ├── types/              # TypeScript types
│   ├── utils/              # Utility functions
│   ├── styles/             # Global styles
│   └── App.tsx
├── public/                 # Static assets
├── index.html
├── vite.config.ts
├── tsconfig.json
└── tailwind.config.js
\`\`\`

## Getting Started

### Prerequisites
- Node.js 18+
- npm or pnpm

### Installation
\`\`\`bash
cd frontend
npm install
\`\`\`

### Development
\`\`\`bash
npm run dev
\`\`\`

Dev server runs on `http://localhost:5173`

### Build
\`\`\`bash
npm run build
npm run preview
\`\`\`

## Testing
\`\`\`bash
npm run test
npm run test:ui
\`\`\`

## Environment Variables
\`\`\`
VITE_API_URL=http://localhost:5001
VITE_API_TIMEOUT=30000
\`\`\`

## Key Features
- ✅ Modern React patterns (Hooks, Suspense, Transitions)
- ✅ Strong TypeScript typing
- ✅ Responsive design with Tailwind
- ✅ API integration with TanStack Query
- ✅ Client-side state management
- ✅ Form validation with Zod
- ✅ Dark mode support
- ✅ Optimized images & code splitting
- ✅ SEO-friendly
- ✅ Comprehensive testing setup
