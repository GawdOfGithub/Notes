#### Recommendation --> Always take fonts from google fonts 
[For further reference](https://nextjs.org/learn/dashboard-app/optimizing-fonts-images)

### Basically the purpose the of next fonts is so that next can save the fonts that you use during build time so that it does not have to fetch font again and again slowing the website so we here we go next fonts hip hip hurrey without wasting time here is how you add them 
```jsx
import { Inter } from 'next/font/google';
 
export const inter = Inter({ subsets: ['latin'] });

```

```jsx
Finally, add the font to the <body> element in /app/layout.tsx:
/app/layout.tsx

import '@/app/ui/global.css';
import { inter } from '@/app/ui/fonts';
 
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body className={`${inter.className} antialiased`}>{children}</body>
    </html>
  );
}
```
