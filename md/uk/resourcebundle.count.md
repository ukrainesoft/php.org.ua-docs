---
navigation:
  - class.resourcebundle.md: « ResourceBundle
  - resourcebundle.create.md: 'ResourceBundle::create »'
  - index.md: PHP Manual
  - class.resourcebundle.md: ResourceBundle
title: 'ResourceBundle::count'
---
# ResourceBundle::count

# resourcebundlecount

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::count -- resourcebundlecount — Отримати кількість елементів у пакеті

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public ResourceBundle::count(): int
```

Процедурний стиль

```methodsynopsis
resourcebundle_count(ResourceBundle $bundle): int
```

Отримує кількість елементів у пакеті.

### Список параметрів

`bundle`

Об'єкт [ResourceBundle](class.resourcebundle.md)

### Значення, що повертаються

Повертає кількість елементів у пакеті.

### Приклади

**Приклад #1 Приклад використання **resourcebundlecount()****

```php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo resourcebundle_count($r);
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r->count();
?>
```

Результат виконання цього прикладу:

```
42
```

### Дивіться також

-   [resourcebundleget()](resourcebundle.get.md) - Отримати дані з пакета
