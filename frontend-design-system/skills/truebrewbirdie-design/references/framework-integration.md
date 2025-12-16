# Framework Integration

Tailwind CSS, shadcn/ui, and Framer Motion configurations.

---

## Tailwind CSS

### Custom Configuration

```javascript
// tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  darkMode: 'class',
  content: [
    './pages/**/*.{js,ts,jsx,tsx,mdx}',
    './components/**/*.{js,ts,jsx,tsx,mdx}',
    './app/**/*.{js,ts,jsx,tsx,mdx}',
  ],
  theme: {
    extend: {
      // ================================
      // FONTS
      // ================================
      fontFamily: {
        display: ['var(--font-display)', 'sans-serif'],
        body: ['var(--font-body)', 'sans-serif'],
        mono: ['var(--font-mono)', 'monospace'],
      },

      // ================================
      // COLORS (Semantic)
      // ================================
      colors: {
        background: 'hsl(var(--background))',
        foreground: 'hsl(var(--foreground))',
        surface: {
          DEFAULT: 'hsl(var(--surface))',
          secondary: 'hsl(var(--surface-secondary))',
        },
        accent: {
          DEFAULT: 'hsl(var(--accent))',
          foreground: 'hsl(var(--accent-foreground))',
          muted: 'hsl(var(--accent-muted))',
        },
        muted: {
          DEFAULT: 'hsl(var(--muted))',
          foreground: 'hsl(var(--muted-foreground))',
        },
        border: 'hsl(var(--border))',
        ring: 'hsl(var(--ring))',
      },

      // ================================
      // BORDER RADIUS
      // ================================
      borderRadius: {
        lg: 'var(--radius-lg)',
        md: 'var(--radius-md)',
        sm: 'var(--radius-sm)',
      },

      // ================================
      // SPACING (Extended)
      // ================================
      spacing: {
        '18': '4.5rem',
        '22': '5.5rem',
        '30': '7.5rem',
      },

      // ================================
      // ANIMATIONS
      // ================================
      keyframes: {
        'fade-up': {
          '0%': { opacity: '0', transform: 'translateY(20px)' },
          '100%': { opacity: '1', transform: 'translateY(0)' },
        },
        'fade-in': {
          '0%': { opacity: '0' },
          '100%': { opacity: '1' },
        },
        'scale-in': {
          '0%': { opacity: '0', transform: 'scale(0.95)' },
          '100%': { opacity: '1', transform: 'scale(1)' },
        },
        'slide-in-right': {
          '0%': { transform: 'translateX(100%)' },
          '100%': { transform: 'translateX(0)' },
        },
      },
      animation: {
        'fade-up': 'fade-up 0.6s cubic-bezier(0.16, 1, 0.3, 1) forwards',
        'fade-in': 'fade-in 0.4s ease-out forwards',
        'scale-in': 'scale-in 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards',
        'slide-in-right': 'slide-in-right 0.3s ease-out forwards',
      },

      // ================================
      // TRANSITIONS
      // ================================
      transitionTimingFunction: {
        'out-expo': 'cubic-bezier(0.16, 1, 0.3, 1)',
        'out-quart': 'cubic-bezier(0.25, 1, 0.5, 1)',
        'out-back': 'cubic-bezier(0.34, 1.56, 0.64, 1)',
      },

      // ================================
      // TYPOGRAPHY PLUGIN
      // ================================
      typography: {
        DEFAULT: {
          css: {
            maxWidth: '65ch',
            color: 'hsl(var(--foreground))',
            a: {
              color: 'hsl(var(--accent))',
              textDecoration: 'underline',
              '&:hover': {
                color: 'hsl(var(--accent))',
              },
            },
            h1: {
              fontFamily: 'var(--font-display)',
              fontWeight: '700',
            },
            h2: {
              fontFamily: 'var(--font-display)',
              fontWeight: '600',
            },
            h3: {
              fontFamily: 'var(--font-display)',
              fontWeight: '600',
            },
            code: {
              fontFamily: 'var(--font-mono)',
              backgroundColor: 'hsl(var(--muted))',
              padding: '0.25rem 0.375rem',
              borderRadius: '0.25rem',
            },
          },
        },
      },
    },
  },
  plugins: [
    require('@tailwindcss/typography'),
    require('@tailwindcss/forms'),
    require('tailwindcss-animate'),
  ],
}
```

### CSS Variables Setup

