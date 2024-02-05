---
navigation:
  - function.assert-options.md: « assert\_options
  - function.cli-get-process-title.md: cli\_get\_process\_title »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: assert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# assert

(PHP 4, PHP 5, PHP 7, PHP 8)

assert — Перевіряє затвердження

### Опис

```methodsynopsis
assert(mixed $assertion, Throwable|string|null $description = null): bool
```

Функция**assert()** — дозволяє визначення очікувань: твердження, які набувають чинності у середовищах розробки та тестування, але оптимізовані так, що у виробничому середовищі мають нульову вартість.

Затвердження слід використовувати лише як налагоджувальну функцію. Один із варіантів їх використання — перевірка на осудність попередніх умов, які завжди мають бути **`true`** і якщо вони не виконуються, це свідчить про помилки програмування. Інший випадок використання – переконатися в наявності певних можливостей, наприклад, функцій модуля або певних обмежень та можливостей системи.

Оскільки твердження можуть бути налаштовані на відмову від них, їх *не* слід використовувати для звичайних операцій під час виконання, як-от перевірка вхідних параметрів. Як правило, код повинен поводитися так, як очікується, навіть якщо перевірка тверджень вимкнена.

Функция**assert()** перевіряє, чи виконується очікування, задане у параметрі `assertion`. Якщо ні, і в результаті повернулося значення **`false`**, то функция**assert()** виконає задану конфігурацією дію.

Поведение конструкции**assert()** визначається наступними налаштуваннями INI:

**Опції налаштування конструкції assert**

