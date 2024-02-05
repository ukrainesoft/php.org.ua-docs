---
navigation:
  - splfileobject.ftruncate.md: '« SplFileObject::ftruncate'
  - splfileobject.getchildren.md: 'SplFileObject::getChildren »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fwrite'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fwrite

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::fwrite — Запис до файлу

### Опис

```methodsynopsis
public SplFileObject::fwrite(string $data, int $length = 0): int|false
```

Записує вміст рядка `string` у файл.

### Список параметрів

`data`

Рядок, який буде записаний у файл.

`length`

Если задан аргумент`length`, запис зупиниться після того, як `length` байт будуть записані або буде досягнуто кінець рядка `string`, Залежно від того, що трапиться раніше.

### Значення, що повертаються

Повертає кількість записаних байт або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Функція тепер повертає **`false`** замість нуля у разі виникнення помилки. |

### Приклади

**Приклад #1 Приклад використання** SplFileObject::fwrite()\*\*\*\*

```php
<?php
$file = new SplFileObject("fwrite.txt", "w");
$written = $file->fwrite("12345");
echo "В файл записано $written байт";
?>
```

Висновок наведеного прикладу буде схожим на:

```
В файл записано 5 байт
```

### Дивіться також

-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
