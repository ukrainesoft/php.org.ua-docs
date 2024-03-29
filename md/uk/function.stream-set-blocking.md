---
navigation:
  - function.stream-select.md: « stream\_select
  - function.stream-set-chunk-size.md: stream\_set\_chunk\_size »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_set\_blocking
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_set\_blocking

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_set\_blocking — Встановити блокуючий/неблокуючий режим у потоці

### Опис

```methodsynopsis
stream_set_blocking(resource $stream, bool $enable): bool
```

Встановлює блокуючий або неблокуючий режим у потоці `stream`

Ця функція працює для будь-якого потоку, який підтримує неблокуючий режим (нині це звичайні файли та сокетні потоки).

### Список параметрів

`stream`

Потік.

`enable`

Якщо параметр `enable`равен\*\*`false`\*\*, вказаний потік буде переключено в неблокуючий режим, а якщо він дорівнює **`true`**, потік буде переключено в блокуючий режим. Це впливає на такі виклики, як [fgets()](function.fgets.md) і [fread()](function.fread.md), які читають із потоку. У неблокувальному режимі виклик функції [fgets()](function.fgets.md) завжди буде повертатися відразу, тоді як в блокувальному режимі він буде очікувати, поки дані стануть доступні на потоці.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Примітки

> **Зауваження** :
> 
> У Windows ця функція не впливає на локальні файли. Неблокуючий IO для локальних файлів не підтримується у Windows.

### Дивіться також

-   [stream\_select()](function.stream-select.md) \- Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