```css
/* globals.css */
@tailwind base;
@tailwind components;
@tailwind utilities;

@layer base {
  :root {
    /* Background & Foreground */
    --background: 0 0% 100%;
    --foreground: 0 0% 9%;

    /* Surfaces */
    --surface: 0 0% 100%;
    --surface-secondary: 0 0% 98%;

    /* Accent */
    --accent: 220 90% 56%;
    --accent-foreground: 0 0% 100%;
    --accent-muted: 220 90% 96%;

    /* Muted */
    --muted: 0 0% 96%;
    --muted-foreground: 0 0% 45%;

    /* Border & Ring */
    --border: 0 0% 90%;
    --ring: 220 90% 56%;

    /* Radius */
    --radius-sm: 0.25rem;
    --radius-md: 0.5rem;
    --radius-lg: 1rem;
  }

  .dark {
    --background: 0 0% 4%;
    --foreground: 0 0% 98%;

    --surface: 0 0% 7%;
    --surface-secondary: 0 0% 10%;

    --accent: 220 90% 60%;
    --accent-foreground: 0 0% 100%;
    --accent-muted: 220 30% 15%;

    --muted: 0 0% 15%;
    --muted-foreground: 0 0% 65%;

    --border: 0 0% 18%;
    --ring: 220 90% 60%;
  }
}

@layer base {
  * {
    @apply border-border;
  }

  body {
    @apply bg-background text-foreground;
    font-family: var(--font-body);
  }
}
```

### Utility Classes

```css
@layer utilities {
  /* Stagger animation delays */
  .stagger-1 { animation-delay: 0ms; }
  .stagger-2 { animation-delay: 75ms; }
  .stagger-3 { animation-delay: 150ms; }
  .stagger-4 { animation-delay: 225ms; }
  .stagger-5 { animation-delay: 300ms; }

  /* Text balance */
  .text-balance {
    text-wrap: balance;
  }

  /* Hide scrollbar */
  .no-scrollbar::-webkit-scrollbar {
    display: none;
  }
  .no-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
}
```

---

## shadcn/ui

### Theme Configuration

```css
/* In globals.css after Tailwind imports */
@layer base {
  :root {
    --background: 0 0% 100%;
    --foreground: 222.2 84% 4.9%;

    --card: 0 0% 100%;
    --card-foreground: 222.2 84% 4.9%;

    --popover: 0 0% 100%;
    --popover-foreground: 222.2 84% 4.9%;

    --primary: 222.2 47.4% 11.2%;
    --primary-foreground: 210 40% 98%;

    --secondary: 210 40% 96.1%;
    --secondary-foreground: 222.2 47.4% 11.2%;

    --muted: 210 40% 96.1%;
    --muted-foreground: 215.4 16.3% 46.9%;

    --accent: 210 40% 96.1%;
    --accent-foreground: 222.2 47.4% 11.2%;

    --destructive: 0 84.2% 60.2%;
    --destructive-foreground: 210 40% 98%;

    --border: 214.3 31.8% 91.4%;
    --input: 214.3 31.8% 91.4%;
    --ring: 222.2 84% 4.9%;

    --radius: 0.5rem;
  }

  .dark {
    --background: 222.2 84% 4.9%;
    --foreground: 210 40% 98%;

    --card: 222.2 84% 4.9%;
    --card-foreground: 210 40% 98%;

    --popover: 222.2 84% 4.9%;
    --popover-foreground: 210 40% 98%;

    --primary: 210 40% 98%;
    --primary-foreground: 222.2 47.4% 11.2%;

    --secondary: 217.2 32.6% 17.5%;
    --secondary-foreground: 210 40% 98%;

    --muted: 217.2 32.6% 17.5%;
    --muted-foreground: 215 20.2% 65.1%;

    --accent: 217.2 32.6% 17.5%;
    --accent-foreground: 210 40% 98%;

    --destructive: 0 62.8% 30.6%;
    --destructive-foreground: 210 40% 98%;

    --border: 217.2 32.6% 17.5%;
    --input: 217.2 32.6% 17.5%;
    --ring: 212.7 26.8% 83.9%;
  }
}
```

### Custom Component Variants

