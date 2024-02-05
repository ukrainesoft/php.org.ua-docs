---
navigation:
  - function.gzwrite.md: « gzwrite
  - function.inflate-get-read-len.md: inflate\_get\_read\_len »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: inflate\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inflate\_add

(PHP 7, PHP 8)

inflate\_add — Інкрементальне розпакування закодованих даних

### Опис

```methodsynopsis
inflate_add(InflateContext $context, string $data, int $flush_mode = ZLIB_SYNC_FLUSH): string|false
```

Інкрементальне розпаковує закодовані дані у зазначеному контексті `context`

Обмеження: інформація заголовка зі стислих даних GZIP недоступна.

### Список параметрів

`context`

Контекст, створений за допомогою [inflate\_init()](function.inflate-init.md)

`data`

Блок стислих даних.

`flush_mode`

Одна из констант:**`ZLIB_BLOCK`** **`ZLIB_NO_FLUSH`** **`ZLIB_PARTIAL_FLUSH`** **`ZLIB_SYNC_FLUSH`**(по умолчанию),**`ZLIB_FULL_FLUSH`** **`ZLIB_FINISH`**. Зазвичай потрібно встановити **`ZLIB_NO_FLUSH`** для максимальної компресії та **`ZLIB_FINISH`** завершення роботи з останнім блоком даних. Детальний опис констант дивіться в [» керівництво zlib](http://www.zlib.net/manual.md)

### Значення, що повертаються

Повертає блок розпакованих даних або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо передано некоректні параметри, розпакування вимагає наявність словника, але він не заданий, потік стислих даних зіпсований або має некоректну контрольну суму, то генерується помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `context` чекає на екземпляр [InflateContext](class.inflatecontext.md); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [inflate\_init()](function.inflate-init.md) \- Ініціалізація контексту інкрементального розпакування
