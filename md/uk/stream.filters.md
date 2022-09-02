---
navigation:
  - stream.constants.md: « Обумовлені константи
  - stream.contexts.md: Контексти потоків »
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Поточні фільтри
---
# Поточні фільтри

Фільтр (`filter`) - робочий код, який може здійснювати операції з даними, що читаються з потоку або записуються до нього. На кожен потік можна надбудувати декілька фільтрів. Фільтри користувача можна реєструвати в PHP-скрипті функцією [streamfilterregister()](function.stream-filter-register.md). Щоб переглянути список зареєстрованих на даний момент фільтрів, скористайтеся функцією [streamgetfilters()](function.stream-get-filters.md)
