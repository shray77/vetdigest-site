# 🐾 vetdigest-site

Публичная витрина дайджеста [VetDigest](https://github.com/shray77/vetdigest) на GitHub Pages.

**Открыть дашборд: [shray77.github.io/vetdigest-site](https://shray77.github.io/vetdigest-site/)**

## Что внутри

- `index.html` — дашборд: выпуски по датам, карточки статей с тремя тезисами, поиск, фильтры по источникам, счётчики. Код, стили и данные — локальные файлы. Единственная внешняя зависимость — веб-шрифты Google Fonts (Instrument Serif, Inter, IBM Plex Mono): подключены с `display=swap` и системными фолбэк-стеками, при недоступности CDN сайт полностью работоспособен и открывается из РФ. Кириллический дисплейный Prata самохостится в `fonts/`.
- `digest.json` — **перезаписывается автоматически воркером vetdigest** после сборки выпуска (крон 07:00 UTC = 10:00 МСК, или кнопка run-now в Actions приватной репы). Руками не редактировать.

## Откуда данные

```
PubMed (NCBI E-utilities)
  → rss-core: инжест, дедуп, D1          (приватная репа)
  → vetdigest: Workers AI → 3 тезиса     (приватная репа)
  → vetdigest-site: этот дашборд         (вы здесь)
```

Статус конвейера (здоровье источников, свежесть данных): [shray77.github.io/rss-core-site](https://shray77.github.io/rss-core-site/)