```tsx
// components/ui/button.tsx
import { cva, type VariantProps } from "class-variance-authority"

const buttonVariants = cva(
  "inline-flex items-center justify-center rounded-md text-sm font-medium ring-offset-background transition-all focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-ring focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50",
  {
    variants: {
      variant: {
        default:
          "bg-primary text-primary-foreground hover:bg-primary/90 shadow-sm hover:shadow-md hover:-translate-y-0.5 active:translate-y-0",
        destructive:
          "bg-destructive text-destructive-foreground hover:bg-destructive/90",
        outline:
          "border border-input bg-background hover:bg-accent hover:text-accent-foreground",
        secondary:
          "bg-secondary text-secondary-foreground hover:bg-secondary/80",
        ghost:
          "hover:bg-accent hover:text-accent-foreground",
        link:
          "text-primary underline-offset-4 hover:underline",
        // Custom variants
        gradient:
          "bg-gradient-to-r from-primary to-accent text-white hover:opacity-90",
        glow:
          "bg-primary text-primary-foreground shadow-[0_0_20px_rgba(var(--primary),0.3)] hover:shadow-[0_0_30px_rgba(var(--primary),0.5)]",
      },
      size: {
        default: "h-10 px-4 py-2",
        sm: "h-9 rounded-md px-3",
        lg: "h-11 rounded-md px-8",
        xl: "h-14 rounded-lg px-10 text-base",
        icon: "h-10 w-10",
      },
    },
    defaultVariants: {
      variant: "default",
      size: "default",
    },
  }
)
```

### Card with Motion

```tsx
// components/ui/motion-card.tsx
"use client"

import { motion } from "framer-motion"
import { cn } from "@/lib/utils"

interface MotionCardProps extends React.HTMLAttributes<HTMLDivElement> {
  children: React.ReactNode
}

export function MotionCard({ className, children, ...props }: MotionCardProps) {
  return (
    <motion.div
      className={cn(
        "rounded-lg border bg-card text-card-foreground shadow-sm",
        className
      )}
      initial={{ opacity: 0, y: 20 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.4, ease: [0.16, 1, 0.3, 1] }}
      whileHover={{
        y: -4,
        boxShadow: "0 20px 40px rgba(0,0,0,0.1)",
        transition: { duration: 0.2 }
      }}
      {...props}
    >
      {children}
    </motion.div>
  )
}
```

---

## Framer Motion

### Motion Components Library

```tsx
// components/motion/index.tsx
"use client"

import { motion, Variants } from "framer-motion"
import { ReactNode } from "react"

// ================================
// FADE UP
// ================================
interface FadeUpProps {
  children: ReactNode
  delay?: number
  duration?: number
  className?: string
}

export function FadeUp({
  children,
  delay = 0,
  duration = 0.6,
  className
}: FadeUpProps) {
  return (
    <motion.div
      className={className}
      initial={{ opacity: 0, y: 20 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{
        duration,
        delay,
        ease: [0.16, 1, 0.3, 1]
      }}
    >
      {children}
    </motion.div>
  )
}

// ================================
// FADE IN
// ================================
export function FadeIn({
  children,
  delay = 0,
  duration = 0.4,
  className
}: FadeUpProps) {
  return (
    <motion.div
      className={className}
      initial={{ opacity: 0 }}
      animate={{ opacity: 1 }}
      transition={{ duration, delay }}
    >
      {children}
    </motion.div>
  )
}

// ================================
// SCALE IN
// ================================
export function ScaleIn({
  children,
  delay = 0,
  duration = 0.4,
  className
}: FadeUpProps) {
  return (
    <motion.div
      className={className}
      initial={{ opacity: 0, scale: 0.95 }}
      animate={{ opacity: 1, scale: 1 }}
      transition={{
        duration,
        delay,
        ease: [0.16, 1, 0.3, 1]
      }}
    >
      {children}
    </motion.div>
  )
}

// ================================
// STAGGER CONTAINER
// ================================
const staggerContainerVariants: Variants = {
  hidden: { opacity: 0 },
  visible: {
    opacity: 1,
    transition: {
      staggerChildren: 0.08,
      delayChildren: 0.1
    }
  }
}

const staggerItemVariants: Variants = {
  hidden: { opacity: 0, y: 20 },
  visible: {
    opacity: 1,
    y: 0,
    transition: {
      duration: 0.5,
      ease: [0.16, 1, 0.3, 1]
    }
  }
}

interface StaggerContainerProps {
  children: ReactNode
  className?: string
}

export function StaggerContainer({ children, className }: StaggerContainerProps) {
  return (
    <motion.div
      className={className}
      variants={staggerContainerVariants}
      initial="hidden"
      animate="visible"
    >
      {children}
    </motion.div>
  )
}

export function StaggerItem({ children, className }: StaggerContainerProps) {
  return (
    <motion.div className={className} variants={staggerItemVariants}>
      {children}
    </motion.div>
  )
}

// ================================
// SCROLL REVEAL
// ================================
interface ScrollRevealProps {
  children: ReactNode
  className?: string
  once?: boolean
}

export function ScrollReveal({
  children,
  className,
  once = true
}: ScrollRevealProps) {
  return (
    <motion.div
      className={className}
      initial={{ opacity: 0, y: 50 }}
      whileInView={{ opacity: 1, y: 0 }}
      viewport={{ once, margin: "-100px" }}
      transition={{
        duration: 0.6,
        ease: [0.16, 1, 0.3, 1]
      }}
    >
      {children}
    </motion.div>
  )
}

// ================================
// PAGE TRANSITION
// ================================
export const pageVariants: Variants = {
  initial: { opacity: 0, y: 20 },
  animate: {
    opacity: 1,
    y: 0,
    transition: {
      duration: 0.6,
      ease: [0.16, 1, 0.3, 1]
    }
  },
  exit: {
    opacity: 0,
    y: -20,
    transition: { duration: 0.4 }
  }
}

interface PageTransitionProps {
  children: ReactNode
  className?: string
}

export function PageTransition({ children, className }: PageTransitionProps) {
  return (
    <motion.div
      className={className}
      variants={pageVariants}
      initial="initial"
      animate="animate"
      exit="exit"
    >
      {children}
    </motion.div>
  )
}
```

