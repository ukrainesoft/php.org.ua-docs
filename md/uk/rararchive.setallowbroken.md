---
navigation:
  - rararchive.open.md: '« RarArchive::open'
  - rararchive.tostring.md: 'RarArchive::toString »'
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::setAllowBroken'
---
# RarArchive::setAllowBroken

(PECL rar >= 3.0.0)

RarArchive::setAllowBroken — Чи відкривати пошкоджені архіви

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public RarArchive::setAllowBroken(bool $allow_broken): bool
```

Процедурний стиль:

```methodsynopsis
rar_allow_broken_set(RarArchive $rarfile, bool $allow_broken): bool
```

Метод визначає, чи можна намагатись читати пошкоджений архів, чи всі операції з ним мають закінчуватися помилкою. Пошкоджені архіви - це такі архіви, які відкриваються без помилок, але при спробі прочитати записи виникають помилки.

### Список параметрів

`rarfile`

Об'єкт [RarArchive](class.rararchive.md), відкритий за допомогою [raropen()](rararchive.open.md)

`allow_broken`

Чи дозволили роботу з пошкодженими архівами (**`true`**) чи ні (**`false`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Помилка може виникнути, якщо файл вже закритий.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* третий аргумент подавляет сообщение "volume not found" */
$a = RarArchive::open($file, null, 'retnull');
$a->setAllowBroken(true);
foreach ($a->getEntries() as $e) {
    echo "$e\n";
}
var_dump(count($a));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
RarEntry for file "file1.txt" (52b28202)
int(1)
```

**Приклад #2 Процедурний стиль**

```php
<?php
function retnull() { return null; }
$file = dirname(__FILE__) . "/multi_broken.part1.rar";
/* третий аргумент подавляет сообщение "volume not found" */
$a = rar_open($file, null, 'retnull');
rar_allow_broken_set($a, true);
foreach (rar_list($a) as $e) {
    echo "$e\n";
}
var_dump(count($a));
?>
```

### Дивіться також

-   [RarArchive::isBroken()](rararchive.isbroken.md) - Перевіряє, чи не зламано архів (не завершено)
