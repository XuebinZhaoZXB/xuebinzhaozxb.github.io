# Xuebin Zhao | Academic Website

Source files for my academic website: <https://xuebinzhaozxb.github.io/>.

The site is published automatically through GitHub Pages. After committing and pushing changes to GitHub, the website will normally update within a few minutes.

## The files you will edit most often

For routine website updates, start with the `content` folder:

| What you want to update | File to edit |
| --- | --- |
| Homepage biography | `content/about.md` |
| Research overview | `content/research.md` |
| Publication list | `content/publications.md` |
| Teaching and student supervision | `content/teaching.md` |
| CV overview | `content/cv.md` |

These are Markdown files and can be edited directly in VS Code. Saving a file does not require you to generate the website manually.

There are also three important locations used less often:

| Content | Location |
| --- | --- |
| Name, position, email, academic-profile links and avatar filename | The `author:` section of `_config.yml` |
| Navigation bar | `_data/navigation.yml` |
| Images, PDFs and supplementary material | `images/`; create `files/` when you need to upload PDFs |

Do not edit `_layouts/`, `_includes/`, `_sass/` or `assets/` for routine content updates. They contain the site template and styling code.

## Simple Markdown rules

- Start a heading with `#` or `##`; use `##` for major sections within a page.
- Start each list item with `- `.
- Create a link with `[link text](https://example.com)`.
- Add two spaces before a line break to place an institution and a year on separate lines within a list item.
- The text between the first `---` and the second `---` in each content file contains page settings. Normally, leave it unchanged and edit the text below it.

### Updating publications

Add one line in the appropriate section of `content/publications.md`, following the existing format:

```markdown
1. Zhao, X. and Coauthor, A. (2027). *Paper title*. Journal name. [DOI](https://doi.org/example).
```

Markdown will renumber the list automatically, so every item may start with `1.`. Add published work under `Peer-reviewed journal articles` and unpublished work under `Manuscripts under review`.

### Replacing the avatar or adding images

1. Put the image in `images/`, using a lowercase English filename with hyphens, for example `conference-2027.jpg`.
2. To use an image as the sidebar avatar, enter its filename in `_config.yml`:

```yaml
avatar: "your-photo.jpg"
```

The current avatar is `images/xuebin-zhao-avatar.jpg`.

## Adding a News page

Use News for appointments, publications, awards, conferences, talks or project updates. Create `content/news.md`, then copy and adapt the following:

```markdown
---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

## 2027

- **January 2027** — Add a short update here.

## 2026

- **September 2026** — Add a short update here.
```

Then open `_data/navigation.yml` and add the following under `main:`:

```yaml
  - title: "News"
    url: /news/
```

Keep the newest items at the top. If a full blog-style news system is needed later, `_posts/` can be enabled again; a static News page is simpler and well suited to an academic website.

## Adding a team or students page

Create `content/team.md` with this structure:

```markdown
---
layout: archive
title: "Students and collaborators"
permalink: /team/
author_profile: true
---

## Current students

- **Name** — PhD student, University of Edinburgh. Topic: ...

## Former students

- **Name** — Degree, graduation year. Current position: ...
```

Then add this entry to `_data/navigation.yml`:

```yaml
  - title: "Team"
    url: /team/
```

If you only want to list students, change the page title to `Students` and the URL to `/students/`.

## Adding a Chinese version

The recommended approach is to keep English as the main site and create parallel Chinese pages inside `content/zh/`. For example, create `content/zh/index.md` for the Chinese homepage:

```markdown
---
layout: archive
title: "赵学彬"
permalink: /zh/
author_profile: true
---

Write the Chinese biography here.
```

Create `content/zh/research.md` for the Chinese research page and set:

```yaml
permalink: /zh/research/
```

The same pattern can be used for `/zh/publications/`, `/zh/teaching/` and `/zh/cv/`. Finally, add this to the navigation bar:

```yaml
  - title: "中文"
    url: /zh/
```

It is best to create the Chinese homepage first and add the other pages gradually. English and Chinese pages are separate, so both versions need to be updated when content changes.

## Publishing changes to GitHub

In the Source Control panel in VS Code:

1. Review the files changed in this update.
2. Click `+` to stage the changes you want to publish.
3. Write a short commit message, such as `Update publications`.
4. Click **Commit**.
5. Click **Sync Changes** or **Push**.

After pushing, visit the repository's **Actions** page or wait a few minutes and refresh the website. If the page does not change, first confirm that the push succeeded, then check the GitHub Pages deployment status.

## Pre-publication checklist

- The links on About, Research, Publications, Teaching and CV all work.
- Publication years, authors, journal names and manuscript statuses are accurate.
- Email, Google Scholar, ResearchGate and GitHub links are correct.
- New images are stored in `images/` and display correctly.
- No CV documents, certificates, private photographs, student information or unpublished material are uploaded unintentionally.

## Credits and licence

This website is built with [AcademicPages](https://academicpages.github.io/), which is based on the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Jekyll theme. Both are released under the MIT License. The [`LICENSE`](LICENSE) file is retained in this repository; please keep the licence and relevant copyright notices when modifying or reusing the website code.

Website text, photographs and research content are copyright Xuebin Zhao unless otherwise stated.
