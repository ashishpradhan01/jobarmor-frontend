# JobArmor Website

Multi-page marketing and utility website for the JobArmor Chrome extension.

## 📄 Pages

| Page        | File           | Purpose                             | Supabase Endpoint  |
| ----------- | -------------- | ----------------------------------- | ------------------ |
| **Home**    | `index.html`   | Product showcase, features, pricing | —                  |
| **Upgrade** | `upgrade.html` | Payment flow with Razorpay          | `initiate-pay`     |
| **Recover** | `recover.html` | OTP subscription recovery           | `recovery-manager` |
| **Help**    | `help.html`    | FAQ, How It Works, Privacy Policy   | —                  |

## 🎨 Design System

Using the **Obsidian Glass** theme:

| Token              | Value                   |
| ------------------ | ----------------------- |
| `--bg-primary`     | `#0D0D0D`               |
| `--bg-card`        | `rgba(26, 26, 26, 0.8)` |
| `--border-color`   | `#2A2A2A`               |
| `--text-primary`   | `#FFFFFF`               |
| `--text-secondary` | `#B0B0B0`               |
| `--accent-success` | `#10B981` (Emerald)     |

## 🚀 Setup

### 1. Update Supabase URL

In `upgrade.html` and `recover.html`, update:

```javascript
const CONFIG = {
  SUPABASE_URL: "https://YOUR_PROJECT_REF.supabase.co/functions/v1",
};
```

### 2. Deploy

Host on any static hosting:

```bash
# Vercel
vercel deploy

# Netlify
netlify deploy --prod

# Or drag & drop to Cloudflare Pages
```

## 🔗 URL Structure

```
https://jobarmor.work/                    → Home
https://jobarmor.work/upgrade.html?uuid=xxx    → Payment (from extension)
https://jobarmor.work/recover.html?uuid=xxx    → Recovery (from extension)
https://jobarmor.work/help                → Help & Privacy
```

## 📱 Responsive

All pages are fully responsive for desktop, tablet, and mobile.
