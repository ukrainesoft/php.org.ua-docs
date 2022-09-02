---
navigation:
  - resourcebundle.count.md: '« ResourceBundle::count'
  - resourcebundle.geterrorcode.md: 'ResourceBundle::getErrorCode »'
  - index.md: PHP Manual
  - class.resourcebundle.md: ResourceBundle
title: 'ResourceBundle::create'
---
# ResourceBundle::create

# resourcebundlecreate

# ResourceBundle::construct

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::create -- resourcebundlecreate -- ResourceBundle::construct — Створити пакет ресурсів

### Опис

Об'єктно-орієнтований стиль (метод)

```methodsynopsis
public static ResourceBundle::create(?string $locale, ?string $bundle, bool $fallback = true): ?ResourceBundle
```

Процедурний стиль

```methodsynopsis
resourcebundle_create(?string $locale, ?string $bundle, bool $fallback = true): ?ResourceBundle
```

Об'єктно-орієнтований стиль (конструктор):

public **ResourceBundle::construct**(?string `$locale`, ?string `$bundle`, bool `$fallback` **`true`**

Створює пакет ресурсів.

### Список параметрів

`locale`

Локаль для якої необхідно завантажувати ресурси (ім'я локалі, наприкладRU).

`bundle`

Директорія, у якій лежать дані, чи ім'я .dat файла.

`fallback`

Визначає, чи потрібно точно дотримуватись заданої локалі, чи можна відкочуватися до батьківської, якщо можливо.

### Значення, що повертаються

Повертає об'єкт [ResourceBundle](class.resourcebundle.md) або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **resourcebundlecreate()****

```php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['teststring'];
?>
```

**Приклад #2 Приклад використання **ResourceBundle::create()****

```php
<?php
$r = ResourceBundle::create( 'es', "/usr/share/data/myapp");
echo $r['teststring'];
?>
```

Результат виконання цього прикладу:

```
¡Hola, mundo!
```

### Дивіться також

-   [resourcebundleget()](resourcebundle.get.md) - Отримати дані з пакета
