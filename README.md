# baypath-sponsors

The Baypath Sponsors app (`index.html`), hosted on GitHub Pages. It reads and edits the Obsidian vault's
`Network/Organizations` and `Network/People` notes from one of three places:

- **A folder on this device** (Chrome or Edge on a computer)
- **A GitHub repository** (any device, including a phone; no Google sign-in)
- **Google Drive** (needs a Google OAuth client; blocked on accounts in Google's Advanced Protection Program)

## Notes in a GitHub repository

Do **not** put the notes in this repository: it is public, and the notes hold names, emails and phone numbers.

1. Create a **private** repository for the notes, for example `baypath-notes`.
2. Upload the vault's `Network` folder (with `Organizations` and `People` inside) to it. It can sit at the top of
   the repository or deeper (for example `Obsidian/Network`); the app finds it.
3. Make a fine-grained token at GitHub → Settings → Developer settings → Personal access tokens →
   Fine-grained tokens:
   - Repository access: **Only select repositories** → the notes repository
   - Permissions: **Contents: Read and write**
   - Pick an expiration date and note it; make a new token when it expires.
4. Open the app → Settings → GitHub. Enter the repository (`owner/name`), paste the token, then tap
   **Use the GitHub repository**. Repeat the token step on each device; the token stays in that browser only.

Each save from the app is a commit to the note's `.md` file. To keep Obsidian on a computer in step, open a clone of
the notes repository as (or inside) the vault and sync it with the Obsidian Git community plugin or GitHub Desktop.
