---
navigation:
  - ref.zlib.md: « Функції Zlib
  - function.deflate-init.md: deflate\_init »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: deflate\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# deflate\_add

(PHP 7, PHP 8)

deflate\_add - Інкрементальний стиск даних

### Опис

```methodsynopsis
deflate_add(DeflateContext $context, string $data, int $flush_mode = ZLIB_SYNC_FLUSH): string|false
```

Інкрементальний стиск даних у зазначеному контексті.

### Список параметрів

`context`

Контекст, створений за допомогою функції [deflate\_init()](function.deflate-init.md)

`data`

Блок даних стиснення.

`flush_mode`

Одна из констант:**`ZLIB_BLOCK`** **`ZLIB_NO_FLUSH`** **`ZLIB_PARTIAL_FLUSH`** **`ZLIB_SYNC_FLUSH`**(по умолчанию),**`ZLIB_FULL_FLUSH`** **`ZLIB_FINISH`**. Зазвичай потрібно встановити **`ZLIB_NO_FLUSH`** для максимальної компресії та **`ZLIB_FINISH`** для завершення на останньому блоці даних. Детальний опис констант дивіться в [» керівництві zlib](http://www.zlib.net/manual.md)

### Значення, що повертаються

Повертає блок стиснутих даних або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі некоректних аргументів буде викликано помилку рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` чекає на екземпляр [DeflateContext](class.deflatecontext.md); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [deflate\_init()](function.deflate-init.md) \- Ініціалізувати контекст інкрементального стиску
