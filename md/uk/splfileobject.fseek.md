---
navigation:
  - splfileobject.fscanf.md: '« SplFileObject::fscanf'
  - splfileobject.fstat.md: 'SplFileObject::fstat »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::fseek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::fseek

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::fseek - Переклад файлового покажчика на задану позицію

### Опис

```methodsynopsis
public SplFileObject::fseek(int $offset, int $whence = SEEK_SET): int
```

Переміщує файловий покажчик на вказане у параметрі `offset` кількість байт. За позицію, від якої відраховуватиметься зсув, відповідає параметр `whence`

### Список параметрів

`offset`

Смещение. Отрицательная величина смещения используется, когда нужно перемещаться по файлу от конца к началу, т.е. когда в качестве аргумента`whence`передано значение SEEK\_END.

`whence`

Можливі значення параметра `whence` :

-   \*\*`SEEK_SET`\*\*- встановити покажчик на позицію`offset`байт от начала файла.
-   \*\*`SEEK_CUR`\*\*- Перемістити покажчик на`offset`байт щодо поточного становища.
-   \*\*`SEEK_END`\*\*- встановити покажчик на позицію`offset`байт від кінця файлу.

Якщо параметр `whence` опущений, функція працюватиме в режимі **`SEEK_SET`**

### Значення, що повертаються

Повертає 0, якщо переміщення пройшло успішно, і -1 інакше. Слід пам'ятати, що переміщення за кінець файлу не сприймається як помилка.

### Приклади

**Пример #1 Пример использования**SplFileObject::fseek()\*\*\*\*

```php
<?php
$file = new SplFileObject("somefile.txt");

// Чтение первой строки
$data = $file->fgets();

// Перемещаемся снова в начало файла
// То же, что и $file->rewind();
$file->fseek(0);
?>
```

### Дивіться також

-   [fseek()](function.fseek.md) \- Встановлює зміщення у файловому покажчику
