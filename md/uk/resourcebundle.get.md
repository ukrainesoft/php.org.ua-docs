---
navigation:
  - resourcebundle.geterrormessage.md: '« ResourceBundle::getErrorMessage'
  - resourcebundle.locales.md: 'ResourceBundle::getLocales »'
  - index.md: PHP Manual
  - class.resourcebundle.md: ResourceBundle
title: 'ResourceBundle::get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ResourceBundle::get

# resourcebundle\_get

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL intl >= 2.0.0)

ResourceBundle::get -- resourcebundle\_get — Отримати дані з пакета

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public ResourceBundle::get(string|int $index, bool $fallback = true): mixed
```

Процедурний стиль

```methodsynopsis
resourcebundle_get(ResourceBundle $bundle, string|int $index, bool $fallback = true): mixed
```

Повертає дані з пакета за індексом або рядковим ключем.

### Список параметрів

`bundle`

Об'єкт [ResourceBundle](class.resourcebundle.md)

`index`

Індекс даних повинен бути рядком або цілим числом.

`fallback`

Чи повинна локаль збігатися точно, чи можна відкотитися до батьківської локалі.

### Значення, що повертаються

Повертає дані з пакета за індексом або рядковим ключем або **`null`** у разі виникнення помилки. Рядки, цілі числа та бінарні рядки повертаються у відповідному типі PHP, масиви цілих чисел повертаються як масиви PHP. Складні типи повертаються як об'єкти [ResourceBundle](class.resourcebundle.md)

### Приклади

**Пример #1 Пример использования**resourcebundle\_get()\*\*\*\*

```php
<?php
$r = resourcebundle_create( 'es', "/usr/share/data/myapp");
echo resourcebundle_get($r, 'somestring');
?>
```

**Приклад #2 Приклад в об'єктно-орієнтованому стилі**

```php
<?php
$r = new ResourceBundle( 'es', "/usr/share/data/myapp");
echo $r->get('somestring');
?>
```

Результат виконання наведеного прикладу:

```
?Hola, mundo!
```

### Дивіться також

-   [resourcebundle\_count()](resourcebundle.count.md) \- Отримати кількість елементів у пакеті
