---
navigation:
  - function.inflate-get-status.md: « inflate\_get\_status
  - function.ob-gzhandler.md: ob\_gzhandler »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: inflate\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inflate\_init

(PHP 7, PHP 8)

inflate\_init - Ініціалізація контексту інкрементального розпакування

### Опис

```methodsynopsis
inflate_init(int $encoding, array $options = []): InflateContext|false
```

Ініціалізує контекст інкрементального розпакування із зазначеним кодуванням `encoding`

### Список параметрів

`encoding`

Одна из констант\*\*`ZLIB_ENCODING_*`\*\*

`options`

Асоціативний масив, який може містити такі елементи:

level

Рівень стиснення в діапазоні -1.9; за замовчуванням -1.

memory

Рівень пам'яті стиснення діапазоні 1..9; за замовчуванням 8.

window

Розмір вікна zlib (логарифмічний) у діапазоні 8..15; за промовчанням 15.

strategy

Одна из констант:**`ZLIB_FILTERED`** **`ZLIB_HUFFMAN_ONLY`** **`ZLIB_RLE`** **`ZLIB_FIXED`**или**`ZLIB_DEFAULT_STRATEGY`**(по умолчанию).

dictionary

Рядок (string) або масив (array) рядків поточного словника (за замовчуванням встановленого словника немає).

### Значення, що повертаються

Повертає ресурс контексту розпакування (`zlib.inflate`) или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо в `options` було передано некоректну опцію, або контекст не може бути створений, то буде викликана помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [InflateContext](class.inflatecontext.md); раніше повертався ресурс (resource). |

### Примітки

**Застереження**

В отличие от[gzinflate()](function.gzinflate.md)контексти інкрементального розширення не обмежують довжину декодованих даних, тому не забезпечують автоматичного захисту від ZIP-бомб.

### Дивіться також

-   [inflate\_add()](function.inflate-add.md) \- Інкрементальне розпакувати закодовані дані
-   [deflate\_init()](function.deflate-init.md) \- Ініціалізувати контекст інкрементального стиску
