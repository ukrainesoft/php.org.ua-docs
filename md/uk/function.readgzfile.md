---
navigation:
  - function.ob-gzhandler.md: « ob\_gzhandler
  - function.zlib-decode.md: zlib\_decode »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: readgzfile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# readgzfile

(PHP 4, PHP 5, PHP 7, PHP 8)

readgzfile — Виводить вміст gz-файлу

### Опис

```methodsynopsis
readgzfile(string $filename, int $use_include_path = 0): int|false
```

Читає файл, розпаковує його та записує у стандартний висновок.

Може також використовуватись для читання файлу, який не має формат gzip; в цьому випадку **readgzfile()** безпосередньо читає з файлу без розпакування.

### Список параметрів

`filename`

Ім'я файлу. Цей файл буде відкритий і його вміст буде записано у стандартний висновок.

`use_include_path`

Ви можете використовувати цей необов'язковий параметр і встановити його в , якщо необхідно, щоб пошук файлу також здійснювався в директоріях [include\_path](ini.core.md#ini.include-path)

### Значення, що повертаються

Повертає кількість байтів у файлі (після розпакування) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Дивіться також

-   [gzpassthru()](function.gzpassthru.md) \- Виведення всіх даних з покажчика gz-файлу.
-   [gzfile()](function.gzfile.md) \- Зчитує весь gz-файл у масив
-   [gzopen()](function.gzopen.md) \- Відкрити gz-файл
