---
navigation:
  - stream.constants.html: « Обумовлені константи
  - stream.contexts.html: Контексти потоків »
  - index.html: PHP Manual
  - book.stream.html: Потоки
title: Поточні фільтри
---
# Поточні фільтри

Фільтр (`filter`) - робочий код, який може здійснювати операції з даними, що читаються з потоку або записуються до нього. На кожен потік можна надбудувати декілька фільтрів. Фільтри користувача можна реєструвати в PHP-скрипті функцією [streamfilterregister()](function.stream-filter-register.html). Щоб переглянути список зареєстрованих на даний момент фільтрів, скористайтеся функцією [streamgetfilters()](function.stream-get-filters.html)
