# Academic Portfolio

Personal academic website

## Repository Structure

```
your-username.github.io/
├── index.html                          # Main website
├── data/                               # JSON data files
│   ├── publications.json              # Publications data
│   ├── teaching.json                  # Teaching data
│   ├── press.json                     # Press/media coverage data
│   ├── research.json                  # Research projects data
│   └── misc.json                      # Awards, service, other info
├── publications/                       # Folder containing all publication PDFs
│   ├── example-publication-2024.pdf
│   ├── another-publication-2023.pdf
│   └── conference-paper-2024.pdf
├── README.md                           # This file
└── .gitignore                          # Git ignore file
```

## How It Works

The website uses **JSON data files** to manage content. Instead of editing HTML directly, you simply update the JSON files in the `data/` folder, and the website automatically loads and displays the information.

**Benefits:**
- ✅ Easy to add/remove publications, teaching, etc.
- ✅ Clean separation between data and presentation
- ✅ No HTML editing needed
- ✅ Consistent formatting automatically applied

## Updating Your Content

### Publications
Edit `data/publications.json` to add/remove publications organized by year:

```json
{
  "2024": [
    {
      "title": "Your Paper Title",
      "authors": "Your Name, Co-Authors",
      "venue": "Journal Name",
      "type": "journal",
      "pdf_file": "your-paper-filename.pdf",
      "doi": "https://doi.org/10.xxxx/xxxxx"
    },
    {
      "title": "Conference Paper",
      "authors": "Your Name, Co-Authors",
      "venue": "Conference Name",
      "type": "conference",
      "pdf_file": "conference-paper.pdf",
      "doi": "https://doi.org/10.xxxx/xxxxx"
    }
  ],
  "2023": [...]
}
```

**Type options:** `"journal"` or `"conference"` (displayed as colored badges)

### Teaching
Edit `data/teaching.json` to add courses:

```json
{
  "courses": [
    {
      "name": "Course Name",
      "institution": "University Name",
      "semester": "Spring 2024",
      "role": "Instructor",
      "description": "Course description..."
    }
  ]
}
```

### Press & Media
Edit `data/press.json` to add media coverage organized by year:

```json
{
  "2024": [
    {
      "title": "Article Title",
      "publication": "Publication Name",
      "date": "2024-01-15",
      "url": "https://example.com/article",
      "description": "Brief description..."
    }
  ],
  "2023": [...]
}
```

### Research Projects
Edit `data/research.json` to add research projects:

```json
{
  "projects": [
    {
      "name": "Project Name",
      "role": "Principal Investigator",
      "funding": "Funding Agency",
      "duration": "2023-2025",
      "description": "Project description..."
    }
  ]
}
```

### Miscellaneous
Edit `data/misc.json` to add awards, service, and other info:

```json
{
  "awards": [...],
  "service": [...],
  "other": [...]
}
```

## Social Profiles

The social profile icons are set up as empty SVG containers. To use your own custom SVGs:

1. Find or create the SVG code for each social platform
2. Open `index.html` and find the social profiles section in the hero
3. Replace the `<!-- LINK TO YOUR SVG -->` comment with your actual SVG code

For example, for ORCID:
```html
<a href="https://orcid.org/YOUR-ORCID-ID" target="_blank" rel="noopener noreferrer" title="ORCID">
    <svg viewBox="0 0 256 256" xmlns="http://www.w3.org/2000/svg" width="24" height="24">
        <!-- Your ORCID SVG code here -->
        <circle cx="128" cy="128" r="128" fill="#a6ce39"/>
        <path d="M86.3 186.2H70.9V79.1h15.4v107.1z..." fill="#fff"/>
    </svg>
</a>
```

Also update the profile URLs:
```html
<a href="https://orcid.org/0000-0000-0000-0000" ... > → Your ORCID URL
<a href="https://www.linkedin.com/in/yourprofile/" ... > → Your LinkedIn
<a href="https://github.com/yourprofile" ... > → Your GitHub
<a href="https://scholar.google.com/citations?user=XXXXX" ... > → Your Scholar ID
<a href="https://www.researchgate.net/profile/YourProfile" ... > → Your ResearchGate
```

## About

This is my academic portfolio showcasing my research, publications, teaching experience, and more.

## Live Site

Visit: `https://your-username.github.io`

## Setup Instructions

### 1. Create the Repository
- On GitHub, create a **new public repository** named `your-username.github.io`
- Replace `your-username` with your actual GitHub username

### 2. Clone the Repository
```bash
git clone https://github.com/your-username/your-username.github.io.git
cd your-username.github.io
```

### 3. Add Your Files
- Place `index.html` in the root directory
- Create a `data/` folder with all JSON files
- Create a `publications/` folder
- Add your PDF files to the `publications/` folder
- Add `.gitignore` and `README.md` to the root

### 4. Update the Content
1. Edit `index.html` and replace:
   - `Your Name` with your actual name
   - `Your Title • Your Affiliation` with your real info
   - Social profile URLs (ORCID, LinkedIn, GitHub, Scholar, ResearchGate)

2. Edit each JSON file in the `data/` folder with your content

3. Add your PDF files to the `publications/` folder

4. Update file references in `publications.json` to match your PDF filenames

### 5. Commit and Push
```bash
git add .
git commit -m "Initial commit: Academic portfolio"
git push origin main
```

### 6. Enable GitHub Pages (if not automatic)
1. Go to your repository settings
2. Scroll to "GitHub Pages" section
3. Select `main` branch as the source
4. Your site will be live at `https://your-username.github.io`

## Adding New Items

**To add a new publication:**
1. Save your PDF to `publications/` folder
2. Add an entry to the correct section in `data/publications.json`
3. Make sure the `pdf_file` matches your filename exactly
4. Commit and push - it updates automatically!

**To add a new course:**
1. Add an entry to `data/teaching.json`
2. Commit and push

**To add press coverage:**
1. Add an entry to `data/press.json`
2. Commit and push

**Same process for research projects and miscellaneous items.**

## Customization

### Change Colors
Edit the CSS variables at the top of `index.html`:
```css
:root {
    --color-bg: #fafaf8;           /* Background color */
    --color-text: #1a1a18;         /* Text color */
    --color-accent: #2563eb;       /* Link and accent color */
    /* ... etc ... */
}
```

### Change Fonts
The site uses:
- **Crimson Text** for headings (serif, elegant)
- **Inter** for body text (sans-serif, clean)

You can change these in the `@import` line in the CSS section of `index.html`.

## Notes

- This is a **static HTML website** - no build process or server needed
- JSON files are loaded dynamically by JavaScript
- GitHub automatically publishes changes when you push to the repository
- The site works offline too (great for backups!)
- All changes are automatically deployed within seconds of pushing

## Troubleshooting

**Data not loading?**
- Make sure the `data/` folder exists in your repository root
- Check that JSON files are properly formatted (use a JSON validator)
- Make sure file names match exactly (case-sensitive on some systems)

**PDFs not downloading?**
- Verify the `pdf_file` names in `publications.json` match the actual file names in `publications/` folder
- Check that PDF files are actually in the `publications/` folder

## Support

For GitHub Pages documentation, visit: https://pages.github.com

