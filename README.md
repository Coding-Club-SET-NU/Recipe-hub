# 🍽️ RecipeHub — Recipe Web Application

A modern, full-featured recipe discovery and meal planning web app built with React, TypeScript, and Firebase.


visit here--->>> https://recipe-hub.anupchowdhury219.workers.dev/
---

## 🚀 Getting Started

```bash
npm i          # Install dependencies
npm run dev    # Start dev server at http://localhost:5173
```

---

## ✨ Features

### 🔐 Authentication (Firebase)
- Email & password **Sign Up** and **Sign In**
- **Forgot Password** — sends a reset link to your inbox via Firebase
- Session persists across page refreshes
- Protected routes: Create Recipe, Meal Planner, Shopping List, My Recipes redirect to login when not signed in

### 🏠 Home Page
- **Three.js 3D hero** — floating, spinning food shapes (donuts, torus-knots, spheres, gems) with particle field and mouse parallax
- **Recipe of the Day** — a cinematic full-width banner featuring the top-rated recipe of the day; clicking opens a specialty modal with highlights, chef insights, step preview, and a link to the full recipe
- **Category pills** — quick filters for cuisine and diet type
- **Recipe grid** with staggered entrance animations
- **Tabs** — All Recipes, Trending, Quick (≤30 min), Top Rated

### 📖 Recipe Detail Page
- **Image gallery** — 3 thumbnails showing the same dish from different angles (crop variants of the original photo), click to switch, click main image to open a full-screen lightbox
- **Expandable instructions** — steps are compact by default; click any step to reveal a contextual chef tip
- **Serving size adjuster** — scales all ingredient quantities dynamically
- **Sticky sidebar** — ingredients list and per-serving nutrition facts
- **Macronutrient chart** and full ingredient breakdown table
- **Star rating widget** — 5-star interactive rating with optional review text

### 🗓️ Meal Planner
- Plan meals across the week by day and meal type
- Add recipes directly from the recipe detail page

### 🛒 Shopping List
- Auto-populated from recipe ingredients
- Check off items as you shop

### 👨‍🍳 My Recipes
- View and manage all user-created recipes

### ➕ Create Recipe
- Full recipe builder with ingredient and step management

---

## 🎨 Design System

- **Framework**: React 19 + TypeScript + Vite
- **Styling**: Tailwind CSS v4 with custom CSS variables (saffron brand palette)
- **Font**: Outfit (Google Fonts)
- **Animations**: Framer Motion (`motion/react`) — page transitions, staggered grids, spring animations, AnimatePresence
- **3D**: Three.js hero canvas with lighting, emissive glow, and mouse parallax
- **UI Components**: Radix UI primitives
- **Notifications**: Sonner toasts
- **Dark Mode**: `next-themes`

---

## 🔥 Firebase Setup

1. Go to [console.firebase.google.com](https://console.firebase.google.com)
2. Create a project and add a Web app
3. Enable **Email/Password** under Authentication → Sign-in method
4. Copy your config into `src/lib/firebase.ts`

---

## 📁 Project Structure

```
src/
├── app/
│   ├── components/       # Reusable UI components
│   │   ├── Header.tsx
│   │   ├── Footer.tsx
│   │   ├── HeroCanvas.tsx    # Three.js 3D scene
│   │   ├── RecipeCard.tsx
│   │   ├── RecipeFilters.tsx
│   │   └── ProtectedRoute.tsx
│   ├── context/
│   │   └── AuthContext.tsx   # Firebase Auth (login, register, reset)
│   ├── pages/
│   │   ├── Home.tsx          # Hero, Recipe of the Day, recipe grid
│   │   ├── RecipeDetail.tsx  # Gallery, instructions, rating
│   │   ├── Login.tsx         # Sign In / Register / Forgot Password
│   │   ├── CreateRecipe.tsx
│   │   ├── MealPlanner.tsx
│   │   ├── ShoppingList.tsx
│   │   └── MyRecipes.tsx
│   ├── data/
│   │   └── mockRecipes.ts    # 12 curated recipes with full nutrition data
│   ├── types/
│   │   └── recipe.ts
│   └── utils/
│       ├── localStorage.ts   # Favorites, shopping list, meal plans
│       └── recipeUtils.ts
└── lib/
    └── firebase.ts           # Firebase app initialisation
```
