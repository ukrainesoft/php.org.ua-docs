---
navigation:
  - ref.zlib.md: « Функции Zlib
  - function.deflate-init.md: deflateinit »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: deflateadd
---
# deflateadd

(PHP 7, PHP 8)

deflateadd - Інкрементальний стиск даних

### Опис

```methodsynopsis
deflate_add(DeflateContext $context, string $data, int $flush_mode = ZLIB_SYNC_FLUSH): string|false
```

Інкрементальний стиск даних у зазначеному контексті.

### Список параметрів

`context`

Контекст, створений за допомогою функції [deflateinit()](function.deflate-init.md)

`data`

Блок даних стиснення.

`flush_mode`

Одна з констант: **`ZLIB_BLOCK`** **`ZLIB_NO_FLUSH`** **`ZLIB_PARTIAL_FLUSH`** **`ZLIB_SYNC_FLUSH`** (за замовчуванням), **`ZLIB_FULL_FLUSH`** **`ZLIB_FINISH`**. Зазвичай потрібно встановити **`ZLIB_NO_FLUSH`** для максимальної компресії та **`ZLIB_FINISH`** для завершення на останньому блоці даних. Детальний опис констант дивіться в [» руководстве zlib](http://www.zlib.net/manual.md)

### Значення, що повертаються

Повертає блок стиснутих даних або **`false`** у разі виникнення помилки.

### Помилки

У разі некоректних аргументів буде викликано помилку рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `context` чекає на екземпляр [DeflateContext](class.deflatecontext.md); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [deflateinit()](function.deflate-init.md) - Ініціалізувати контекст інкрементального стиску
