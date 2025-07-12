# Intelligent Traffic System

This is a Next.js project that implements an intelligent traffic light management system based on a combination of Petri nets and machine learning.

## Features

- **Petri Net Model**: Models the logical behavior of traffic lights at a four-way intersection (North, South, East, West), including state transitions and firing conditions.
- **Machine Learning (Reinforcement Learning)**: Analyzes traffic data (simulated from sensors) to dynamically optimize the duration of each traffic light phase.
- **Q-Learning Agent**: Learns to reduce the average waiting time of vehicles.
- **Simulable System**: Capable of adapting to variable traffic conditions.
- **Interactive Visualization**: Real-time display of traffic light states, vehicle queues, and performance metrics.

## Getting Started

Follow these steps to set up and run the project locally.
Pour installer ce projet localement dans votre IDE, voici les étapes complètes :

## **Installation Locale**

### **1. Prérequis**

```shellscript
# Vérifier que Node.js est installé (version 18+)
node --version
npm --version

# Si pas installé, télécharger depuis https://nodejs.org/
```

### **2. Créer le projet Next.js**

```shellscript
# Créer un nouveau projet Next.js avec TypeScript
npx create-next-app@latest traffic-light-system --typescript --tailwind --eslint --app --src-dir --import-alias "@/*"

# Aller dans le dossier
cd traffic-light-system
```

### **3. Installer les dépendances**

```shellscript
# Installer shadcn/ui
npx shadcn@latest init

# Installer les composants UI nécessaires
npx shadcn@latest add card button slider badge

# Installer Lucide React pour les icônes
npm install lucide-react

# Installer les types TypeScript (si nécessaire)
npm install --save-dev @types/node @types/react @types/react-dom
```

### **4. Fichiers à créer/modifier**

**`src/app/page.tsx`** :

```typescriptreact
import TrafficLightSystem from '../components/traffic-light-system'

export default function Home() {
  return (
    <main>
      <TrafficLightSystem />
    </main>
  )
}
```

**`src/components/traffic-light-system.tsx`** :
Copiez tout le code du composant principal que j'ai fourni.

### **5. Configuration shadcn/ui**

Si `components.json` n'existe pas, créez-le :

```json
{
  "$schema": "https://ui.shadcn.com/schema.json",
  "style": "default",
  "rsc": true,
  "tsx": true,
  "tailwind": {
    "config": "tailwind.config.js",
    "css": "src/app/globals.css",
    "baseColor": "slate",
    "cssVariables": true
  },
  "aliases": {
    "components": "@/components",
    "utils": "@/lib/utils"
  }
}
```

### **6. Lancer le projet**

```shellscript
# Installer toutes les dépendances
npm install

# Lancer en mode développement
npm run dev
```

### **7. Ouvrir dans le navigateur**

```plaintext
http://localhost:3000
```

## **Package.json complet**

Votre `package.json` devrait ressembler à ça :

```json
{
  "name": "traffic-light-system",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint"
  },
  "dependencies": {
    "react": "^18",
    "react-dom": "^18",
    "next": "14.0.0",
    "lucide-react": "^0.294.0",
    "class-variance-authority": "^0.7.0",
    "clsx": "^2.0.0",
    "tailwind-merge": "^2.0.0"
  },
  "devDependencies": {
    "typescript": "^5",
    "@types/node": "^20",
    "@types/react": "^18",
    "@types/react-dom": "^18",
    "autoprefixer": "^10.0.1",
    "postcss": "^8",
    "tailwindcss": "^3.3.0",
    "eslint": "^8",
    "eslint-config-next": "14.0.0"
  }
}
```

## ️ **IDEs Recommandés**

### **Visual Studio Code**

```shellscript
# Extensions recommandées :
# - ES7+ React/Redux/React-Native snippets
# - Tailwind CSS IntelliSense
# - TypeScript Importer
# - Prettier - Code formatter
```

### **WebStorm/IntelliJ**

- Support TypeScript natif
- Plugin Tailwind CSS
- Plugin Next.js


## **Dépannage**

Si vous avez des erreurs :

```shellscript
# Nettoyer le cache
rm -rf .next node_modules package-lock.json
npm install

# Réinstaller shadcn/ui
npx shadcn@latest init --force
```

### Prerequisites

Make sure you have Node.js (version 18 or higher) and npm installed.

\`\`\`bash
node --version
npm --version
\`\`\`

If not, you can download Node.js from [nodejs.org](https://nodejs.org/).

### Installation

1.  **Clone the repository:**

    \`\`\`bash
    git clone https://github.com/your-username/Feux-tricolore-r-seau-de-p-tri-.git
    cd Feux-tricolore-r-seau-de-p-tri-
    \`\`\`

2.  **Install dependencies:**

    \`\`\`bash
    npm install
    \`\`\`

3.  **Initialize shadcn/ui components:**

    This project uses `shadcn/ui` for its UI components. You need to initialize it and add the required components.

    \`\`\`bash
    npx shadcn@latest init
    npx shadcn@latest add card button slider badge
    \`\`\`

    Follow the prompts during initialization. Ensure the `components.json` file is correctly configured (it should be automatically set up by `npx shadcn@latest init`).

4.  **Run the development server:**

    \`\`\`bash
    npm run dev
    \`\`\`

    Open [http://localhost:3000](http://localhost:3000) in your browser to see the result.

## Project Structure

The core logic of the traffic light system is located in `src/components/traffic-light-system.tsx`.

\`\`\`
.
├── public/
├── src/
│   ├── app/
│   │   ├── globals.css
│   │   ├── layout.tsx
│   │   └── page.tsx
│   ├── components/
│   │   ├── ui/
│   │   │   └── ... (shadcn/ui components)
│   │   └── traffic-light-system.tsx  <-- Main component
│   └── lib/
│       └── utils.ts
├── components.json
├── next.config.mjs
├── package.json
├── postcss.config.mjs
├── tailwind.config.ts
└── tsconfig.json
\`\`\`

## Learn More

To learn more about Next.js, take a look at the following resources:

-   [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
-   [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
