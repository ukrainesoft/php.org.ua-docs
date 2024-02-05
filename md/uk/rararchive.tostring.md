---
navigation:
  - rararchive.setallowbroken.md: '« RarArchive::setAllowBroken'
  - class.rarentry.md: RarEntry »
  - index.md: PHP Manual
  - class.rararchive.md: RarArchive
title: 'RarArchive::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RarArchive::\_\_function toString() { \[native code\] }

(PECL rar >= 2.0.0)

RarArchive::\_\_toString — Отримати текстове уявлення

### Опис

```methodsynopsis
public RarArchive::__toString(): string
```

Повертає рядок, що представляє об'єкт [RarArchive](class.rararchive.md). Вона містить повний шлях до поточного відкритого тому архіву та інформацію про те, чи коректний ресурс чи вже закритий за допомогою [RarArchive::close()](rararchive.close.md)

Даний метод призначений тільки для налагодження, тому що немає жодної гарантії, з чого складатиметься відповідь і як він буде відформатований.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текстове подання об'єкта [RarArchive](class.rararchive.md). Контент не визначено.

### Приклади

**Пример #1 Пример использования**RarArchive::\_\_toString()\*\*\*\*

```php
<?php
$rar_arch = RarArchive::open('latest_winrar.rar');
echo $rar_arch."\n";
$rar_arch->close();
echo $rar_arch."\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar"
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar" (closed)
```
