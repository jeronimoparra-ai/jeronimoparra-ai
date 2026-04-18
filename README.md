<h1 align="center">Hi 👋, I'm Andres Jeronimo Parra Bastidas</h1>
<h3 align="center">Software Development Student | Autodidact | BeeStation</h3>

<p align="center">
  I am a second-semester student in a Software Development Technology program.
  I am currently learning programming from scratch in a self-taught way, building small projects,
  improving my technical skills, and growing step by step in web development and software creation.
</p>

---

## About Me

- 🎓 Second-semester student in Software Development Technology
- 📚 Self-taught learner, still building my programming foundations
- 🐝 Working on **BeeStation**, an IoT apiculture project
- 💡 Interested in web development, design, and technology
- 🚀 Focused on learning by doing and improving with each project

---

## What I'm Working On

- Basic programming concepts
- HTML, CSS, and JavaScript
- Responsive web design
- Git and GitHub
- Project documentation
- BeeStation: IoT project for apiary monitoring

---
name: Update README cards

on:
  schedule:
    - cron: "0 3 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Generate stats card
        uses: readme-tools/github-readme-stats-action@v1
        with:
          card: stats
          options: username=${{ github.repository_owner }}&show_icons=true
          path: profile/stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Commit cards
        run: |
          git config user.name "github-actions"
          git config user.email "github-actions@users.noreply.github.com"
          git add profile/*.svg
          git commit -m "Update README cards" || exit 0
          git push

## Current Goal

My goal is to keep learning consistently, strengthen my programming fundamentals,
and build useful projects that show my progress as a developer.

---

## Contact

- GitHub: @jeronimoparra-ai
