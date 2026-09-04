# Svitlana Domashenko — Portfolio Website

Особистий сайт-портфоліо для Junior Data Analyst позиції. Односторінковий сайт, що зібрано з CV, GitHub та Tableau Public профілю — з описом навичок,  портфоліо-проєктів та шляху навчання.

**Live site:** [https://svdom.github.io/data-analyst-portfolio/](https://svdom.github.io/data-analyst-portfolio/) *(після публікації через GitHub Pages)*

## Overview

Сайт зібраний в один самодостатній `index.html` — без збірки, без залежностей від npm чи фреймворків. Фото власника вбудоване напряму в HTML (base64), тому файл можна публікувати на GitHub Pages без жодних додаткових ассетів.

## Sections

- **Hero** — ім'я, роль, фото, короткий pitch, CTA (LinkedIn, GitHub, Contact)
- **About Me** — позиціонування кандидата на основі портфоліо
- **Skills** — навички за категоріями: Data Analysis, SQL & Databases, Python, BI & Visualization, Tools, Business Focus
- **Portfolio Projects** — 6 проєктів з описом, інструментами, результатами й посиланнями (GitHub, Google Drive, Tableau Public)
- **Experience** — чесний виклад шляху без комерційного досвіду: від курсів до готових проєктів
- **Education & Courses** — 3 курси DATAbi
- **Contact** — Email, LinkedIn, GitHub, Tableau Public

## Tech Stack

- HTML5, CSS3 (custom properties, без фреймворків), vanilla JavaScript
- Google Fonts: Inter, Space Grotesk, JetBrains Mono
- Inline SVG-іконки (без сторонніх іконкових бібліотек)
- `IntersectionObserver` для fade-in анімацій секцій
- `localStorage` для збереження вибраної теми (light/dark)

## Design

- Світла тема за замовчуванням (`#fafafa`), перемикач на темну
- Акцентний колір `#1F4E5F` — узгоджений з кольором заголовків у CV для візуальної єдності
- Mobile-first, брейкпоінти на 700px і 820px
- WCAG AA контраст (≥4.5) перевірено для всіх комбінацій тексту й акцентного кольору

## Project Structure

```
data-analyst-portfolio/
├── index.html   ← весь сайт: HTML + CSS (<style>) + JS (<script>) в одному файлі
└── README.md
```

## Local Preview

Файл не потребує сервера — достатньо відкрити `index.html` напряму в браузері, або:

```bash
python3 -m http.server 8000
```

і перейти на `http://localhost:8000`.

## How to Update Content

Весь контент — в HTML-розмітці, секціями:
- Проєкти: блоки `<div class="project">` в секції `#projects`
- Навички: списки `<ul class="skill-list">` в секції `#skills`
- Контакти й посилання: пошук за `mailto:`, `github.com`, `linkedin.com`, `tableau.com`

Фото зберігається як `data:image/jpeg;base64,...` рядок у `<img src="...">` — для заміни потрібно перегенерувати base64 нового фото і вставити замість поточного.

## Deployment (GitHub Pages)

1. Створити репозиторій `data-analyst-portfolio`
2. Завантажити `index.html` у корінь репозиторію
3. Settings → Pages → Source → Deploy from branch `main` → `/root`
4. Перевірити, що всі посилання на проєкти відкриваються після публікації

