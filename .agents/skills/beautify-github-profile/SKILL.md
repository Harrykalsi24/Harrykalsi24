---
name: beautify-github-profile
description: >-
  Comprehensive guide, widgets, badge patterns, and design templates for building, styling, and beautifying GitHub Profile READMEs. Use this skill whenever creating, enhancing, or customizing GitHub profile README files, adding GitHub stats cards, streak counters, tech stack badges, typing SVGs, trophies, activity graphs, contribution snake animations, music/Spotify widgets, or designing profile layouts.
---

# Beautify GitHub Profile Skill

This skill provides patterns, snippets, and tools based on the curated [beautify-github-profile](https://github.com/rzashakeri/beautify-github-profile) repository by Reza Shakeri.

---

## 1. Core Profile Architecture

A balanced GitHub profile README balances aesthetics, personal branding, technical skills, and active metrics.

Recommended Section Order:
1. **Dynamic Header**: Animated banner or Capsule Render + Typing SVG tagline.
2. **Key Metric Badges**: Follower count, profile views, open-to-work status, star count.
3. **About Me**: Brief intro, current focus, collaborative interests, or code snippet card (TypeScript/JSON/Python format).
4. **Tech Stack & Skills**: Categorized skill icons (Languages, Frontend, Backend, Cloud, DevOps, Tools).
5. **Featured Projects**: Markdown table or card grid highlighting live demo, repository, and tech tags.
6. **Live GitHub Metrics**:
   - GitHub Readme Stats (Stats card + Top Languages)
   - Streak Stats
   - Profile Trophy or Activity Graph
7. **Interactive / Fun Widgets (Optional)**: Contribution Snake, Spotify Now Playing, Dev Quotes/Jokes, or Recent Blog Posts.
8. **Contact & Social Connect**: Badges or custom icons linking to LinkedIn, Twitter/X, Portfolio, Email.

---

## 2. Key Components & Code Snippets

### A. Dynamic Headers & Banners

#### Capsule Render
Customizable SVG dynamic headers:
```markdown
<img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=200&section=header&text=Your%20Name&fontSize=50&animation=fadeIn" width="100%"/>
```
*Types:* `wave`, `waving`, `slice`, `rect`, `soft`, `rounded`, `cylinder`.  
*Animations:* `twinkling`, `fadeIn`, `scaleIn`.

#### Readme Typing SVG
Generates animated typewriter text:
```markdown
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=0A66C2&center=true&vCenter=true&width=500&lines=Full+Stack+Developer;Cloud+%26+DevOps+Enthusiast;Open+Source+Contributor" alt="Typing SVG" />
</a>
```

---

### B. Tech Stack Icons & Badges

#### SkillIcons (Fast, Modern, Unified Design)
```markdown
<div align="center">
  <img src="https://skillicons.dev/icons?i=py,js,ts,react,tailwind,aws,docker,git,linux&theme=dark" alt="Tech Stack" />
</div>
```

#### Shields.io Custom Badges
```markdown
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white" />
```

---

### C. Live GitHub Stats Cards

#### GitHub Readme Stats
```markdown
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=nord" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=nord" alt="Top Languages" />
</p>
```
*Popular Themes:* `nord`, `tokyonight`, `dracula`, `onedark`, `radical`, `merko`, `gruvbox`.

#### GitHub Readme Streak Stats
```markdown
<img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=nord" alt="Streak Stats" />
```

#### GitHub Profile Trophy
```markdown
<img src="https://github-profile-trophy.vercel.app/?username=YOUR_USERNAME&theme=onedark&no-frame=false&no-bg=false&margin-w=4" alt="Trophies" />
```

#### GitHub Activity Graph
```markdown
<img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_USERNAME&theme=github-compact" alt="Activity Graph" />
```

#### Contribution Snake Animation (via GitHub Actions)
Generate an animated snake eating contribution squares:
Use action `Platane/snk@v3` outputting to `dist/github-contribution-grid-snake.svg`, and embed via:
```markdown
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-contribution-grid-snake.svg">
</picture>
```

---

### D. Profile Views & Metrics

```markdown
<!-- Anton Komarev Profile Views Counter -->
<img src="https://komarev.com/ghpvc/?username=YOUR_USERNAME&color=blue&style=for-the-badge&label=PROFILE+VIEWS" alt="Profile Views" />
```

---

### E. Spotify / Media Integration

#### Spotify Readme (Now Playing / Top Tracks)
```markdown
<a href="https://spotify-github-profile.kittinan.com/api/view?uid=YOUR_UID&cover_image=true&theme=default">
  <img src="https://spotify-github-profile.kittinan.com/api/view?uid=YOUR_UID&cover_image=true&theme=default" />
</a>
```

---

## 3. Best Practices & Guidelines

1. **Theme Consistency**: Match color schemes across all cards (`border_color`, `title_color`, `bg_color`, `text_color`, or unified presets like `nord` / `tokyonight` / `dark`).
2. **Mobile & Dark/Light Mode Adaptability**:
   - Use `<picture>` tags with `(prefers-color-scheme: dark)` and `(prefers-color-scheme: light)` for images that need light/dark variants.
   - Use percentage widths (e.g. `width="100%"`) or flexible `<div align="center">` wrappers so layout doesn't break on mobile screens.
3. **Table Grids for Projects**: Use markdown tables (`| Project | Description | Tech Stack | Links |`) or HTML `<table>` blocks to keep projects vertically aligned without ragged whitespace.
4. **Rate Limit Prevention**: Deploy personal Vercel instances for `github-readme-stats` if hitting API limits, or cache SVGs via GitHub Actions.

---

## References

- [Full Reference Guide & Index](./references/full-guide.md): Complete repository guide with 100+ badges, widgets, counters, and tools.
