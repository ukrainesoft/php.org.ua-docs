---
navigation:
  - function.strval.md: « strval
  - function.unset.md: unset »
  - index.md: PHP Manual
  - ref.var.md: Функції для роботи зі змінними
title: unserialize
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# unserialize

(PHP 4, PHP 5, PHP 7, PHP 8)

unserialize — Створює PHP-значення зі збереженого уявлення

### Опис

```methodsynopsis
unserialize(string $data, array $options = []): mixed
```

Функция**unserialize()** приймає одну серіалізовану змінну та конвертує її назад у значення PHP.

**Увага**

Не рекомендовано передавати ненадійні дані користувача в функцію **unserialize()**, навіть якщо параметр `options`задано значение`allowed_classes`. Десеріалізація вміє створити код, який виконається при інстанціюванні об'єкта або автоматичному завантаженні коду, що можуть використовувати несумлінні користувачі. Краще викликати більш безпечні стандартні формати обміну даними, наприклад, JSON (функціями [json\_decode()](function.json-decode.md) і [json\_encode()](function.json-encode.md)), якщо потрібно передати серіалізовані дані користувачеві.

Коли потрібно десеріалізувати дані із зовнішніх джерел, користуються функцією [hash\_hmac()](function.hash-hmac.md), щоб перевірити ці дані. Перевіряють, щоб дані були змінені ніким, крім розробника.

### Список параметрів

`data`

Серіалізований рядок.

Якщо змінна об'єкт, що вимагає десеріалізації, то після успішного відновлення об'єкта PHP автоматично спробує викликати магічні методи. [\_\_unserialize()](language.oop5.magic.md#object.unserialize) або [\_\_wakeup()](language.oop5.magic.md#object.wakeup) (якщо визначено).

> **Зауваження** **Директива unserialize\_callback\_func**
> 
> Дозволено встановлювати callback-функцію, яка буде викликана, якщо при десеріалізації потрібно проініціалізувати невизначений клас (щоб унеможливити отримання неповного об'єкта (object) «\_\_PHP\_Incomplete\_Class»). Щоб визначити функцію для директиви [unserialize\_callback\_func](var.configuration.md#ini.unserialize-callback-func), користуються файлом php.ini, функцією [ini\_set()](function.ini-set.md) або файлом .htaccess. Функція буде викликатися щоразу, коли має бути проініціалізований невизначений клас. Для відключення цієї поведінки значення директиви залишають порожнім.

`options`

Будь-які опції у вигляді асоціативного масиву, які можна передавати в функцію **unserialize()**

**Коректні опції**

| Имя | Тип | Опис |
| --- | --- | --- |
| `allowed_classes` | [mixed](language.types.declarations.md#language.types.declarations.mixed) | Або масив імен класів, які мають бути прийняті, **`false`** для вказівки не приймати жодних класів, або **`true`**, щоб приймати все. Якщо ця опція задана та функція **unserialize()** виявить об'єкт неприйнятного класу, то він не буде прийнятий, а натомість інстанцується як об'єкт класу **\_\_PHP\_Incomplete\_Class**. . Якщо опція не задана, вважатиметься, що їй встановлено значення **`true`**: PHP спробує інстанцувати об'єкти будь-якого класу |
| `max_depth` | int | Максимальна глибина структур, дозволена при десеріалізації та призначена для запобігання переповненню стека. За умовчанням обмеження глибини становить `4096` та вимикається встановленням опції `max_depth`значення |

### Значення, що повертаються

Повертає перетворене значення, яке набуває одного з типів bool, int, float, string, array або object.

Якщо переданий рядок не піддається десеріалізації, повертає **`false`** та видає помилку рівня **`E_WARNING`**

### Помилки

Об'єктам дозволено викидати винятки [Throwable](class.throwable.md) у своїх оброблювачах десеріалізації.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер видає помилку рівня **`E_WARNING`**, якщо переданий рядок несеріалізується; раніше видавалася помилка рівня **`E_NOTICE`** |
| 7.4.0 | Доданий елемент `max_depth`в параметр`options` для встановлення максимальної глибини структур, дозволених під час десеріалізації. |
| 7.1.0 | Тепер елемент `allowed_classes`параметра`options` строго типізований, тобто якщо що-небудь передано, крім array і bool, **unserialize()** поверне **`false`** та викличе помилку **`E_WARNING`** |

### Приклади

**Приклад #1 Приклад использования функции**unserialize()\*\*\*\*

```php
<?php

// Используем функцию unserialize() для загрузки сессионных данных в массив
// $session_data из строки, извлекаемой из базы данных.
// Приклад дополняет Приклад, описывающий вызов функции serialize().

$conn = odbc_connect("webdb", "php", "chicken");
$stmt = odbc_prepare($conn, "SELECT data FROM sessions WHERE id = ?");
$sqldata = array($_SERVER['PHP_AUTH_USER']);
if (!odbc_execute($stmt, $sqldata) || !odbc_fetch_into($stmt, $tmp)) {
    // Если процедура извлечения данных не удалась, то инициализируем пустой массив
    $session_data = array();
} else {
    // Сейчас в элементе $tmp[0] должны быть сериализованные данные.
    $session_data = unserialize($tmp[0]);
    if (!is_array($session_data)) {
        // Что-то пошло не так, инициализируем пустой массив
        $session_data = array();
    }
}

?>
```

**Приклад #2 Приклад використання директиви unserialize\_callback\_func**

```php
<?php

$serialized_object='O:1:"a":1:{s:5:"value";s:3:"100";}';

ini_set('unserialize_callback_func', 'mycallback'); // определяем свою callback-функцию

function mycallback($classname)
{
    // просто подключаете файл, содержащий определение класса
    // переменная $classname указывает, для какого класса требуется определение
}

?>
```

### Примітки

**Увага**

Значение\*\*`false`\*\* повертається як у разі помилки, так і при десеріалізації серіалізованого значення **`false`**. Цей особливий випадок можна відловити, порівнявши значення параметра `data` зі значенням, яке повертає виклик `serialize(false)`, або перехопивши видану помилку рівня **`E_NOTICE`**

### Дивіться також

-   [json\_encode()](function.json-encode.md) \- Повертає JSON-подання даних
-   [json\_decode()](function.json-decode.md) \- Декодує рядок JSON
-   [hash\_hmac()](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Автоматичне завантаження класів](language.oop5.autoload.md)
-   [unserialize\_callback\_func](var.configuration.md#ini.unserialize-callback-func)
-   [unserialize\_max\_depth](var.configuration.md#ini.unserialize-max-depth)
-   [\_\_wakeup()](language.oop5.magic.md#object.wakeup)
-   [\_\_serialize()](language.oop5.magic.md#object.serialize)
-   [\_\_unserialize()](language.oop5.magic.md#object.unserialize)
