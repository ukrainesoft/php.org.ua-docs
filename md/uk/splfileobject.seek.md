---
navigation:
  - splfileobject.rewind.md: '« SplFileObject::rewind'
  - splfileobject.setcsvcontrol.md: 'SplFileObject::setCsvControl »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::seek

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::seek - Переклад файлового покажчика на заданий рядок

### Опис

```methodsynopsis
public SplFileObject::seek(int $line): void
```

Переводить файловий покажчик на заданий рядок.

### Список параметрів

`line`

Номер рядка, починаючи з 0, який потрібно перейти.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [LogicException](class.logicexception.md), якщо аргумент `line` набуває негативного значення.

### Приклади

**Пример #1 Пример использования**SplFileObject::seek()\*\*\*\*

Цей приклад виводить третій рядок скрипта, що знаходиться на 2-й позиції.

```php
<?php
$file = new SplFileObject(__FILE__);
$file->seek(2);
echo $file->current();
?>
```

Висновок наведеного прикладу буде схожим на:

```
$file->seek(2);
```

### Дивіться також

-   [SplFileObject::current()](splfileobject.current.md) \- Отримати поточний рядок файлу
-   [SplFileObject::key()](splfileobject.key.md) \- Отримати номер рядка
-   [SplFileObject::next()](splfileobject.next.md) \- Читати наступний рядок
-   [SplFileObject::rewind()](splfileobject.rewind.md) \- Перемотування файлового покажчика на початок файлу
-   [SplFileObject::valid()](splfileobject.valid.md) \- Перевіряє, чи кінець файлу (EOF) досягнуто.
