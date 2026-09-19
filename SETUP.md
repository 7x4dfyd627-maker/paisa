# Paisa on your iPhone — permanent, free, no Xcode

This folder is the complete app. Put it on GitHub Pages once, add it to your
Home Screen, and it never expires and never needs your Mac again.

**Before you start:** open the current Xcode-built Paisa on your iPhone,
go to Settings → Back up data → **Copy**, and paste that text into Notes.
You will paste it back at Step 9.

---

## Step 1 — Create a GitHub account
Go to github.com and sign up (free). Skip if you already have one.

## Step 2 — Create a repository
1. Click the **+** at the top right → **New repository**
2. Repository name: `paisa`
3. Choose **Public** (required for free GitHub Pages)
4. Click **Create repository**

## Step 3 — Upload these files
1. On the new repo page click **uploading an existing file**
2. Drag in **all of these, keeping the icons folder**:
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - the whole `icons` folder
3. Click **Commit changes**

Your repo should now list: index.html, manifest.webmanifest, sw.js, icons/

## Step 4 — Turn on GitHub Pages
1. In the repo, click **Settings** (top bar)
2. In the left sidebar click **Pages**
3. Under "Build and deployment" → Source: **Deploy from a branch**
4. Branch: **main**, folder: **/ (root)** → **Save**
5. Wait 1–2 minutes, then refresh the page. It shows your link:
   `https://YOUR-USERNAME.github.io/paisa/`

## Step 5 — Write the link down
That address is where your app lives. Your saved data is tied to it,
so never rename the repo afterwards.

## Step 6 — Open it in Safari on your iPhone
Type the link into **Safari** (it must be Safari — not Chrome).
The app should load.

## Step 7 — Add it to your Home Screen
1. Tap the **Share** button (square with an arrow, at the bottom)
2. Scroll down → **Add to Home Screen**
3. Name it **Paisa** → **Add**

You now have a Paisa icon on your Home Screen.

## Step 8 — Always use the Home Screen icon
Open Paisa from the icon, not from Safari. Safari and the icon keep
separate data, and only the icon version runs full screen.

## Step 9 — Restore your data
In the Home Screen app: Settings → **Restore from copied text** →
paste the backup from Notes → **Restore**.

Check that your accounts, transactions and balances are all there.
Once confirmed, you can delete the Xcode-built app from your phone.

---

## Updating the app later

When you get a new `index.html`:

1. Open your repo on github.com → click `index.html` → the **pencil** icon
2. Delete everything and paste the new file's contents → **Commit changes**
   *(or: Add file → Upload files → drop the new index.html → commit)*
3. Edit `sw.js` the same way and change the version line near the top,
   e.g. `const CACHE_VERSION = "paisa-v4.3";` → commit
4. On your iPhone: close Paisa completely (swipe it away in the app
   switcher), wait a moment, and reopen it

**Your data is not affected by updates.** Check Settings at the bottom to
confirm the new version number is showing.

---

## Good habits

- **Back up monthly.** Settings → Back up data → Copy → paste into Notes or
  email it to yourself. iOS can clear a web app's storage if the app goes
  unused for a very long time, and there is no iCloud backup of it.
- **Keep the URL the same.** Renaming the repo creates a new address, which
  means an empty app. If you ever must, back up first and restore after.
- **Offline works.** After the first load, the app runs with no internet.
  Only PDF statement import and online rate updates need a connection.

## If something goes wrong

- **Blank page after opening the link:** wait 2 minutes — Pages takes a
  moment on the first deploy — then reload.
- **Old version still showing:** confirm you changed the version in `sw.js`,
  then close the app fully from the app switcher and reopen.
- **Icon looks wrong:** make sure the `icons` folder uploaded with its files
  inside, then remove the Home Screen icon and add it again.
