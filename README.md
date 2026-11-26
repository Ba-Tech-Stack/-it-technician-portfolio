# IT Technician Portfolio — GitHub Edition

A repository-ready portfolio package containing two deployment targets:

- **GitHub Pages site:** `docs/` — static HTML, CSS and JavaScript; can be hosted free on GitHub Pages.
- **Full PHP/MySQL application:** `php-app/` — V3 dynamic portfolio with admin dashboard, projects, skills, certificates, CV upload and contact-message storage. GitHub Pages cannot execute PHP or host MySQL; deploy this folder to a PHP/MySQL web host.
- **Professional CV:** `cv/` — PDF and editable DOCX versions.

## Publish the free GitHub Pages website

1. Create a GitHub account at https://github.com/ and create a **public** repository named `it-technician-portfolio`.
2. Extract this ZIP. Open the extracted folder in File Explorer.
3. Upload all repository contents (including hidden `.github` folder) to the repository, or use Git:

```bash
git init
git add .
git commit -m "Add professional IT technician portfolio"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/it-technician-portfolio.git
git push -u origin main
```

4. In GitHub, open **Settings → Pages**. Under Build and deployment choose **GitHub Actions**.
5. The included workflow deploys the `docs/` folder. After it completes, your site will be available at `https://YOUR_USERNAME.github.io/it-technician-portfolio/`.

## Deploy the dynamic PHP/MySQL version

GitHub Pages cannot run PHP or MySQL. Deploy the contents of `php-app/` to a PHP 8+ host with MySQL/MariaDB and PDO MySQL enabled. Import `php-app/database.sql`, configure `php-app/includes/config.php` with your host's database credentials, enable HTTPS, create the first admin through `admin/setup.php`, then disable/remove the setup endpoint. Never commit real database passwords, private keys, uploaded personal documents or production secrets to GitHub.

## Personalise before publishing

Search and replace these placeholders in `docs/index.html` and complete the CV:
- `YOUR_EMAIL@example.com`
- `+254 7XX XXX XXX`
- `YOUR_GITHUB_USERNAME`
- Add LinkedIn URL, accurate education, qualification dates, employment dates and verified certifications.

The experience summary is based on the supplied background in Jitume/digital-skills coordination at Kaloleni Technical and Vocational College. Confirm job title and dates before sending applications. Project descriptions are portfolio summaries; add live links/screenshots only for work you have actually completed.

## CV

- `cv/Professional_IT_Technician_CV.pdf` — ready-to-review PDF.
- `cv/Professional_IT_Technician_CV.docx` — editable Word document.

## Repository structure

```text
.
├── .github/workflows/pages.yml
├── docs/                 # GitHub Pages static site
├── php-app/              # Dynamic PHP/MySQL V3 application
├── cv/                   # PDF + editable CV
├── .gitignore
└── README.md
```
