# Anantya Digital

Static React portfolio with Home, Services, About Us, and Contact pages. Built with React and Vite. No backend required.

## Run locally

```sh
npm install
npm run dev
```

On Windows PowerShell, use `npm.cmd` if script execution is disabled. Open the local URL printed by Vite.

## Production

```sh
npm run build
npm run preview
```

Deploy the `dist` directory to any static host. Hash-based routes work without server rewrite rules. To serve from XAMPP at `/rushi_portfolio/`, copy the contents of `dist` to the serving directory (or visit `/rushi_portfolio/dist/`).

The contact form validates required fields and posts visitor details to FormSubmit for delivery to rushikatekar2003@gmail.com. After the first submission, the recipient must activate the form using the confirmation email from FormSubmit (check spam too). Until activation is complete, delivery is not verified. FormSubmit handles the spam check and confirmation page. No custom backend or SMTP password is required. Test from an HTTP/HTTPS served site rather than opening index.html directly. Google Fonts and the About page's Unsplash office photograph require internet access; system fonts provide a fallback.

After successful FormSubmit processing, _next returns visitors to public/thank-you.html (copied to dist on build). This is a public confirmation page, not proof of inbox delivery. Activation and spam checks remain with FormSubmit. email-templates/new-enquiry.html is a prepared custom email layout for a future server-side mail integration; it is not used by FormSubmit, which currently sends its built-in table template. Never put SMTP credentials in React.

Current form flow: AJAX POST to FormSubmit with CAPTCHA disabled. Visitors remain on the Contact page. A modal appears only after a successful API response; errors preserve input. Recipient activation is still required. API acceptance does not verify inbox delivery. The thank-you HTML file is retained but no longer used by the form.
