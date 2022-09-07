---
navigation:
  - function.gzwrite.md: « gzwrite
  - function.inflate-get-read-len.md: inflategetreadlen »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: inflateadd
---
# inflateadd

(PHP 7, PHP 8)

inflateadd — Інкрементальне розпакування закодованих даних

### Опис

```methodsynopsis
inflate_add(InflateContext $context, string $data, int $flush_mode = ZLIB_SYNC_FLUSH): string|false
```

Інкрементальне розпаковує закодовані дані у зазначеному контексті `context`

Обмеження: інформація заголовка зі стислих даних GZIP недоступна.

### Список параметрів

`context`

Контекст, створений за допомогою [inflateinit()](function.inflate-init.md)

`data`

Блок стислих даних.

`flush_mode`

Одна з констант: **`ZLIB_BLOCK`** **`ZLIB_NO_FLUSH`** **`ZLIB_PARTIAL_FLUSH`** **`ZLIB_SYNC_FLUSH`** (за замовчуванням), **`ZLIB_FULL_FLUSH`** **`ZLIB_FINISH`**. Зазвичай потрібно встановити **`ZLIB_NO_FLUSH`** для максимальної компресії та **`ZLIB_FINISH`** завершення роботи з останнім блоком даних. Детальний опис констант дивіться в [» руководство zlib](http://www.zlib.net/manual.md)

### Значення, що повертаються

Повертає блок розпакованих даних або **`false`** у разі виникнення помилки.

### Помилки

Якщо передано некоректні параметри, розпакування вимагає наявність словника, але він не заданий, потік стислих даних зіпсований або має некоректну контрольну суму, то генерується помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `context` чекає на екземпляр [InflateContext](class.inflatecontext.md); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [inflateinit()](function.inflate-init.md) - Ініціалізація контексту інкрементального розпакування
