ARCO GLOBAL MEDIA — DEPLOY PACKAGE
==================================

GO LIVE (about 5 minutes)

1. Go to app.netlify.com and sign in (GitHub or email).
2. Choose "Add new site" > "Deploy manually".
3. Drag this ENTIRE folder onto the drop zone.
   The site goes live immediately on a temporary address
   like random-name-123.netlify.app. Open it and check it.

CONNECT THE DOMAIN

4. In Netlify: Site configuration > Domain management >
   "Add a domain". Enter arcoglobalmedia.com.
   Netlify will show you the DNS records it needs.

5. In Squarespace: Settings > Domains > arcoglobalmedia.com >
   DNS Settings.
   - Delete the existing A records that point to Squarespace.
   - Add the four A records Netlify gives you for the root
     domain (@), and the CNAME for "www".
   - Save.

6. Wait for DNS (usually under an hour, occasionally longer).
   Netlify issues the HTTPS certificate automatically once
   the domain resolves. No action needed.

7. Once https://arcoglobalmedia.com loads the new site,
   cancel the Squarespace WEBSITE subscription.
   KEEP the domain registration active — that is separate.

THE CONTACT FORM

Netlify picks up the form automatically on first deploy.
To have submissions emailed to Ben:
  Site configuration > Forms > Form notifications >
  "Add notification" > Email notification >
  enter ben@arcoglobalmedia.com.
Every submission is also stored in the Forms tab as a
permanent record. There is no activation link to click.

FILES

  index.html             homepage
  case-study.html        Toys"R"Us x PPA Finals
  press.html             market coverage
  brand-kit.html         logos, colour, type, boilerplate
  support.js             page runtime (required)
  brand/                 logo, favicon, social card
  brandkit/              downloadable brand kit
  img/                   photography and portraits
  logos/ logos-color/    team and partner logos
  roster/                represented property logos
  robots.txt sitemap.xml search engine files
  _redirects             clean URLs (/press, /case-study)
  netlify.toml           caching and security headers

FUTURE EDITS

Edit the source, export a fresh deploy folder, then drag it
onto the same Netlify site under "Deploys". It replaces the
live version in seconds. Nothing else needs to change.
