# AGENTS.md - Project Context

## Project Overview
This project is a personal blog and notes website built using [Zola](https://www.getzola.org/), a static site generator written in Rust. It utilizes the [Cela theme](https://github.com/edwardzcn-decade/cela) (integrated as a git submodule) for its UI and layout.

### Core Tech Stack
- **Static Site Generator:** Zola
- **Content Format:** Markdown (with TOML front matter)
- **Styling:** CSS (with custom overrides in `static/css/custom.css`)
- **Deployment:** GitHub Pages via GitHub Actions
- **Environment:** VS Code DevContainers (pre-configured with Zola)

## Building and Running

### Local Development
The project is designed to be run within a DevContainer. Once the container is active, use the following command:

```bash
zola serve
```
The site will be available at `http://localhost:1111`.

### Production Build
To generate the static files for deployment (found in the `public/` directory):

```bash
zola build
```

## Project Structure

- `config.toml`: Central configuration for site metadata, taxonomies (tags/categories), and theme-specific settings (`[extra.cela]`).
- `content/`: Contains all Markdown content.
  - `content/_index.md`: Configuration for the homepage.
  - `content/blog/`: Directory for blog posts.
- `static/`: Static assets (images, custom CSS).
- `templates/`: Local HTML template overrides to customize the theme without modifying the submodule directly.
- `themes/cela/`: The theme's source code (Git submodule).
- `.github/workflows/deploy.yml`: CI/CD pipeline for building and deploying to GitHub Pages.

## Development Conventions

### Creating New Content
To create a new post with the correct front matter, use the helper script:

```bash
./new_post "My New Post"
```

Alternatively, you can manually add a new `.md` file to `content/blog/`. Every file MUST have TOML front matter:
   ```markdown
   +++
   title = "My New Post"
   date = 2026-02-28
   [taxonomies]
   tags = ["tech", "zola"]
   categories = ["notes"]
   +++
   Your content goes here.
   ```

### Customization
- **Styles:** Add custom CSS to `static/css/custom.css`.
- **Layouts:** To override a theme component, copy the template from `themes/cela/templates/` to the root `templates/` directory and modify it there.

### Deployment
Deployment is automatic on every push to the `main` branch. Ensure all submodules are updated if changes are made to the theme.
