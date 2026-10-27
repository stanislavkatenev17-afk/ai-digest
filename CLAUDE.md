# CLAUDE.md

Личный футбольный блог-дайджест на Astro + Vercel (проект курса Claude Code Basics). Единственный читатель — автор. Цель — быстро узнавать главное без эмоций комментаторов.

## Команды

- `npm run dev` — локальный сервер на `:4321`.
- `npm run build` — production-сборка. Запускай перед каждым коммитом.

## Архитектура

- Статьи: `src/content/blog/*.md`, схема — `src/content.config.ts`.
- Обложки: `public/covers/`.
- Выпуск собирается вручную командой `/digest`: news-scout → writer → cover-artist → page-builder (`.claude/skills/`, `.claude/agents/`). Tavily и Replicate — ступень 5, расписание — ступень 8.
- Vercel разворачивает сайт после push в `main`.

## Правила по темам

- Before writing or editing articles, read `.claude/rules/article-style.md`.
- Before choosing news for an issue, read `.claude/rules/news-selection.md`.
- Before working with covers, read `.claude/rules/covers.md`.
- Git-правила — `.claude/rules/git-workflow.md` (без `paths:`, загружается всегда).

## Compact Instructions

При сжатии контекста обязательно сохрани:
- Написанные и изменённые статьи (заголовок + файл).
- Текущую задачу и её статус.
- Решения, принятые в сессии, и найденные ошибки.
- Текущую ветку и номер открытого PR.

Формат резюме: «Написано: … В процессе: … Решения: …».
