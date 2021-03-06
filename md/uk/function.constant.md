- [«connection_status](function.connection-status.md)
- [define »](function.define.md)

- [PHP Manual](index.md)
- [Різні функції](ref.misc.md)
- Повертає значення константи

# constant

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

constant — Повертає значення константи

### Опис

**constant**(string `$name`):
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Повертає значення константи, вказаної у параметрі `name`.

Функція **constant()** корисна, якщо вам потрібно отримати значення
константи, але невідомо її ім'я. Наприклад, якщо воно зберігається в
змінною або повертається функцією.

Ця функція також працює з [константами класів](language.oop5.constants.md).

### Список параметрів

`name`
Ім'я константи.

### Значення, що повертаються

Повертає значення константи.

### Помилки

Викидається виняток [Error](class.error.md), якщо константа не
визначено. До PHP 8.0.0 у цьому випадку видавалася помилка рівня
**`E_WARNING`**.

### Список змін

| Версія | Опис                                                                                                                                                                               |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.0.0  | Якщо константа не визначена, функція **constant()** тепер викидає виняток [Error](class.error.md); раніше видавалася помилка рівня **E_WARNING** та поверталося значення **null**. |

### Приклади

**Приклад #1 Приклад функції **constant()****

`<?phpdefine("MAXSIZE", 100);echo MAXSIZE;echo constant("MAXSIZE"); // результат аналогічний попередньому висновкуinterface bar {    const test = 'foobar!';}class foo {   const test = 'foobar!';}$const ':}' ; // string(7) "foobar!"var_dump(constant('foo::'. $const)); // string(7) "foobar!"?> `

### Дивіться також

- [define()](function.define.md) - Визначає іменовану константу
- [defined()](function.defined.md) - Перевіряє існування
зазначеної іменованої константи
- Дивіться розділ [Константи](language.constants.md)
