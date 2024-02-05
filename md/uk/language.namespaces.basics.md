---
navigation:
  - language.namespaces.definitionmultiple.md: « Опис кількох просторів імен в одному файлі
  - language.namespaces.dynamic.md: Простір імен та динамічні особливості мови »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: 'Простори імен: основи'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Простори імен: основи

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

На початку обговорення того, як працюють простори імен, важливо зрозуміти, як PHP дізнається, які елементи із простору імен запитуються в коді. Можна провести аналогію між просторами імен PHP та файловою системою. Є три способи звернутися до файлу у файловій системі:

1.  Відносне ім'я файлу на кшталт`foo.txt`вирішиться у`currentdirectory/foo.txt`, где`currentdirectory`— поточна директорія, де ми знаходимося. Тоді, якщо поточна директорія`/home/foo`, то ім'я перетворюється на`/home/foo/foo.txt`
2.  Відносне ім'я шляху на кшталт`subdirectory/foo.txt`вирішиться у`currentdirectory/subdirectory/foo.txt`
3.  Абсолютне ім'я шляху на кшталт`/main/foo.txt`залишиться таким самим:`/main/foo.txt`

Той самий принцип збережеться під час вирішення елементів з просторів імен PHP. Наприклад, ім'я класу можна вказати трьома способами:

1.  Неповне ім'я або ім'я класу без префікса, на кшталт`$a = new foo();`или`foo::staticmethod();`. Якщо поточний простір імен`currentnamespace`, то це ім'я дозволиться у`currentnamespace\foo`. У коді в глобальному просторі імен ім'я залишиться таким самим:`foo`. Застереження: неповні імена функцій та констант будуть дозволені на глобальні функції та константи, якщо вони не визначені в поточному просторі імен. Докладніше про це розказано у розділі «[Простори імен: доступ до глобальних функцій та класів](language.namespaces.fallback.md)».
2.  Повне ім'я, або ім'я класу з префіксами, на зразок`$a = new subnamespace\foo();`или`subnamespace\foo::staticmethod();`. Якщо поточний простір імен`currentnamespace`, то це ім'я дозволиться у`currentnamespace\subnamespace\foo`. У коді в глобальному просторі імен ім'я дозволиться в`subnamespace\foo`
3.  Абсолютне ім'я або ім'я з префіксом на початку, який вказує на глобальний простір імен, на кшталт`$a = new \currentnamespace\foo();`или`\currentnamespace\foo::staticmethod();`. Таке ім'я дозволяється буквальне ім'я, задане в коді:`currentnamespace\foo`

Ось приклад трьох видів синтаксису у реальному коді:

file1.php

```php
<?php

namespace Foo\Bar\subnamespace;

const FOO = 1;
function foo() {}
class foo
{
    static function staticmethod() {}
}
?>
```

file2.php

```php
<?php

namespace Foo\Bar;
include 'file1.php';

const FOO = 2;
function foo() {}
class foo
{
    static function staticmethod() {}
}

/* Неполные имена */
foo(); // разрешается в функцию Foo\Bar\foo
foo::staticmethod(); // разрешается в метод staticmethod класса Foo\Bar\foo
echo FOO; // разрешается в константу Foo\Bar\FOO

/* Полные имена */
subnamespace\foo(); // разрешается в функцию Foo\Bar\subnamespace\foo
subnamespace\foo::staticmethod(); // разрешается в метод staticmethod класса Foo\Bar\subnamespace\foo
echo subnamespace\FOO; // разрешается в константу Foo\Bar\subnamespace\FOO

/* Абсолютные имена */
\Foo\Bar\foo(); // разрешается в функцию Foo\Bar\foo
\Foo\Bar\foo::staticmethod(); // разрешается в метод staticmethod класса Foo\Bar\foo
echo \Foo\Bar\FOO; // разрешается в константу Foo\Bar\FOO

?>
```

Зверніть увагу, що для доступу до глобальних класів, функцій або константів можна вказати абсолютне ім'я, наприклад, **\\strlen()** **\\Exception**или\\**`INI_ALL`**

**Приклад #1 Доступ до глобальних класів, функцій та константів із простору імен**

```php
<?php

namespace Foo;

function strlen() {}
const INI_ALL = 3;
class Exception {}

$a = \strlen('hi'); // Вызывает глобальную функцию strlen
$b = \INI_ALL; // Получает доступ к глобальной константе INI_ALL
$c = new \Exception('error'); // Создаёт экземпляр глобального класса Exception

?>
```
