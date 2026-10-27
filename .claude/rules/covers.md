---
paths:
  - "public/covers/**"
  - ".claude/agents/cover-artist.md"
  - ".claude/skills/cover.md"
---

# Обложки

- Файл: `public/covers/<basename>.webp`, где `<basename>` совпадает с именем файла статьи без `.md`.
- Во frontmatter: `heroImage: /covers/<basename>.webp` — локальный путь, не удалённый URL.
- С ступени 5 картинка генерируется в Replicate и скачивается в `public/covers/` через `curl`: URL `replicate.delivery` живут около суток.
- До ступени 5 `heroImage` пустой (`""`) или отсутствует.

| Артефакт | Путь |
|---|---|
| Статья | `src/content/blog/2026-10-27-barcelona-real-madrid.md` |
| Обложка | `public/covers/2026-10-27-barcelona-real-madrid.webp` |
| Frontmatter | `heroImage: /covers/2026-10-27-barcelona-real-madrid.webp` |
