# CAE Lab Link Portal

Static link portal for CAE Lab resources. The portal displays hierarchical categories, nested groups, regular links, buttons, notes, and coming-soon items from `site-content.json`.

## Files

- `index.html` — public-facing portal.
- `admin.html` — browser-based editor for the data file. It can import/export JSON, edit categories and nested groups, and download the updated file.
- `site-content.json` — portal content and links.

## Add or update links

1. Open the published site and select **Manage links**, or open `admin.html` through a web server.
2. Add/edit sections, items, or nested groups. Choose **Link** or **Button**, then provide its label and URL.
3. Select **Download site-content.json**.
4. Replace `site-content.json` in this repository with the downloaded file and commit the change. GitHub Pages will deploy the updated portal.

The manager intentionally does not write to GitHub directly and does not contain a GitHub access token. To make changes in the repository, sign in to GitHub and have write permission. Multiple editors should coordinate commits to avoid overwriting one another.

## Link and privacy notes

- Use `https://`/`http://` or relative paths. For internal documents, prefer an approved company intranet or SharePoint URL.
- A GitHub Pages website cannot reliably open Windows SMB paths such as `\\server\share`; browser security and company policy may block them.
- The current `cont-hyoushi.htm`, `CONTENTS_new.htm`, and `HYOUSHI.htm` snippets refer to companion files, but do not include direct URLs to the actual manual documents. For example, the old pages reference `CONTENTS.htm`, `HYOUSHI.htm`, `CONTENTS_files/sheet001.htm`, and `HYOUSHI.files/sheet001.htm`. The companion files must remain available at their original location for the legacy pages to work.
- Do not put restricted content, credentials, private tokens, or sensitive internal server details in a public repository or public site. Anyone can read content in a public repo/site. Internal documents still enforce their own access permissions, but link names and URLs can be exposed.

## GitHub Pages

After the repository is made public (or Pages access is otherwise available for the repository), configure Pages in **Settings → Pages** to deploy from the `main` branch and `/ (root)`. The portal URL will be shown in the Pages settings after deployment. The repository itself is currently private; making it public is a separate repository setting.
