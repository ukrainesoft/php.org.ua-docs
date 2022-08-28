Виводить список розробників PHP

-   [« php\_uname](function.php-uname.html)
    
-   [phpinfo »](function.phpinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Опции PHP/информационные функции](ref.info.html)
    
-   Виводить список розробників PHP
    

# phpcredits

(PHP 4, PHP 5, PHP 7, PHP 8)

phpcredits - Виводить список розробників PHP

### Опис

```methodsynopsis
phpcredits(int $flags = CREDITS_ALL): bool
```

Ця функція виводить список розробників PHP, модулів тощо. Вона створює відповідний HTML-код для вставки на сторінку.

### Список параметрів

`flags`

Використання аргументу `flags` дозволяє довільно компонувати інформацію про окремі групи розробників.

**Обумовлені прапори **phpcredits()****

| Имя | Описание |
| --- | --- |
| CREDITSALL | Усі розробники, еквівалентно використанню: **`CREDITS_DOCS`** **`CREDITS_GENERAL`** **`CREDITS_GROUP`** **`CREDITS_MODULES`** **`CREDITS_FULLPAGE`**. У цьому випадку буде згенеровано повністю незалежну HTML-сторінку з відповідними тегами. |
| CREDITSDOCS | Учасники команди документування |
| CREDITSFULLPAGE | Зазвичай використовується у комбінації з іншими прапорами. Вказує на те, що незалежна HTML-сторінка повинна містити інформацію інших прапорів. |
| CREDITSGENERAL | Головні розробники: Концепція та дизайн мови, автори PHP та модуля SAPI. |
| CREDITSGROUP | Список розробників ядра мови |
| CREDITSMODULES | Список модулів для PHP та їх авторів |
| CREDITSSAPI | Список модулів серверних API та їх авторів |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

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
phpcredits(CREDITS_GROUP | CREDITS_DOCS | CREDITS_FULLPAGE);
?>
```

**Приклад #3 Виведення всіх розробників**

```php
<html>
 <head>
  <title>Сведения об авторах</title>
 </head>
 <body>
<?php
// какой-то код
phpcredits(CREDITS_ALL - CREDITS_FULLPAGE);
// ещё код
?>
 </body>
</html>
```

### Примітки

> **Зауваження**
> 
> У режимі роботи з командного рядка (CLI) **phpcredits()** виводить звичайний текст замість HTML.

### Дивіться також

-   [phpversion()](function.phpversion.html) - Отримує поточну версію PHP
-   [phpinfo()](function.phpinfo.html) - Виводить інформацію про поточну конфігурацію PHP