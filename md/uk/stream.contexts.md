---
navigation:
  - stream.filters.html: « Поточні фільтри
  - stream.errors.html: Ошибки потока »
  - index.html: PHP Manual
  - book.stream.html: Потоки
title: Контексти потоків
---
# Контексти потоків

`Контекст` - це набір `параметров` та залежних від контексту `опций`, який змінює або розширює поведінку потоку . `Контексты` створюються за допомогою функції [streamcontextcreate()](function.stream-context-create.html) і можуть бути передані більшості функцій файлової системи, пов'язаних із створенням потоків (наприклад, [fopen()](function.fopen.html) [file()](function.file.html) [filegetcontents()](function.file-get-contents.html), і т.д...).

`Опции` можуть бути визначені під час виклику функції [streamcontextcreate()](function.stream-context-create.html), чи пізніше, використовуючи функцію [streamcontextsetoption()](function.stream-context-set-option.html). Список можливих `опций` у цьому контексті може бути знайдений у розділі [Контекстні опції та параметри](context.html)

`Параметры` можуть бути визначені для `контекстов`, використовуючи функцію [streamcontextsetparams()](function.stream-context-set-params.html)
