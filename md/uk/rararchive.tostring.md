Отримати текстове уявлення

-   [« RarArchive::setAllowBroken](rararchive.setallowbroken.html)
    
-   [RarEntry »](class.rarentry.html)
    
-   [PHP Manual](index.html)
    
-   [RarArchive](class.rararchive.html)
    
-   Отримати текстове уявлення
    

# RarArchive::function toString() { \[native code\] }

(PECL rar >= 2.0.0)

RarArchive::toString — Отримати текстове уявлення

### Опис

```methodsynopsis
public RarArchive::__toString(): string
```

Повертає рядок, що представляє об'єкт [RarArchive](class.rararchive.html). Вона містить повний шлях до поточного відкритого тому архіву та інформацію про те, чи коректний ресурс чи вже закритий за допомогою [RarArchive::close()](rararchive.close.html)

Даний метод призначений тільки для налагодження, тому що немає жодної гарантії, з чого складатиметься відповідь і як він буде відформатований.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Текстове подання об'єкта [RarArchive](class.rararchive.html). Контент не визначено.

### Приклади

**Приклад #1 Приклад використання **RarArchive::toString()****

```php
<?php
$rar_arch = RarArchive::open('latest_winrar.rar');
echo $rar_arch."\n";
$rar_arch->close();
echo $rar_arch."\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar"
RAR Archive "D:\php_rar\trunk\tests\latest_winrar.rar" (closed)
```