### Usage Examples

```tsx
// Page with staggered content
import { StaggerContainer, StaggerItem, ScrollReveal } from "@/components/motion"

export default function Page() {
  return (
    <main>
      <StaggerContainer className="grid grid-cols-3 gap-6">
        {items.map((item) => (
          <StaggerItem key={item.id}>
            <Card>{item.content}</Card>
          </StaggerItem>
        ))}
      </StaggerContainer>

      <ScrollReveal>
        <section className="py-20">
          <h2>This fades in on scroll</h2>
        </section>
      </ScrollReveal>
    </main>
  )
}
```

---

## Font Setup

### Next.js Font Configuration

```tsx
// app/layout.tsx
import { Clash_Display } from "next/font/local"
import { Outfit } from "next/font/google"
import { JetBrains_Mono } from "next/font/google"

const clashDisplay = localFont({
  src: "../fonts/ClashDisplay-Variable.woff2",
  variable: "--font-display",
})

const outfit = Outfit({
  subsets: ["latin"],
  variable: "--font-body",
})

const jetbrainsMono = JetBrains_Mono({
  subsets: ["latin"],
  variable: "--font-mono",
})

export default function RootLayout({ children }) {
  return (
    <html
      lang="en"
      className={`${clashDisplay.variable} ${outfit.variable} ${jetbrainsMono.variable}`}
    >
      <body>{children}</body>
    </html>
  )
}
```

### CSS Font Variables

```css
/* globals.css */
:root {
  --font-display: 'Clash Display', sans-serif;
  --font-body: 'Outfit', sans-serif;
  --font-mono: 'JetBrains Mono', monospace;
}

body {
  font-family: var(--font-body);
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-display);
}

code, pre {
  font-family: var(--font-mono);
}
```

---

## Quick Start Template

### Complete Setup

```bash
# Create Next.js app
npx create-next-app@latest my-app --typescript --tailwind --eslint --app

# Install dependencies
npm install framer-motion class-variance-authority clsx tailwind-merge

# Install shadcn/ui
npx shadcn@latest init

# Add components
npx shadcn@latest add button card input
```

### File Structure

```
my-app/
├── app/
│   ├── globals.css          # Tailwind + CSS variables
│   ├── layout.tsx           # Font setup
│   └── page.tsx
├── components/
│   ├── motion/              # Motion components
│   │   └── index.tsx
│   └── ui/                  # shadcn components
│       ├── button.tsx
│       └── card.tsx
├── lib/
│   └── utils.ts             # cn() helper
└── tailwind.config.js       # Custom config
```

### Utils Helper

```tsx
// lib/utils.ts
import { type ClassValue, clsx } from "clsx"
import { twMerge } from "tailwind-merge"

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs))
}
```
