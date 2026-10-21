# Dr. Talha Khalid — Physiotherapy website

A fast static website (no server, no database). Pages: Home, Conditions (19 guides), Booking, Hijama calendar, Reviews. Bookings and reviews are sent to WhatsApp.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole website |
| `404.html` | Page shown for wrong addresses |
| `robots.txt` | Lets search engines read the site |
| `.nojekyll` | Tells GitHub to publish the files as they are |
| `LICENSE` | All-rights-reserved copyright notice |

## Publish on GitHub Pages (free)
1. Create a GitHub account at github.com and turn on two-factor authentication (Settings > Password and authentication).
2. Click **New repository**. Name it `dr-talha-khalid`, choose **Public** (GitHub Pages is free for public repositories), click **Create repository**.
3. Click **uploading an existing file**, drag in ALL files from this folder (including `.nojekyll`; if your computer hides it, skip it, the site still works), and click **Commit changes**.
4. Open **Settings > Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch **main**, folder **/ (root)**, then **Save**.
5. Wait 1–3 minutes. Your site is live at `https://YOUR-USERNAME.github.io/dr-talha-khalid/`. (Name the repository `YOUR-USERNAME.github.io` to get the shorter address `https://YOUR-USERNAME.github.io/`.)

## Use your own domain (optional, paid)
`.pk` domains are not free; buy one from PKNIC or a registrar.
1. In **Settings > Pages > Custom domain**, type your domain (for example `www.drtalhakhalid.pk`) and **Save**.
2. At your domain provider's DNS settings:
   - For `www`: add a **CNAME** record pointing to `YOUR-USERNAME.github.io`.
   - For the bare domain (apex): add four **A** records pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
3. Wait for DNS to update (up to 24 hours), then tick **Enforce HTTPS** in Settings > Pages.
Remove any other A, AAAA or CNAME records on the same names, because extra records can stop the HTTPS certificate from being issued.

## Editing the website
Open `index.html` on GitHub and click the pencil icon. Use Ctrl+F to find:
- **Phone, WhatsApp, hours, addresses, headline, colors, fonts:** find `const DEF=`. Change the values inside the quotes (`ph`, `wa`, `hrs`, `l1`, `l2`, `h1`, `hp`, `pri`, `acc`, `bg`, `ink` and so on).
- **Reviews:** find `const R=[`. Each review looks like `{n:'Name',c:'Condition',r:5,t:'Review text'}`. Copy a line to add one, delete a line to remove one, and keep a comma between lines. Do not use a straight apostrophe inside the text; type ’ instead.
- **Condition guides:** find `const D={` for the long guides and `const C=[` for the list.
Click **Commit changes**; the live site updates in about a minute.
Note: the in-page Settings panel only works on the Claude-hosted version, not on GitHub. Edit the file as above instead.

## Security checklist
- Two-factor authentication on GitHub, your domain registrar, email and WhatsApp.
- Never put passwords or keys into any file, because a public repository is visible to everyone.
- Ask patients to share only the details needed for booking.

## Copyright
Keep the copyright line in the footer and the `LICENSE` file. Only publish text, images and reviews you own or have permission to use (get the patient's consent for reviews).
