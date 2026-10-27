# Git-процесс

- Ветка по умолчанию `main`. В неё попадаем через PR, не прямым push.
- Новые изменения — в отдельной ветке: `feat/…`, `fix/…`, `docs/…`, `chore/…`, `refactor/…`, `digest/…`.
- Коммиты атомарные: одно логическое изменение — один коммит.
- Сообщение: `тип: что сделано` по-русски (Conventional Commits: `feat`, `fix`, `docs`, `chore`, `refactor`). Пример: `feat: обзор Барселона — Реал`.
- Перед коммитом проверь сборку: `npm run build`.
- Запрещены `git push --force`, `git reset --hard`, `git commit --amend`.
- `gh` по умолчанию смотрит в upstream (репозиторий курса) — всегда указывай `--repo stanislavkatenev17-afk/ai-digest`.
