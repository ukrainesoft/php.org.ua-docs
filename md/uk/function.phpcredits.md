---
navigation:
  - function.php-uname.md: « php\_uname
  - function.phpinfo.md: phpinfo »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: phpcredits
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpcredits

(PHP 4, PHP 5, PHP 7, PHP 8)

phpcredits - Виводить список розробників PHP

### Опис

```methodsynopsis
phpcredits(int $flags = CREDITS_ALL): true
```

Ця функція виводить список розробників PHP, модулів тощо. Вона створює відповідний HTML-код для вставки на сторінку.

### Список параметрів

`flags`

Использование аргумента`flags` дозволяє довільно компонувати інформацію про окремі групи розробників.

**Обумовлені прапори **phpcredits()****

| Имя | Опис |
| --- | --- |
| CREDITS\_ALL | Усі розробники, еквівалентно використанню: **`CREDITS_DOCS`** **`CREDITS_GENERAL`** **`CREDITS_GROUP`** **`CREDITS_MODULES`** **`CREDITS_FULLPAGE`**. . У цьому випадку буде згенеровано повністю незалежну HTML-сторінку з відповідними тегами. |
| CREDITS\_DOCS | Учасники команди документування |
| CREDITS\_FULLPAGE | Зазвичай використовується у комбінації з іншими прапорами. Вказує на те, що незалежна HTML-сторінка повинна містити інформацію інших прапорів. |
| CREDITS\_GENERAL | Головні розробники: Концепція та дизайн мови, автори PHP та модуля SAPI. |
| CREDITS\_GROUP | Список розробників ядра мови |
| CREDITS\_MODULES | Список модулів для PHP та їх авторів |
| CREDITS\_SAPI | Список модулів серверних API та їх авторів |

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Приклад #1 Виводить головних розробників**

```php
<?php
phpcredits(CREDITS_GENERAL);
?>
```

**Приклад #2 Виводить розробників ядра та учасників команди документування**

```php
<?php
phpcredits(CREDITS_GROUP | CREDITS_DOCS | CREDITS_FULLPAGE);
?>
```

**Приклад #3 Виведення всіх розробників**

```php
<html>
 <head>
  <title>Сведения об авторах</title>
 </head>
 <body>
<?php
// какой-то код
phpcredits(CREDITS_ALL - CREDITS_FULLPAGE);
// ещё код
?>
 </body>
</html>
```

### Примітки

> **Зауваження** :
> 
> У режимі роботи з командного рядка (CLI) **phpcredits()** виводить звичайний текст замість HTML.

### Дивіться також

-   [phpversion()](function.phpversion.md) \- Отримує поточну версію PHP
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
