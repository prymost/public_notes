# My Personal Notes & Blog

This is my personal blog and notes repository built with [Zola](https://www.getzola.org/) and the [Cela theme](https://github.com/edwardzcn-decade/cela).

## 🚀 How to Run Locally

Since this project is set up with a **DevContainer**, you don't need to install anything locally.

1.  **Open in VS Code**: Open this folder.
2.  **Reopen in Container**: Click the green button in the bottom-left corner or use the Command Palette (`Ctrl+Shift+P`) and select **"Dev Containers: Reopen in Container"**.
3.  **Start the Server**: Open the terminal inside VS Code and run:
    ```bash
    zola serve
    ```
4.  **View Site**: Open [http://localhost:1111](http://localhost:1111) in your browser.

## 📝 Writing Content

-   **Automatic**: Run the helper script to create a post with correct metadata:
    ```bash
    ./new_post "My New Post"
    ```
-   **Manual**: Add new Markdown files to `content/blog/`. Every post needs a "Front Matter" block at the top:
    ```markdown
    +++
    title = "My New Post"
    date = 2026-02-26
    +++
    Your content here...
    ```

## 🌐 Deployment

Deployment is **automatic**.
- Whenever you push changes to the `main` branch, a GitHub Action will build and deploy the site to GitHub Pages.
- Submodules are automatically updated during the build.

## 🛠 Project Structure

- `content/blog/`: Where your posts live.
- `config.toml`: Main configuration (titles, menu, theme settings).
- `static/css/custom.css`: Custom styles (e.g., used to hide the language picker).
- `templates/`: Local template overrides (keeps the theme submodule clean).
- `.devcontainer/`: Environment configuration for Zola and Zsh.
