---
navigation:
  - class.resourcebundle.md: « ResourceBundle
  - resourcebundle.create.md: 'ResourceBundle::create »'
  - index.md: PHP Manual
  - class.resourcebundle.md: ResourceBundle
title: 'ResourceBundle::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ResourceBundle::count

# resourcebundle\_count

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::count -- resourcebundle\_count — Отримати кількість елементів у пакеті

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

**Пример #1 Пример использования**resourcebundle\_count()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
42
```

### Дивіться також

-   [resourcebundle\_get()](resourcebundle.get.md) \- Отримати дані з пакета
