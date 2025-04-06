# pnpm installation

(https://pnpm.io/installation)
npm install -g pnpm@latest-10

# shadcn installation

(https://ui.shadcn.com/docs/installation/next)
pnpm create next-app@latest . --typescript --tailwind --eslint
pnpm dlx shadcn@latest init

# font configuration

```javascript
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
