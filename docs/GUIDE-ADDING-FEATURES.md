# How to Add Features to Your Static Site

Since your site is now **Static HTML** (and not WordPress), you handle updates differently.

## 1. Posting Updates (News/Blog)
You don't have a "Dashboard" anymore. To add an update:
1. Copy an existing page (like `issues.html`) to a new file (e.g., `update-dec-2025.html`).
2. Edit the text in your text editor.
3. Add a link to it on your Homepage (`index.html`).

## 2. Collecting Grievances (Forms)
Because we deleted the database, **contact forms won't work** the old way. You cannot use PHP or WordPress plugins.

**The Solution: Embeds**
The easiest, free way to collect grievances securely is to embed an external form.

### Recommended Tools:
- **Google Forms:** Free, unlimited responses.
- **Tally.so:** Beautiful, free tier, looks like a Notion doc.
- **Formspree:** Allows you to keep your existing HTML form but sends the data to your email (requires a small setup).

### Example: Adding a Google Form
1. Create the form in Google Forms.
2. Click **Send > <> (Embed)**.
3. Copy the `<iframe>` code.
4. Paste it into your `index.html` or a new `grievances.html` page.

## 3. Workflow
Always try these changes on your `staging` branch first!
```bash
git checkout staging
# Create your new page...
# Test it...
git add .
git commit -m "Add grievance form"
git push origin staging
```
