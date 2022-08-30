Використання простору імен: основи

-   [« Опис кількох просторів імен в одному файлі](language.namespaces.definitionmultiple.html)
    
-   [Простір імен та динамічні особливості мови »](language.namespaces.dynamic.html)
    
-   [PHP Manual](index.html)
    
-   [Пространства имён](language.namespaces.html)
    
-   Використання простору імен: основи
    

## Використання простору імен: основи

(PHP 5> = 5.3.0, PHP 7, PHP 8)

До обговорення використання просторів імен важливо зрозуміти, як PHP дізнається, які елементи з простору імен запитуються у вашому коді. Можна провести аналогію між просторами імен PHP та файловою системою. Є три способи звернутися до файлу у файловій системі:

1.  Відносне ім'я файлу, таке як `foo.txt`, що перетворюється на `currentdirectory/foo.txt`, де поточнадиректорія - поточна директорія, в якій ми знаходимося. Тоді, якщо поточна директорія `/home/foo`, то ім'я перетворюється на `/home/foo/foo.txt`
2.  Відносне ім'я шляху, таке як `subdirectory/foo.txt`, перетворюється на `currentdirectory/subdirectory/foo.txt`
3.  Абсолютне ім'я шляху, таке як `/main/foo.txt`, Що залишається таким же: `/main/foo.txt`

Той же принцип застосовується і до елементів з просторів імен PHP. Наприклад, ім'я класу може бути вказано трьома способами:

1.  Неповні імена (імена класів без префіксу), такі як `$a = new foo();` або `foo::staticmethod();`. Якщо поточний простір імен `currentnamespace`, то ці імена перетворюються на `currentnamespace\foo`. Якщо код знаходиться в глобальному просторі імен, то імена залишаються такими ж: `foo`. Попередження: неповні імена для функцій та констант будуть визначатися у глобальному просторі імен, якщо вони не визначені у поточному просторі імен. Детальніше у [Використання просторів імен: доступ до глобальних функцій та класів](language.namespaces.fallback.html)
2.  Повні імена (імена класів із префіксами), такі як `$a = new subnamespace\foo();` або `subnamespace\foo::staticmethod();`. Якщо поточний простір імен `currentnamespace`, то ці імена перетворюються на `currentnamespace\subnamespace\foo`. Якщо код знаходиться у глобальному просторі імен, то імена перетворюються на `subnamespace\foo`
3.  Абсолютні імена або імена з попереднім префіксом, що означає глобальний простір . `$a = new \currentnamespace\foo();` або `\currentnamespace\foo::staticmethod();`. Імена завжди визначаються так само, як і записані: `currentnamespace\foo`

Нижче наведено приклад трьох варіантів синтаксису в реальному коді:

file1.php

```php
<?php
namespace Foo\Bar\subnamespace;

const FOO = 1;
function foo() {}
class foo
{
    static function staticmethod() {}
}
?>
```

file2.php

```php
<?php
namespace Foo\Bar;
include 'file1.php';

const FOO = 2;
function foo() {}
class foo
{
    static function staticmethod() {}
}

/* Неполные имена */
foo(); // определяется как функция Foo\Bar\foo
foo::staticmethod(); // определяется как класс Foo\Bar\foo с методом staticmethod
echo FOO; // определяется как константа Foo\Bar\FOO

/* Полные имена */
subnamespace\foo(); // определяется как функция Foo\Bar\subnamespace\foo
subnamespace\foo::staticmethod(); // определяется как класс Foo\Bar\subnamespace\foo
                                  // c методом staticmethod
echo subnamespace\FOO; // определяется как константа Foo\Bar\subnamespace\FOO

/* Абсолютные имена */
\Foo\Bar\foo(); // определяется как функция Foo\Bar\foo
\Foo\Bar\foo::staticmethod(); // определяется как класс Foo\Bar\foo с методом staticmethod
echo \Foo\Bar\FOO; // определяется как константа Foo\Bar\FOO
?>
```

Зверніть увагу, що для доступу до будь-яких глобальних класів, функцій або константів може використовуватися абсолютне ім'я, таке як **strlen()**, або **Exception**, або `\INI_ALL`

**Приклад #1 Доступ до глобальних класів, функцій та константів із простору імен**

```php
<?php
namespace Foo;

function strlen() {}
const INI_ALL = 3;
class Exception {}

$a = \strlen('hi'); // вызывает глобальную функцию strlen
$b = \INI_ALL; // получает доступ к глобальной константе INI_ALL
$c = new \Exception('error'); // Создаёт экземпляр глобального класса Exception
?>
```