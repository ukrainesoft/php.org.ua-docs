---
navigation:
  - stream.constants.md: « Зумовлені константи
  - stream.contexts.md: Контексти потоків »
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Поточні фільтри
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Поточні фільтри

Фільтр (`filter`) - робочий код, який може здійснювати операції з даними, що читаються з потоку або записуються до нього. На кожен потік можна надбудувати декілька фільтрів. Фільтри користувача можна реєструвати в PHP-скрипті функцією [stream\_filter\_register()](function.stream-filter-register.md). Щоб переглянути список зареєстрованих на даний момент фільтрів, скористайтеся функцією [stream\_get\_filters()](function.stream-get-filters.md)
