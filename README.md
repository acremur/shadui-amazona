# Next.js ECommerce App With Admin Panel For Beginners

### [Nextjs, Tailwind, ShadUI, Stripe, PayPal]

A [video](https://www.youtube.com/watch?v=M4DrCi8EuYE&ab_channel=AIWithBasir) from the youtube channel **AI With Basir**.

<br>

## Initial setup

[pnpm installation](https://pnpm.io/installation)

`npm install -g pnpm@latest-10`

[ShadUI installation](https://ui.shadcn.com/docs/installation/next)

`pnpm create next-app@latest . --typescript --tailwind --eslint`

`pnpm dlx shadcn@latest init`

<br>

[Color style personalization](https://ui.shadcn.com/themes)

> Change global.css

```css
:root {
  --radius: 0.5rem;
  --background: oklch(1 0 0);
  --foreground: oklch(0.141 0.005 285.823);
  --card: oklch(1 0 0);
  --card-foreground: oklch(0.141 0.005 285.823);
  /* ... */
}

.dark {
  --background: oklch(0.141 0.005 285.823);
  --foreground: oklch(0.985 0 0);
  --card: oklch(0.21 0.006 285.885);
  --card-foreground: oklch(0.985 0 0);
  --popover: oklch(0.21 0.006 285.885);
  /* ... */
}
```

<br>

## Tailwind merge and font configuration

> Change layout.tsx

```javascript
  import { cn } from '@/lib/utils'
  import { Poppins as FontSans } from 'next/font/google'

  const fontSans = FontSans({
      subsets: ['latin'],
      weight: ['400', '600'],
      variable: '--font-sans',
  })

  <body
      className={cn(
          'min-h-screen, bg-background font-sans antialiased',
          fontSans.variable
      )}
      >
      {children}
  </body>
```
