```markdown
# Detailed Implementation Plan for Android Rooting Service Website

This plan outlines the step-by-step changes and the dependent files to build an SEO-optimized, modern website with landing, services, blog, and contact pages.

---

## 1. Global Layout and SEO Base
**File:** `src/app/layout.tsx`  
- Import the new Navbar and Footer components.
- Wrap the page content with a common layout that includes a header for SEO meta tags (using Next.js Metadata API or `<Head>` component).
- Ensure proper semantic HTML structure and add error boundaries if needed.
- Update global styling with `src/app/globals.css` for a modern light/dark theme using CSS variables and responsive design.

---

## 2. Navigation Bar Component
**File:** `src/components/Navbar.tsx`  
- Create a responsive navigation bar with links to Home (`/`), Services (`/services`), Blog (`/blog`), and Contact (`/contact`) using Next.js `Link` components.
- Style the navigation using typography, spacing, and background color (avoid any icon libraries).
- Include fallback text if a link fails to render.

---

## 3. Footer Component with Messaging Buttons
**File:** `src/components/Footer.tsx`  
- Build a footer displaying direct message buttons for Messenger, WhatsApp, and Telegram.  
- Use simple `<a>` tags styled as buttons.  
- Set the href attributes to placeholder URLs (e.g., `https://m.me/yourUsername`, `https://wa.me/yourNumber`, `https://t.me/yourUsername`) for direct messaging.
- Ensure clear, accessible text labels and proper focus/hover styles.

---

## 4. Landing Page (Hero Section)
**File:** `src/app/page.tsx`  
- Create a hero section with a strong headline (e.g., "Top-rated Android Rooting & Modification Services") and a call-to-action button ("Get Started").
- Integrate a hero image using an `<img>` tag with:
  - `src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/712925ba-2581-456e-8a3c-5083a181f151.png"`
  - A highly descriptive `alt` attribute (e.g., "Modern creative android rooting service landing page featuring sleek typography and minimal design").
  - An `onerror` handler to load a fallback image.
- Include SEO-friendly metadata (title, description, keywords such as "Android Rooting, Android Modification, US Android Rooting, EU Android Rooting").

---

## 5. Services Page
**File:** `src/app/services/page.tsx`  
- Create a section detailing the rooting services (e.g., "Safe Rooting," "Advanced Modding," "Customization").
- Use existing UI components (like the Card from `src/components/ui/card.tsx`) for each service.
- Embed brief descriptions and possibly an image per service using placeholder URLs:
  - Example: `<img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a28202af-1adf-485b-998b-21c70bead7ee.png" alt="Safe android rooting service feature" onError="this.onerror=null;this.src='fallback.jpg';" />`
- Add SEO meta tags specific for the services page.

---

## 6. Blog Page
**File:** `src/app/blog/page.tsx`  
- Develop a listing page for blog posts in a card layout.
- Each blog card should display a title, a short snippet, and a “Read More” link.
- Consider static sample data for now; later integration with a headless CMS or Markdown files can be added.
- Include appropriate SEO metadata (e.g., "Android Rooting Blog").

---

## 7. Contact Page with Form
**File:** `src/app/contact/page.tsx`  
- Design a contact form using semantic HTML elements with fields: Name, Email, Subject, and Message.
- Use an existing Button component (from `src/components/ui/button.tsx`) for form submission.
- Add client-side validation and display error/success messages.
- Integrate the direct messaging buttons (optional reiteration from Footer for quick access).
- Ensure proper accessibility and responsive design.

---

## 8. API Route for Contact Submissions
**File:** `src/app/api/contact/route.ts`  
- Create a POST API route to handle form submissions.
- Validate input fields (check for empty strings, valid email formats).
- Use try/catch blocks to handle errors and return JSON responses with appropriate HTTP status codes.
- For now, simulate email processing with a success response message such as "Thank you for contacting us."

---

## 9. Global Styling and Best Practices
**File:** `src/app/globals.css`  
- Update global CSS to include typography, spacing, and color themes that support both light and dark modes.
- Ensure accessibility standards, responsive breakpoints, and modern minimal design aesthetics.
- Review existing CSS to prevent conflicts with new components.

---

## 10. Testing, SEO & Error Handling
- Test navigation flows between pages using Next.js routing.
- Validate SEO meta tags in the browser’s developer tools.
- Use curl commands to test the contact API endpoint, ensuring that proper JSON responses are returned.
- Ensure graceful fallbacks for images and handle any runtime errors using try/catch in form submissions and API routes.

---

## Summary
- The layout is centralized in `src/app/layout.tsx` with integrated navigation and footer components.
- New components (`Navbar.tsx` and `Footer.tsx`) provide seamless navigation and direct messaging through external links.
- Dedicated pages (Landing, Services, Blog, Contact) include modern UI sections, semantic markup, and SEO metadata.
- A contact form is implemented with client-side validation and an API route (`src/app/api/contact/route.ts`) for handling submissions.
- Global styling is updated for a modern, responsive, and accessible design.
- Each image uses a placeholder URL with descriptive text and proper error handling.
- The plan includes detailed error handling and best practices, ensuring a robust and SEO-optimized website.
