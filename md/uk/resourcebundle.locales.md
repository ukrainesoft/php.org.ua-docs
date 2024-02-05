---
navigation:
  - resourcebundle.get.md: '« ResourceBundle::get'
  - class.spoofchecker.md: Spoofchecker »
  - index.md: PHP Manual
  - class.resourcebundle.md: ResourceBundle
title: 'ResourceBundle::getLocales'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ResourceBundle::getLocales

# resourcebundle\_locales

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::getLocales -- resourcebundle\_locales — Отримати підтримувані локалі

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static ResourceBundle::getLocales(string $bundle): array|false
```

Процедурний стиль

```methodsynopsis
resourcebundle_locales(string $bundle): array|false
```

Повертає доступні в ResourceBundle локалі.

### Список параметрів

`bundle`

Шлях до ResourceBundle або порожній рядок для отримання списку за замовчуванням або \*\*`false`\*\*в случае возникновения ошибки.

### Значення, що повертаються

Повертає доступні в ResourceBundle локалі.

### Приклади

**Пример #1 Пример использования**resourcebundle\_locales()\*\*\*\*

```php
<?php
$bundle = "/user/share/data/myapp";
echo join(PHP_EOL, resourcebundle_locales($bundle));
?>
```

Висновок наведеного прикладу буде схожим на:

```
es
root
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$bundle = "/usr/share/data/myapp";
$r = new ResourceBundle( 'es', $bundle);
echo join("\n", $r->getLocales($bundle));
?>
```

Висновок наведеного прикладу буде схожим на:

```
es
root
```

### Дивіться також

-   [resourcebundle\_get()](resourcebundle.get.md) \- Отримати дані з пакета
