- [« Threaded::isTerminated](threaded.isterminated.md)
- [Threaded::notify »](threaded.notify.md)

- [PHP Manual](index.md)
- [Threaded](class.threaded.md)
- обробка

# Threaded::merge

(PECL pthreads \>= 2.0.0)

Threaded::merge — Обробка

### Опис

public
**Threaded::merge**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$from`, bool `$overwrite` = ?): bool

Об'єднує дані у поточний об'єкт.

### Список параметрів

`from`
Дані об'єднання.

`overwrite`
Перезаписати існуючі ключі за промовчанням true.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Об'єднання з таблицею властивостей пов'язаного об'єкта**

` <?php$array = [];while (count($array) < 10)    $array[] = count($array);$stdClass = new stdClass();$stdClass->foo = "$o" stdClass->bar = "bar";$stdClass->baz = "baz";$safe = new Threaded();$safe->merge($array);$safe->foo = "bar";$safe- >merge($stdClass, false);var_dump($safe);?> `

Результат виконання цього прикладу:

object(Threaded)#2 (13) {
["0"]=>
int(0)
["1"]=>
int(1)
["2"]=>
int(2)
["3"]=>
int(3)
["4"]=>
int(4)
["5"]=>
int(5)
["6"]=>
int(6)
["7"]=>
int(7)
["8"]=>
int(8)
["9"]=>
int(9)
["foo"]=>
string(3) "bar"
["bar"]=>
string(3) "bar"
["baz"]=>
string(3) "baz"
}
