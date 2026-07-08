# respiral-docs

Дизайн-документация контент-пака **Respiral** для Space Station 14.
Статический сайт на [mdBook](https://rust-lang.github.io/mdBook/), публикуется на GitHub Pages.

Игровой репозиторий: [ss14-respiral](https://github.com/NoxLiquid/ss14-respiral) *(поправьте ссылку при необходимости)*.

## Локальная сборка

```shell
cargo install mdbook mdbook-mermaid   # один раз
mdbook-mermaid install .              # один раз: ассеты для диаграмм
mdbook serve --open                   # локальный предпросмотр на http://localhost:3000
```

`mdbook build` кладёт готовый сайт в `book/` (в `.gitignore`).

## Публикация

Push в `main` запускает workflow `.github/workflows/deploy.yml`, который собирает
книгу и деплоит её на GitHub Pages.

> **Разовая настройка на GitHub:** *Settings → Pages → Build and deployment → Source = GitHub Actions.*

## Структура

- `src/SUMMARY.md` — оглавление (сайдбар строится строго по нему).
- `src/professions/` — обзор профессий и план диздока.
- `src/departments/` — страницы департаментов по шаблону.
