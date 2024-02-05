---
navigation:
  - language.oop5.constants.md: « Константи класів
  - language.oop5.decon.md: Конструктори та деструктори »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Автоматичне завантаження класів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Автоматичне завантаження класів

Більшість розробників об'єктно-орієнтованих додатків використовують таку угоду іменування файлів, в якій кожен клас зберігається в окремо створеному для нього файлі. Одна з найбільших неприємностей - необхідність писати на початку кожного скрипта довгий список файлів, що підвантажуються (по одному для кожного класу).

Функция[spl\_autoload\_register()](function.spl-autoload-register.md) дозволяє зареєструвати необхідну кількість автозавантажувачів для автоматичного завантаження класів та інтерфейсів, якщо вони не визначені. Реєструючи автозавантажувачі, PHP отримує останній шанс для інтерпретатора завантажити клас, перш ніж він закінчить виконання скрипта з помилкою.

Будь-яка конструкція, подібна до класу може бути автоматично завантажена таким же чином, включаючи класи, інтерфейси, трейти та перерахування.

**Застереження**

До PHP 8.0.0 можна було використати [\_\_autoload()](function.autoload.md) для автозавантаження класів та інтерфейсів. Однак це менш гнучка альтернатива [spl\_autoload\_register()](function.spl-autoload-register.md), функция[\_\_autoload()](function.autoload.md) оголошено застарілою в PHP 7.2.0 і видалено в PHP 8.0.0.

> **Зауваження** :
> 
> Функция[spl\_autoload\_register()](function.spl-autoload-register.md) може бути викликана кілька разів, щоб зареєструвати кілька автозавантажувачів. Викид виключення з автозавантаження, однак, перерве цей процес і не дозволить запускати подальші функції автозавантаження. З цієї причини викидати винятки з функції автозавантаження не рекомендується.

**Приклад #1 Приклад автоматичного завантаження**

У цьому прикладі функція намагається завантажити класи `MyClass1`и`MyClass2` з файлів MyClass1.php та MyClass2.php відповідно.

```php
<?php
spl_autoload_register(function ($class_name) {
    include $class_name . '.php';
});

$obj  = new MyClass1();
$obj2 = new MyClass2();
?>
```

**Приклад #2 Ще один приклад автоматичного завантаження**

У цьому прикладі подано спробу завантаження інтерфейсу `ITest`

```php
<?php

spl_autoload_register(function ($name) {
    var_dump($name);
});

class Foo implements ITest {
}

/*
string(5) "ITest"

Fatal error: Interface 'ITest' not found in ...
*/
?>
```

### Дивіться також

-   [unserialize()](function.unserialize.md)
-   [unserialize\_callback\_func](var.configuration.md#ini.unserialize-callback-func)
-   [unserialize\_max\_depth](var.configuration.md#ini.unserialize-max-depth)
-   [spl\_autoload\_register()](function.spl-autoload-register.md)
-   [spl\_autoload()](function.spl-autoload.md)
-   [\_\_autoload()](function.autoload.md)
