---
navigation:
  - language.types.intro.md: « Введение
  - language.types.integer.md: Цілі числа "
  - index.md: PHP Manual
  - language.types.md: Типи
title: Бульов
---
## Бульов

Це найпростіший тип. bool виражає істинність значення. Він може бути або **`true`**, або **`false`**

### Синтаксис

Для вказівки bool, використовуйте константи **`true`** або **`false`**. Вони обидві реєстронезалежні.

```php
<?php
$foo = True; // присвоить $foo значение TRUE
?>
```

Зазвичай, деякий [оператор](language.operators.md) повертає значення типу bool, яке потім передається [управляющей конструкции](language.control-structures.html)

```php
<?php
// == это оператор, который проверяет
// эквивалентность и возвращает boolean
if ($action == "show_version") {
    echo "Версия 1.23";
}

// это необязательно...
if ($show_separators == TRUE) {
    echo "<hr>\n";
}

// ... потому что следующее имеет тот же самый смысл:
if ($show_separators) {
    echo "<hr>\n";
}
?>
```

### Перетворення на булев тип

Для явного перетворення на bool, використовуйте `(bool)` або `(boolean)`. Однак, у більшості випадків приведення типу необов'язкове, оскільки значення буде автоматично перетворено, якщо оператор, функція або конструкція, що управляє, вимагає аргумент типу bool.

Дивіться також [маніпуляції з типами](language.types.type-juggling.html)

При перетворенні в bool, наступні значення розглядаються як **`false`**

-   саме значення [boolean](language.types.boolean.md) **`false`**
-   [integer](language.types.integer.md) 0 (нуль)
-   [float](language.types.float.md) 0.0 (нуль) та -0.0 (мінус нуль)
-   порожня [рядок](language.types.string.md), і [рядок](language.types.string.md) "0"
-   [Масив](language.types.array.md) без елементів
-   особливий тип [NULL](language.types.null.md) (включаючи невстановлені змінні)
-   об'єкти [SimpleXML](ref.simplexml.md), Створені з порожніх елементів без атрибутів, тобто елементів, що не мають ні дочірніх елементів, ні атрибутів.

Всі інші значення розглядаються як **`true`** (включаючи будь-який [resource](language.types.resource.md) і **`NAN`**

**Увага**

`-1` розглядається як **`true`**, як і будь-яке інше ненульове (негативне чи позитивне) число!

```php
<?php
var_dump((bool) "");        // bool(false)
var_dump((bool) "0");       // bool(false)
var_dump((bool) 1);         // bool(true)
var_dump((bool) -2);        // bool(true)
var_dump((bool) "foo");     // bool(true)
var_dump((bool) 2.3e5);     // bool(true)
var_dump((bool) array(12)); // bool(true)
var_dump((bool) array());   // bool(false)
var_dump((bool) "false");   // bool(true)
?>
```
