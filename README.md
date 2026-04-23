# ORU MVP

Simple MVP built with **Tailwind CSS + HTML + JavaScript + MySQL (PHP API)**.

## Features
- Landing page with explanation, usage, and rules.
- User registration (username, phone, password).
- "Make first post" flow.
- Request posting form (description, delivery, optional time, price).
- Bid history section for users.
- Admin dashboard to review posts and send offer messages.

## Project Structure
- `public/index.html` - Landing page.
- `public/register.html` - Registration.
- `public/post.html` - User dashboard + post form + bid history.
- `public/admin.html` - Admin dashboard to review and reply.
- `public/js/app.js` - Front-end logic.
- `api/api.php` - Backend endpoints.
- `api/config.example.php` - DB config template.
- `database/schema.sql` - MySQL schema.

## Quick start
1. Create a MySQL database and run `database/schema.sql`.
2. Copy `api/config.example.php` to `api/config.php` and set credentials.
3. Serve project with PHP (example):
   ```bash
   php -S localhost:8000 -t public
   ```
4. API is expected at `/../api/api.php` from the `public` pages (works in this layout when served from repo root or adjusted virtual host).

## Admin login
- Default admin passcode in example config: `oru_admin_123`.
- Change it in `api/config.php` before using in production.

## Notes
- This is a simple MVP and not production-hardened.
- Add stronger auth, rate limiting, validation, and moderation for real-world use.
