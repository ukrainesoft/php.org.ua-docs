---
navigation:
  - language.types.null.md: « NULL
  - language.types.integer.md: Цілі числа "
  - index.md: PHP Manual
  - language.types.md: Типи
title: Логічний тип
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Логічний тип

У логічного типу (bool) лише два значення, що використовуються для вираження істиннісного значення. Він може бути або **`true`**, либо\*\*`false`\*\*

### Синтаксис

Для вказівки bool, використовуйте константи **`true`**или**`false`**. Вони обидві реєстронезалежні.

```php
<?php
$foo = True; // присвоить $foo значение TRUE
?>
```

Зазвичай, деякий [оператор](language.operators.md) повертає значення типу bool, яке потім передається [керуючої конструкції](language.control-structures.md)

```php
<?php
// == это оператор, который проверяет
// эквивалентность и возвращает boolean
if ($action == "show_version") {
    echo "Версия 1.23";
}

// это необязательно...
if ($show_separators == TRUE) {
    echo "<hr>\n";
}

// ... потому что следующее имеет тот же самый смысл:
if ($show_separators) {
    echo "<hr>\n";
}
?>
```

### Перетворення на логічний тип

Для явного преобразования в bool, используйте приведение`(bool)`. Зазвичай у цьому немає потреби, оскільки при використанні значення в логічному контексті воно автоматично інтерпретується як значення логічного типу (bool). Додаткову інформацію дивіться на сторінці [маніпуляції з типами](language.types.type-juggling.md)

При преобразовании в bool, следующие значения рассматриваются как\*\*`false`\*\* :

-   саме значення[boolean](language.types.boolean.md) **`false`**
-   [integer](language.types.integer.md) (нуль)
-   [float](language.types.float.md) `0.0`(нуль) та`-0.0`(мінус нуль)
-   порожня[рядок](language.types.string.md) `""`и[рядок](language.types.string.md) `"0"`
-   [масив](language.types.array.md)без елементів
-   особливий тип[NULL](language.types.null.md)(включаючи невстановлені змінні)
-   внутрішні об'єкти, які перевантажують свою поведінку приведення до логічного типу. Наприклад: об'єкти[SimpleXML](ref.simplexml.md)створені з порожніх елементів без атрибутів.

Всі інші значення вважаються **`true`** (включаючи [resource](language.types.resource.md)и\*\*`NAN`\*\*

**Увага**

`-1` розглядається як **`true`**, як і будь-яке інше ненульове (негативне чи позитивне) число!

```php
<?php
var_dump((bool) "");        // bool(false)
var_dump((bool) "0");       // bool(false)
var_dump((bool) 1);         // bool(true)
var_dump((bool) -2);        // bool(true)
var_dump((bool) "foo");     // bool(true)
var_dump((bool) 2.3e5);     // bool(true)
var_dump((bool) array(12)); // bool(true)
var_dump((bool) array());   // bool(false)
var_dump((bool) "false");   // bool(true)
?>
```
