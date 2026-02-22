# NextJS Notes
---
# 1. Why do we need nextjs?

## The Problem with plain React (CSR only)
React (Vite/CRA) applications use **Client-Side Rendering (CSR)** only by default.

### What happens in CSR:
1. Browser requests a page,
2. Server sends minimal HTML,
3. Browser downloads JavaScript bundle,
4. React renders the UI in the broswer

### Probems with Pure CSR
- Slow initial load (Large JS bundle)
- Poor SEO (empty initial HTML)
- Blank screen until JS loads
- No built-in routing
- No bult-in backend/API layer
- Performance optimizations are manual

## Special Features NextJS Provides which React does not

## 1. Multiple Rendering Strategies
- Server Side Rendering (SSR)
- Static Site Generation (SSG)
- React Server Components
- Hybrid rendering per page

## 2. File based Routing
- Automatic routing using folder structure
- No need to install `react-router-dom`
- Supports dynamic routes and mested layouts

## 3. Built-in Backend Support
- API routes inside the same project
- Server-side logic handling
- Databse integration capability
- Authentication handling

## 4. Automatic Code Splitting
- Splits JavaScript per route automatically
- Reduces bundle size
- Improves performance

## 5. Image Optimization
- Automatic resizing
- Lazy loading
- Modern formats
- Reduced layout shift

## 6. Font Optimization
- Self-hosted fonts
- Optmized laoding
- No external blocking

## 7. Script Optimization
- Control over script loading strategy
- Prevents render-blocking scripts

## 8. SEO Management
- Built-in metadata handling
- Dynamic meta tags
- Better search engine indexing

## 9. React Server Components
- Server-only components
- Reduced clint-side JavaScript
- Improved performance

## 10. Development Enhancements
- Fast Refresh
- Hot Module Replacement (HMR)
- Built-in analytics support
- React Compiler compatibility

---

# 2. What is NextJS?
NextJS is a **React Framework** that adds:

- Server-Side Rendering (SSR)
- Static Site Generation (SSG)
- File-based routing
- API routes
- Image optimization
- App Router architecture
- Server Components

> React = UI Library
> NextJS = Production ready React framework

---

# 3. React vs NextJS

| Feature | React (Vite) | Next.js |
|----------|--------------|----------|
| Rendering | CSR only | CSR + SSR + SSG |
| Routing | React Router | File-based routing |
| SEO | Weak | Strong |
| Backend | Separate server | Built-in API routes |
| Optimization | Manual | Automatic |
| Project Structure | Flexible | Opinionated |

---

# 4 Client-Side Rendering (CSR)

## What is CSR?
- The browser renders the page after downloading and executing JavaScript.
- The server sends minimal HTML.

## How CSR Works

1. User requests a page,
2. Server returns basic HTML,
3. Browser downloads JS bundle,
4. React executes JavaScript,
5. UI is rendered in the broswer

## Example: CSR in react
```jsx
// App.jsx
export default function App()
{
  return <h1>Hello world</h1>;
}

// index.html
<body>
  <div id="root"></div>
  <script src="/bundle.jsx"></script>
</body>
```
Content appears only after Javascript runs.
