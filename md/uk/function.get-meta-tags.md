---
navigation:
  - function.get-headers.md: « get\_headers
  - function.http-build-query.md: http\_build\_query »
  - index.md: PHP Manual
  - ref.url.md: Функції URL
title: get\_meta\_tags
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_meta\_tags

(PHP 4, PHP 5, PHP 7, PHP 8)

get\_meta\_tags — Витягує вміст усіх метатегів із файлу та повертає масив

### Опис

```methodsynopsis
get_meta_tags(string $filename, bool $use_include_path = false): array|false
```

Відкриває `filename` і розбирає його рядками у пошуках тегів . Розбір файлу зупиняється на тезі `</head>`

### Список параметрів

`filename`

Шлях до HTML-файлу у вигляді рядка. Можливо як локальним файлом, і URL.

**Приклад #1 Що обробляє функція **get\_meta\_tags()****

`use_include_path`

Якщо `use_include_path`равен\*\*`true`\*\*, PHP буде шукати файл, використовуючи стандартні шляхи пошуку з директиви php.ini [include\_path](ini.core.md#ini.include-path). Це актуально лише для локальних файлів, але не URL.

### Значення, що повертаються

Повертає асоціативний масив із значеннями розібраних метатегів.

Значення атрибута name стає ключем масиву, а значення атрибута content – ​​значенням цього елемента. Ви можете використовувати стандартні функції роботи з масивами для обходу чи доступу до конкретних значень. Спеціальні символи в іменах (ключах масиву) замінюються на '\_', і ключі наводяться до нижнього регістру. Якщо два метатеги мають однакові імена, буде повернено лише останній.

Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #2 Що функція повертає **get\_meta\_tags()****

```php
<?php
// Предположим, что указанные выше метатеги расположены на www.example.com
$tags = get_meta_tags('http://www.example.com/');

// Обратите внимание, что ключи приведены к нижнему регистру,
// а точки ('.') в ключах заменены на '_'
echo $tags['author'];       // name
echo $tags['keywords'];     // php documentation
echo $tags['description'];  // a php manual
echo $tags['geo_position']; // 49.33;-86.59
?>
```

### Примітки

> **Зауваження** :
> 
> Обробляються лише метатеги із атрибутом name. Лапки не потрібні.

### Дивіться також

-   [htmlentities()](function.mdentities.md) \- Перетворює всі можливі символи у відповідні HTML-сутності
-   [urlencode()](function.urlencode.md) \- URL-кодування рядка
