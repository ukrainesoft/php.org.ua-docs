---
navigation:
  - language.oop5.anonymous.md: « Анонімні класи
  - language.oop5.iterations.md: Ітератори об'єктів »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Перевантаження
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Перевантаження

Перевантаження в PHP означає можливість динамічно створювати властивості та методи. Ці динамічні сутності обробляються за допомогою магічних методів, які можна створити у класі для різних видів дій.

Методи навантаження викликаються при взаємодії з властивостями або методами, які не були оголошені чи не [видно](language.oop5.visibility.md) у поточній області видимості. Далі в цьому розділі будуть використовуватися терміни недоступні властивості або недоступні методи позначення цієї комбінації оголошення і області видимості.

Усі методи навантаження мають бути оголошені як `public`

> **Зауваження** :
> 
> Жоден з аргументів цих магічних методів може бути переданий [за посиланням](functions.arguments.md#functions.arguments.by-reference)

> **Зауваження** :
> 
> Інтерпретація перевантаження PHP відрізняється від більшості об'єктно-орієнтованих мов. Традиційно перевантаження означає можливість мати кілька однойменних методів із різною кількістю та типами аргументів.

### Перевантаження властивостей

```methodsynopsis
public __set(string $name, mixed $value): void
```

```methodsynopsis
public __get(string $name): mixed
```

```methodsynopsis
public __isset(string $name): bool
```

```methodsynopsis
public __unset(string $name): void
```

Метод[\_\_set()](language.oop5.overloading.md#object.set) буде виконано під час запису даних у недоступні (захищені та приватні) або неіснуючі властивості.

Метод[\_\_get()](language.oop5.overloading.md#object.get) буде виконано під час читання даних із недоступних (захищених чи приватних) чи неіснуючих властивостей.

Метод[\_\_isset()](language.oop5.overloading.md#object.isset) буде виконано при використанні [isset()](function.isset.md) або [empty()](function.empty.md) на недоступних (захищених чи приватних) чи неіснуючих властивостях.

Метод[\_\_unset()](language.oop5.overloading.md#object.unset) буде виконано під час виклику [unset()](function.unset.md) на недоступній (захищеній або приватній) або неіснуючій властивості.

Аргумент $name являє собою ім'я властивості, що викликається. Метод [\_\_set()](language.oop5.overloading.md#object.set) містить аргумент $value, що є значенням, яке буде записано у властивість з ім'ям $name.

Перевантаження властивостей працює лише у контексті об'єкта. Дані магічні методи не будуть викликані у статичному контексті. Тому ці методи не повинні оголошуватися [статичними](language.oop5.static.md). При оголошенні будь-якого магічного методу як `static` буде видано попередження.

> **Зауваження** :
> 
> Возвращаемое значение[\_\_set()](language.oop5.overloading.md#object.set)будет проигнорировано из-за способа обработки в PHP оператора присваивания. Аналогично,[\_\_get()](language.oop5.overloading.md#object.get) ніколи не викликається при об'єднанні присвоювань, наприклад, таким чином:
> 
> ```
> $a = $obj->b = 8;
> ```

> **Зауваження** :
> 
> PHP не викликатиме перевантажений метод зсередини того ж перевантаженого методу. Це означає, що, наприклад, написання `return $this->foo`внутри[\_\_get()](language.oop5.overloading.md#object.get) поверне `null` та викличе помилку рівня **`E_WARNING`**, если не определено свойство`foo`замість того, щоб викликати метод [\_\_get()](language.oop5.overloading.md#object.get) вдруге. Однак методи перевантаження можуть неявно викликати інші методи навантаження (наприклад, метод [\_\_set()](language.oop5.overloading.md#object.set) викликає метод [\_\_get()](language.oop5.overloading.md#object.get)

**Приклад #1 Перевантаження властивостей за допомогою методів [\_\_get()](language.oop5.overloading.md#object.get) [\_\_set()](language.oop5.overloading.md#object.set) [\_\_isset()](language.oop5.overloading.md#object.isset) і [\_\_unset()](language.oop5.overloading.md#object.unset)**

```php
<?php
class PropertyTest
{
    /**  Место хранения перегружаемых данных.  */
    private $data = array();

    /**  Перегрузка не применяется к объявленным свойствам.  */
    public $declared = 1;

    /**  Здесь перегрузка будет использована только при доступе вне класса.  */
    private $hidden = 2;

    public function __set($name, $value)
    {
        echo "Установка '$name' в '$value'\n";
        $this->data[$name] = $value;
    }

    public function __get($name)
    {
        echo "Получение '$name'\n";
        if (array_key_exists($name, $this->data)) {
            return $this->data[$name];
        }

        $trace = debug_backtrace();
        trigger_error(
            'Неопределённое свойство в __get(): ' . $name .
            ' в файле ' . $trace[0]['file'] .
            ' на строке ' . $trace[0]['line'],
            E_USER_NOTICE);
        return null;
    }

    public function __isset($name)
    {
        echo "Установлено ли '$name'?\n";
        return isset($this->data[$name]);
    }

    public function __unset($name)
    {
        echo "Уничтожение '$name'\n";
        unset($this->data[$name]);
    }

    /**  Не магический метод, просто для Приклада. */
    public function getHidden()
    {
        return $this->hidden;
    }
}


echo "<pre>\n";

$obj = new PropertyTest;

$obj->a = 1;
echo $obj->a . "\n\n";

var_dump(isset($obj->a));
unset($obj->a);
var_dump(isset($obj->a));
echo "\n";

echo $obj->declared . "\n\n";

echo "Давайте поэкспериментируем с закрытым свойством 'hidden':\n";
echo "Закрытые свойства видны внутри класса, поэтому __get() не используется...\n";
echo $obj->getHidden() . "\n";
echo "Закрытые свойства не видны вне класса, поэтому __get() используется...\n";
echo $obj->hidden . "\n";
?>
```

Результат виконання наведеного прикладу:

```
Установка 'a' в '1'
Получение 'a'
1

Установлено ли 'a'?
bool(true)
Уничтожение 'a'
Установлено ли 'a'?
bool(false)

1

Давайте поэкспериментируем с закрытым свойством 'hidden':
Закрытые свойства видны внутри класса, поэтому __get() не используется...
2
Закрытые свойства не видны вне класса, поэтому __get() используется...
Получение 'hidden'


Notice: Неопределённое свойство в __get(): hidden в <file> on line 70 in <file> on line 29
```

### Перевантаження методів

```methodsynopsis
public __call(string $name, array $arguments): mixed
```

```methodsynopsis
public static __callStatic(string $name, array $arguments): mixed
```

[\_\_call()](language.oop5.overloading.md#object.call) запускається під час виклику недоступних методів у контексті об'єкт.

[\_\_callStatic()](language.oop5.overloading.md#object.callstatic) запускається під час виклику недоступних методів у статичному контексті.

Аргумент $name являє собою ім'я методу, що викликається. Аргумент $arguments є нумерованим масивом, що містить параметри, передані в метод $name, що викликається.

**Приклад #2 Перевантаження методів за допомогою методів [\_\_call()](language.oop5.overloading.md#object.call) і [\_\_callStatic()](language.oop5.overloading.md#object.callstatic)**

```php
<?php
class MethodTest {
    public function __call($name, $arguments) {
        // Замечание: значение $name регистрозависимо.
        echo "Вызов метода '$name' "
             . implode(', ', $arguments). "\n";
    }

    public static function __callStatic($name, $arguments) {
        // Замечание: значение $name регистрозависимо.
        echo "Вызов статического метода '$name' "
             . implode(', ', $arguments). "\n";
    }
}

$obj = new MethodTest;
$obj->runTest('в контексте объекта');

MethodTest::runTest('в статическом контексте');
?>
```

Результат виконання наведеного прикладу:

```
Вызов метода 'runTest' в контексте объекта
Вызов статического метода 'runTest' в статическом контексте
```
