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
  vendor/                React, React-DOM and Babel (required)
  video/                 the PPA Finals film and the loop
  brand/                 logo, favicon, social card
  brandkit/              downloadable brand kit
  img/                   photography and portraits
  logos/ logos-color/    team and partner logos
  roster/                represented property logos
  robots.txt sitemap.xml search engine files
  _redirects             clean URLs (/press, /case-study)
  netlify.toml           caching and security headers

The folder is about 45 MB. The film is most of that.

THE VIDEO

  video/arco-ppa-reel.mp4      the full film, 2:33
  video/ppa-finals-loop.mp4    the 5s loop on the home page
  img/ppa-film-poster.jpg      the still behind the play button
  img/ppa-finals-poster.jpg    the still behind the loop

The film does not download until a visitor clicks play.
To change the film, replace the file and keep the name.
To change a poster, replace the .jpg and keep the name.

THE vendor/ FOLDER — DO NOT DELETE

The pages load React and Babel from vendor/, not from the
internet. A short script in the <head> of every page maps the
old unpkg.com addresses to these local files:

  window.__resources = { ... }

Without vendor/, every page renders blank when unpkg.com is
slow or down. Keep the folder and keep the script.

FUTURE EDITS

Edit the source, export a fresh deploy folder, then drag it
onto the same Netlify site under "Deploys". It replaces the
live version in seconds.

WARNING: a fresh export overwrites the HTML. Three changes
live in the exported HTML and are lost on every export:

  1. The window.__resources script in each <head>.
  2. The local img/cs-*.webp paths on the case study page,
     which replaced images hosted by Squarespace.
  3. The film and loop markup on the case study page and
     the home page.

Put these three changes into the builder source. Until you
do, check for them after every export.
