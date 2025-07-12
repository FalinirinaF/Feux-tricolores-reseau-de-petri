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
