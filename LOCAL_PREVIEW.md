# Local Preview Guide

Use this guide when you want to test the website on your computer before publishing it to GitHub Pages.

## The important rule

Do **not** double-click `index.html` to preview the public website.

Double-clicking opens an address like this:

```text
file:///C:/.../index.html
```

The website loads its content from `hackathon.config.yml`. Browsers block that file request when the page is opened with `file:///`, so your new configuration will not appear.

Instead, run a small local web server and open an `http://localhost` address.

## Preview with Python (recommended)

### One-time requirement

Install Python 3 if it is not already installed. During installation, select the option to add Python to your PATH.

### Start the local server

1. Open PowerShell.
2. Go to the folder that contains `index.html` and `hackathon.config.yml`:

```powershell
cd "C:\path\to\your\repository"
```

3. Start the server:

```powershell
python -m http.server 8000
```

4. Keep that PowerShell window open.
5. In your browser, open:

```text
http://localhost:8000/
```

The setup generator is available at:

```text
http://localhost:8000/setup/
```

## Make and check a change

1. Edit or replace the root `hackathon.config.yml` file.
2. Save the file.
3. Go back to `http://localhost:8000/`.
4. Refresh the browser. If needed, use `Ctrl + Shift + R` on Windows or `Cmd + Shift + R` on macOS.
5. Confirm the new name, dates, tracks, or other edited content appears.

No server restart is normally required after changing YAML.

## Stop the local server

Return to the PowerShell window that is running the server and press `Ctrl + C`.

## If Python is not available

First try this command:

```powershell
py -m http.server 8000
```

If that also does not work, install Python 3 or use the **Live Server** extension in Visual Studio Code:

1. Open the repository folder in VS Code.
2. Install the “Live Server” extension by Ritwick Dey.
3. Right-click `index.html` and select **Open with Live Server**.
4. Use the `http://localhost:...` address that it opens; do not use a `file:///` address.

## Local preview checklist

- `hackathon.config.yml` is in the same root folder as `index.html`
- The file is named exactly `hackathon.config.yml`, not `hackathon.config.yml.txt`
- The browser address starts with `http://localhost`, not `file:///`
- You saved the YAML file before refreshing
- You used spaces rather than tabs if you edited YAML by hand
