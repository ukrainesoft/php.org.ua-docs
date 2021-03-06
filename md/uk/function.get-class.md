- [«get_class_vars](function.get-class-vars.md)
- [get_declared_classes »](function.get-declared-classes.md)

- [PHP Manual](index.md)
- [Функції роботи з класами та об'єктами](ref.classobj.md)
- Повертає ім'я класу, до якого належить об'єкт

#get_class

(PHP 4, PHP 5, PHP 7, PHP 8)

get_class — Повертає ім'я класу, до якого належить об'єкт

### Опис

**get_class**(object `$object` = ?): string

Повертає ім'я класу, екземпляром якого є об'єкт `object`.

### Список параметрів

`object`
Об'єкт, що тестується. Усередині класу цей параметр можна опустити.

> **Примітка**: Починаючи з PHP 7.2.0, явна передача **`null`** в
> `object` заборонено та видає помилку рівня **`E_WARNING`**. Починаючи з
> PHP 8.0.0, при передачі **`null`**, викидається виняток
> [TypeError](class.typeerror.md).

### Значення, що повертаються

Повертає ім'я класу, якого належить екземпляр `object`.

Якщо параметр `object` опущений усередині класу, буде повернено ім'я цього
класу.

Якщо параметр `object` є екземпляром класу, що існує в
просторі імен, то буде повернено повне ім'я із зазначенням
простору імен.

### Помилки

Якщо функція **get_class()** викликається з чимось, крім об'єкта,
викидається виняток [TypeError](class.typeerror.md). До PHP 8.0.0
видавалась помилка рівня **`E_WARNING`**.

Якщо функція **get_class()** викликається без аргументів поза класом,
викидається виняток [Error](class.error.md). До PHP 8.0.0
видавалась помилка рівня **`E_WARNING`**.

### Список змін

| Версія | Опис                                                                                                                                                                                                                       |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | Виклик функції поза класом без жодних аргументів викликає виняток [Error](class.error.md). Раніше видавалася помилка рівня **E_WARNING** та функція повертала значення **false**.                                          |
| 7.2.0  | До цієї версії значенням за умовчанням для object було null з тим же ефектом, що і відсутність передачі значення. Тепер **null** було видалено як значення за замовчуванням для object і більше не є допустимим значенням. |

### Приклади

**Приклад #1 Використання **get_class()****

`<?phpclass foo {   function name()    {        echo "Мене звуть " , get_class($this) , "
";    }}// створення об'єкта$bar = new foo();// зовнішній визовecho "Його ім'я " , get_class($bar) , "
";// внутрішній виклик$bar->name();?> `

Результат виконання цього прикладу:

Його ім'я foo
Мене звуть foo

**Приклад #2 Використання **get_class()** у батьківському класі**

`<?phpabstract class| var_dump(get_class()); }}class foo extends bar {}new foo;?> `

Результат виконання цього прикладу:

string(3) "foo"
string(3) "bar"

**Приклад #3 Використання **get_class()** з класами у просторах
імен**

`<?phpnamespace Foo\Bar;class Baz {    public function __construct()   {    }}$baz = new \Foo\Bar\Baz;var_dump(get_class($ba)

Результат виконання цього прикладу:

string(11) "Foo\Bar\Baz"

### Дивіться також

- [get_called_class()](function.get-called-class.md) - Ім'я класу,
отримане за допомогою пізнього статичного зв'язування
- [get_parent_class()](function.get-parent-class.md) - Повертає
ім'я батьківського класу для об'єкта чи класу
- [gettype()](function.gettype.md) - Повертає тип змінної
- [get_debug_type()](function.get-debug-type.md) - Повертає ім'я
типу змінної у вигляді, що підходить для налагодження
- [is_subclass_of()](function.is-subclass-of.md) - Перевіряє,
чи містить об'єкт у своєму дереві предків зазначений клас чи прямо
реалізує його
