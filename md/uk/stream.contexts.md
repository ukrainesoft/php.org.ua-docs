---
navigation:
  - stream.filters.md: « Поточні фільтри
  - stream.errors.md: Ошибки потока »
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Контексти потоків
---
# Контексти потоків

`Контекст` - це набір `параметров` та залежних від контексту `опций`, який змінює або розширює поведінку потоку . `Контексты` створюються за допомогою функції [streamcontextcreate()](function.stream-context-create.md) і можуть бути передані більшості функцій файлової системи, пов'язаних із створенням потоків (наприклад, [fopen()](function.fopen.md) [file()](function.file.md) [filegetcontents()](function.file-get-contents.md), і т.д...).

`Опции` можуть бути визначені під час виклику функції [streamcontextcreate()](function.stream-context-create.md), чи пізніше, використовуючи функцію [streamcontextsetoption()](function.stream-context-set-option.md). Список можливих `опций` у цьому контексті може бути знайдений у розділі [Контекстні опції та параметри](context.md)

`Параметры` можуть бути визначені для `контекстов`, використовуючи функцію [streamcontextsetparams()](function.stream-context-set-params.md)
