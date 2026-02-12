# Vercel Web Analytics Integration

This project has been configured with Vercel Web Analytics to track visitors and page views.

## Setup

The analytics integration has been implemented following the official Vercel documentation:

1. **Package Installed**: `@vercel/analytics` (v1.4.0+)
2. **Integration Point**: `app/layout.tsx` - The `Analytics` component is added to the root layout
3. **Framework**: Next.js App Router

## Implementation Details

The `<Analytics />` component from `@vercel/analytics/next` is placed at the bottom of the body tag in the root layout (`app/layout.tsx`). This ensures tracking is enabled across all pages of the application.

```tsx
import { Analytics } from '@vercel/analytics/next'

export default function RootLayout({ children }) {
  return (
    <html lang="id">
      <body>
        {children}
        <Analytics />
      </body>
    </html>
  )
}
```

## How to Enable

1. Deploy this application to Vercel
2. Go to your Vercel dashboard
3. Select this project
4. Click the **Analytics** tab
5. Click **Enable**

After enabling and deploying, the application will start tracking:
- Page views
- Visitor data
- Performance metrics

## Verification

After deployment, you can verify the analytics are working by:
1. Visiting your deployed site
2. Opening the browser's Developer Tools (Network tab)
3. Looking for a request to `/_vercel/insights/view`

## Documentation

For more information about Vercel Web Analytics:
- [Official Documentation](https://vercel.com/docs/analytics)
- [Analytics Package Documentation](https://vercel.com/docs/analytics/package)
- [Custom Events](https://vercel.com/docs/analytics/custom-events)
- [Privacy Policy](https://vercel.com/docs/analytics/privacy-policy)