| Имя | По умолчанию | Опис | Список изменений |
| --- | --- | --- | --- |
| [zend.assertions](ini.core.md#ini.zend.assertions) |  |  |  |

-   : генерує та виконує код (режим розробки)
-   : генерує код, але перестрибує через нього під час виконання
-   `-1`: не генерує код (робочий режим)

[assert.active](info.configuration.md#ini.assert.active) **`true`** | Якщо **`false`**, функция**assert()** не перевіряє очікування та повертає **`true`**, безоговорочно. | Устарела с PHP 8.3.0. | |[assert.callback](info.configuration.md#ini.assert.callback) **`null`** | Функція, що визначається користувачем, викликана у разі невдалої перевірки затвердження. Її сигнатура має бути такою:

```methodsynopsis
assert_callback(    string $file,    int $line,    null $assertion,    string $description = ?): void
```

Застаріла із PHP 8.3.0. | До PHP 8.0.0 сигнатура callback-функції має бути:

```methodsynopsis
assert_callback(    string $file,    int $line,    string $assertion,    string $description = ?): void
```

[assert.exception](info.configuration.md#ini.assert.exception) **`true`** | Якщо **`true`**, буде викинута помилка [AssertionError](class.assertionerror.md)в случае неудачной проверки утверждения. | Устарела с PHP 8.3.0. | |[assert.bail](info.configuration.md#ini.assert.bail) **`false`** | Якщо **`true`**, виконання PHP-скрипту перерветься у разі невдалої перевірки затвердження. | Застаріла із PHP 8.3.0. | | [assert.warning](info.configuration.md#ini.assert.warning) **`true`** | Якщо **`true`**, у разі невдалої перевірки затвердження буде видано помилку рівня **`E_WARNING`**. Ця INI-настройка неефективна, якщо включена директива [assert.exception](info.configuration.md#ini.assert.exception)| Устарела с PHP 8.3.0. |

### Список параметрів

`assertion`

Будь-який вираз, що повертає значення, яке буде виконано, а результат використовується для вказівки того, чи вдалася чи не вдалася перевірка затвердження.

**Увага**

До версії PHP 8.0.0, якщо параметр `assertion` був рядком (string), він інтерпретований як PHP-код і виконувався за допомогою функції [eval()](function.eval.md). Цей рядок передавався в callback-функцію як третій аргумент. Ця поведінка *ЗАСТАРІЛО* в PHP 7.2.0 та *ВИДАЛЕНО* у PHP 8.0.0.

`description`

Якщо параметр `description` є екземпляром класу [Throwable](class.throwable.md), він буде викинутий лише в тому випадку, якщо перевірка затвердження `assertion` не вдастся.

> **Зауваження** :
> 
> Починаючи з PHP 8.0.0, це робиться *до* виклику потенційно певної callback-функції затвердження.

> **Зауваження** :
> 
> Починаючи з PHP 8.0.0, об'єкт (object) буде викинутий незалежно від конфігурації параметра [assert.exception](info.configuration.md#ini.assert.exception)

> **Зауваження** :
> 
> Начиная с PHP 8.0.0, параметр[assert.bail](info.configuration.md#ini.assert.bail) немає жодного ефекту у разі.

Якщо параметр `description` є рядком (string), це повідомлення використовуватиметься у разі викидання виключення чи попередження. Необов'язковий опис, який буде включено до повідомлення, якщо перевірка затвердження `assertion` не вдастся.

Якщо параметр `description` опущений. Під час компіляції створюється опис за промовчанням, що дорівнює вихідному коду для виклику **assert()**

### Значення, що повертаються

Функция**assert()** завжди повертатиме значення \*\*`true`\*\*якщо істинно хоча б одне з наступних тверджень:

-   `zend.assertions=0`
-   `zend.assertions=-1`
-   `assert.exception=1`
-   `assert.bail=1`
-   Об'єкт виключення користувача передано до параметра`description`

Якщо жодна з умов не є істинною, функція **assert()** поверне значення **`true`**, якщо параметр `assertion` правда, інакше поверне значення **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Всі INI-налаштування `assert.`устарели. |
| 8.0.0 | Функция**assert()** більше не буде оцінювати строкові аргументи, натомість вони розглядатимуться як будь-який інший аргумент. Замість `assert('$a == $b')` слід використовувати assert($a == $b). Директива `assert.quiet_eval` php.ini та константа **`ASSERT_QUIET_EVAL`** також були видалені, оскільки вони більше не матимуть жодного ефекту. |
| 8.0.0 | Якщо параметр `description` є екземпляром класу [Throwable](class.throwable.md), об'єкт викидається у разі невдалої перевірки затвердження, незалежно від значення [assert.exception](info.configuration.md#ini.assert.exception) |
| 8.0.0 | Якщо параметр `description` є екземпляром класу [Throwable](class.throwable.md), користувальницька callback-функція не викликається, навіть якщо вона встановлена. |
| 8.0.0 | Оголошення функції з ім'ям `assert()` всередині простору імен більше не допускається та видає помилку рівня **`E_COMPILE_ERROR`** |
| 7.3.0 | Оголошення функції `assert()` усередині простору імен застаріло. Таке оголошення тепер видає помилку рівня **`E_DEPRECATED`** |
| 7.2.0 | Використання рядка (string) як `assertion` застаріло. Тепер воно видає помилку рівня **`E_DEPRECATED`**, коли значення та [assert.active](info.configuration.md#ini.assert.active) і [zend.assertions](ini.core.md#ini.zend.assertions) одно |

### Приклади

**Приклад #1 Приклад использования функции**assert()\*\*\*\*

```php
<?php
assert(1 > 2);
echo 'Привет!';
```

Якщо твердження включені ([`zend.assertions=1`](ini.core.md#ini.zend.assertions)), то приклад вище виведе:

```
Fatal error: Uncaught AssertionError: assert(1 > 2) in example.php:2
Stack trace:
#0 example.php(2): assert(false, 'assert(1 > 2)')
#1 {main}
  thrown in example.php on line 2
```

Якщо твердження вимкнено (`zend.assertions=0`or`zend.assertions=-1`), то приклад вище виведе:

```
Привет!
```

**Приклад #2 Приклад повідомлення користувача**

```php
<?php
assert(1 > 2, "Ожидается, что один больше двух");
echo 'Привет!';
```

Якщо твердження включені, приклад вище виведе:

```
Fatal error: Uncaught AssertionError: Ожидается, что один больше двух in example.php:2
Stack trace:
#0 example.php(2): assert(false, 'Expected one to...')
#1 {main}
  thrown in example.php on line 2
```

Якщо твердження вимкнені, то приклад виведе:

```
Привет!
```

**Приклад #3 Приклад використання користувальницького класу виключення**

```php
<?php
class ArithmeticAssertionError extends AssertionError {}

assert(1 > 2, new ArithmeticAssertionError("Ожидается, что один больше двух"));
echo 'Hi!';
```

Якщо твердження включені, то приклад виведе:

```
Fatal error: Uncaught ArithmeticAssertionError: Ожидается, что один больше двух in example.php:4
Stack trace:
#0 {main}
  thrown in example.php on line 4
```

Якщо твердження вимкнені, приклад виведе:

```
Привет!
```

### Дивіться також

-   [assert\_options()](function.assert-options.md) \- Встановлення та отримання налаштувань механізму перевірки тверджень
