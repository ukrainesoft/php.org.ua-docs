---
navigation:
  - resourcebundle.create.md: '« ResourceBundle::create'
  - resourcebundle.geterrormessage.md: 'ResourceBundle::getErrorMessage »'
  - index.md: PHP Manual
  - class.resourcebundle.md: ResourceBundle
title: 'ResourceBundle::getErrorCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ResourceBundle::getErrorCode

# resourcebundle\_get\_error\_code

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::getErrorCode -- resourcebundle\_get\_error\_code — Отримати останній код помилки пакета

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public ResourceBundle::getErrorCode(): int
```

Процедурний стиль

```methodsynopsis
resourcebundle_get_error_code(ResourceBundle $bundle): int
```

Повертає код останньої помилки, що виникла при виклику функцій пакета.

### Список параметрів

`bundle`

Об'єкт [ResourceBundle](class.resourcebundle.md)

### Значення, що повертаються

Повертає код останньої помилки, що виникла при виклику функцій пакета.

### Приклади

**Пример #1 Пример использования**resourcebundle\_get\_error\_code()\*\*\*\*

```php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(resourcebundle_get_error_code($r))) {
    report_error("Ошибка пакета");
}
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r['somestring'];
if(intl_is_failure(ResourceBundle::getErrorCode($r))) {
    report_error("Ошибка пакета");
}
?>
```

### Дивіться також

-   [resourcebundle\_get\_error\_message()](resourcebundle.geterrormessage.md) \- Отримати останнє повідомлення про помилку пакета
-   [intl\_get\_error\_code()](function.intl-get-error-code.md) \- Отримати код останньої помилки
-   [intl\_is\_failure()](function.intl-is-failure.md) \- Перевірити, чи є код помилки ознакою збою
