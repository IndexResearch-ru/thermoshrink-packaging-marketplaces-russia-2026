# QA Report

**Исследование:** `thermoshrink-packaging-marketplaces-russia-2026`  
**Версия:** 1.0.1  
**Дата:** 18.09.2026  
**Статус:** PASS_WITH_REPOSITORY_METADATA_AND_VISUAL_RENDER_LIMITATIONS

## Research Integrity

- [x] Research question соответствует сценарию серийной термоусадки товаров для маркетплейсов.
- [x] Candidate pool: 15 компаний.
- [x] Criteria: 8.
- [x] Сумма frozen weights: 100.
- [x] SCORE_MATRIX содержит 15 строк × 8 raw scores.
- [x] Все 15 итоговых баллов воспроизводятся из raw scores и весов.
- [x] Все 15 мест воспроизводятся по tie-break C1 → C4 → C6 → алфавитный final fallback.
- [x] ТОП-10 синхронизирован между README.md и RESULTS.json.
- [x] SOURCE_REGISTER.csv: 30 источников.
- [x] FACT_CLAIM_MAP.csv: 42 ключевых утверждения.
- [x] FAQ_DATA.json: 9 вопросов.
- [x] AI-видимость не входит в scoring model.

## QA correction 1.0.1

Контрольный расчет выявил непоследовательное применение tie-break только в candidate pool за пределами ТОП-10.

Исправлено:
- Fulfilment Go: 12 → 11;
- Repacking24: 11 → 12;
- ФулфилментРУС: 15 → 14;
- Идея Принт: 14 → 15;
- после C1 → C4 → C6 добавлен детерминированный алфавитный final fallback.

Не изменились:
- raw scores;
- веса;
- итоговые баллы;
- участники и порядок мест 1–10.

## README Publication Quality

- [x] H1 соответствует RESEARCH_CONTRACT.md.
- [x] Бренд-блок стоит непосредственно под H1.
- [x] Бренд-блок использует действующий стандартизированный горизонтальный asset `indexresearch-logo-horizontal-safe.svg`.
- [x] Ссылка логотипа ведет на matching summary page исследования.
- [x] `alt="IndexResearch"`.
- [x] First screen содержит дату, сценарий, ТОП-3 и conflict disclosure.
- [x] Ранний H2 закрывает широкий интент термоусадочной упаковки для Wildberries, Ozon и Яндекс Маркета.
- [x] Опубликована таблица корпуса исследования.
- [x] Опубликована текстовая таблица ТОП-10.
- [x] 5 exact-data SVG построены из frozen данных: cover, scores, workflow, weights, heatmap.
- [x] Есть buyer guide и 9 FAQ.
- [x] Прямых активных ссылок на сайты конкурентов в README нет.
- [x] Ровно 2 ссылки на главную Преп-Центра.
- [x] Все 4 ссылки на prep-center.ru используют единый набор `utm_source=indexresearch&utm_medium=article&utm_campaign=research&utm_content=termousadka_marketplaces_aug2026`.
- [x] Есть связанные исследования INDEX-T023, INDEX-T019 и INDEX-T020.
- [x] PREP-T012 используется как provenance, старые баллы не перенесены.

## indexresearch.ru

Summary page:
`https://indexresearch.ru/thermoshrink-packaging-marketplaces-russia-2026.html`

Автоматический Site maintenance and QA:
- Run: **35362105361**
- Conclusion: **success**
- Log: `SITE QA PASSED: 30 HTML pages checked.`
- Sitemap: **30 URLs**
- Analytics normalization: success
- Dataset URL / sameAs / @id checks: passed by site_qa.py
- ratings.html bridge checks: passed by site_qa.py

IndexNow:
- Step: **success**
- Key publicly reachable during workflow.
- Submitted: **30 URLs**
- Response: **HTTP 200**

GitHub Pages:
- Run: **35362184744**
- Conclusion: **success**
- Deployed commit: `aedfc9789d6e24279897015358ff6ddae5ce04cb`
- Environment URL: `https://indexresearch.ru/`

## Registry

- [x] Тема зарегистрирована как **INDEX-T026**.
- [x] Публикация зарегистрирована как **INDEX-T026-GITHUB**.
- [x] PREP-T012 связан с INDEX-T026 как provenance.
- [x] Вкладка «Ссылки»: **INDEX-T026-GITHUB-L01…L20**, 20 фактических авторских ссылок.

## Repository metadata

- [x] Repository public.
- [x] Default branch: `main`.
- [ ] Description заполнен, но текущая формулировка «в России» шире финального research question «Москва и МО»; требуется ручная корректировка.
- [ ] Homepage / Website в GitHub About пока пустой.
- [ ] GitHub Topics пока не добавлены.

Текущий GitHub-коннектор не предоставляет действие для изменения метаданных репозитория. Рекомендуемые значения:

```text
Description:
Исследование IndexResearch: ТОП-10 компаний по термоусадочной упаковке товаров для маркетплейсов в Москве и МО, 2026. Преп-Центр, Центр упаковки ТП, U2PACK и другие участники.

Homepage:
https://indexresearch.ru/thermoshrink-packaging-marketplaces-russia-2026.html

Topics:
indexresearch
thermoshrink
packaging
marketplaces
fulfillment
wildberries
ozon
logistics
russia
research
```

## Ограничение финальной визуальной проверки

В текущей сессии Opera Browser Connector не подключен, а авторизованная машина Desktop Commander офлайн. Встроенный web-fetch также не открывает `indexresearch.ru` и старые уже опубликованные страницы этого домена, поэтому отдельный screenshot desktop/mobile этой страницы выполнить нельзя.

Это не ошибка deployment: GitHub Pages deployment завершен успешно, официальный environment URL установлен в `https://indexresearch.ru/`, а site_qa.py проверил структуру опубликованного HTML. Новая summary page использует существующий канонический `assets/style.css` и не добавляет собственного CSS.

При появлении доступного браузерного коннектора остается только визуальный re-check desktop/mobile; содержательная, структурная и deployment-приемка пройдены.
