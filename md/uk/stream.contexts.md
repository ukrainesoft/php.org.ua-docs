---
navigation:
  - stream.filters.md: « Поточні фільтри
  - stream.errors.md: Помилки потоку »
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Контексти потоків
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Контексти потоків

`Контекст` - це набір `параметрів`и зависящих от контекста`опцій`, який змінює або розширює поведінку потоку . `Контексти` створюються за допомогою функції [stream\_context\_create()](function.stream-context-create.md) і можуть бути передані більшості функцій файлової системи, пов'язаних із створенням потоків (наприклад, [fopen()](function.fopen.md) [file()](function.file.md) [file\_get\_contents()](function.file-get-contents.md), і т.д...).

`Опції` можуть бути визначені під час виклику функції [stream\_context\_create()](function.stream-context-create.md), чи пізніше, використовуючи функцію [stream\_context\_set\_option()](function.stream-context-set-option.md). Список можливих `опцій` у цьому контексті може бути знайдений у розділі [Контекстні опції та параметри](context.md)

`Параметри` можуть бути визначені для `контекстів`, используя функцию[stream\_context\_set\_params()](function.stream-context-set-params.md)
