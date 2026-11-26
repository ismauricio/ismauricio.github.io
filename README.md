# pudim — your website

## Publish (free)
1. Sign in at github.com as ismauricio. Create a PUBLIC repository named exactly `ismauricio.github.io` (if it already exists, back it up before making changes). Initialize with a README if needed.
2. Unzip the website package. In the repository, click Add file > Upload files. Drag the CONTENTS of the pudim folder, not the folder itself. Include folders such as `_layouts`, `_data`, and `assets`. Commit changes to main. Do not upload the separate preview or your original resume.
3. Go to Settings > Pages. Under Build and deployment, choose Deploy from a branch, main, / (root), Save. Check Actions for a successful build. Visit https://ismauricio.github.io/ when deployment finishes. Enable Enforce HTTPS if available.
4. If that repository is already used for something else, use a repository named pudim instead and change baseurl in _config.yml to "/pudim"; the address will be https://ismauricio.github.io/pudim/.

## Write a new post
Click Add file > Create new file. Name it `_posts/2026-11-26-my-first-post.md` (use the actual date and a unique lowercase slug). Paste the contents of templates/post.md, change the title, and write beneath the second `---`. Use blank lines for paragraphs, `##` for headings, `*italic*` for italics, `**bold**` for bold, and `[link text](https://example.com)` for links. Click Preview to inspect Markdown, then Commit changes to publish. The writing page and homepage update automatically. The search covers titles and post text.

## Drafts
Keep private drafts in a local Notes app or local Markdown file. A public repository exposes EVERY committed file, even `_drafts` and deleted history. If you are comfortable with a draft being visible in source but not on the site, use `_drafts/my-post.md`; publish by moving it to `_posts/YYYY-MM-DD-my-post.md`. The included example draft is generic. GitHub's browser editor is free; press `.` on your repository homepage to open github.dev, a more capable file editor. Save work by committing. No separate CMS account is needed.

## Scenes
Upload photos into assets/images/ (lowercase simple names; resize and remove metadata first). Open `_data/scenes.yml`, click the pencil, and replace `[]` with entries like:

```yaml
- image: /assets/images/seoul.jpg
  alt: "A quiet street in Seoul"
  caption: "Seoul, summer"
  date: "2026"
```

Add more entries using the same pattern. Only use photos you have permission to publish.

## Inspiration
Open `_data/inspiration.yml`. Replace `[]` with any mix of entries. Example formats (not actual recommendations):

```yaml
- title: "A song I like"
  url: "https://example.com"
  text: "A short thought about it."
- image: /assets/images/my-art.jpg
  alt: "Description of the artwork"
  title: "Artwork title"
  credit: "Artist, year"
- text: "A thought worth keeping."
```

Fields are optional. Entries share a single masonry board, not categories. Add new ones at the top if desired. Use your own, licensed or public-domain images; link to copyrighted songs, movies and artwork rather than uploading unauthorized copies. Only use http/https links. Keep YAML indentation consistent and quote text containing punctuation.

## Visitor analytics (free, not active yet)
Create a free Cloudflare account and open Web Analytics. Add ismauricio.github.io as a site using manual setup (no DNS changes). Copy the token from the provided beacon snippet into `_config.yml` as cloudflare_token: "YOUR_TOKEN". Commit. The site already includes the conditional beacon on every page; no account password or secret is needed. See https://developers.cloudflare.com/web-analytics/ for details. If you change domains, update the analytics site. Analytics will collect visits only after setup.

## Other edits
About text: about/index.html. Experience: _data/experience.yml. Research: research/index.html. Homepage: index.html. Colors and layout: assets/css/style.css. No full name, email, phone, resume, or reference details are included in the site. However the GitHub username and public profile can disclose identity. Google indexing is allowed but not guaranteed. Avoid committing private information.

## Local technical preview (optional)
With Ruby and Bundler installed, `bundle install` and `bundle exec jekyll serve` then open http://localhost:4000. For a nontechnical preview, use the separate preview ZIP and open its index.html. Preview reflects the initial content, not future edits.
