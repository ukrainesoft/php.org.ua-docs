Створює PHP-значення зі збереженого уявлення

-   [« strval](function.strval.md)
    
-   [unset »](function.unset.md)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи зі змінними](ref.var.md)
    
-   Створює PHP-значення зі збереженого уявлення
    

# unserialize

(PHP 4, PHP 5, PHP 7, PHP 8)

unserialize — Створює PHP-значення зі збереженого уявлення

### Опис

```methodsynopsis
unserialize(string $data, array $options = []): mixed
```

**unserialize()** приймає одну серіалізовану змінну і конвертує її у значення PHP.

**Увага**

Не передавайте неперевірені дані користувача в **unserialize()**, навіть якщо в `options` поставлено `allowed_classes`. Десеріалізація може створити код, який виконається при створенні об'єкта або автоматичному завантаженні коду, чим можуть скористатися несумлінні користувачі. Найкраще використовувати більш безпечні стандартні формати обміну даними, такі як JSON (за допомогою функцій [jsondecode()](function.json-decode.html) і [jsonencode()](function.json-encode.html)), якщо вам потрібно передати серіалізовані дані користувачеві.

Якщо вам потрібно десеріалізувати дані із зовнішніх джерел, використовуйте функцію [hashhmac()](function.hash-hmac.html) для перевірки цих даних. Переконайтеся, що ці дані, крім вас, ніхто не змінював.

### Список параметрів

`data`

Серіалізований рядок.

Якщо змінна, яка потребує десеріалізації, є об'єктом, то після успішного відновлення об'єкта PHP автоматично спробує викликати магічний метод [unserialize()](language.oop5.magic.html#object.unserialize) або [wakeup()](language.oop5.magic.html#object.wakeup) (якщо він існує).

> **Зауваження** **Директива unserializecallbackfunc**
> 
> Існує можливість вказати функцію зворотного виклику, яка буде викликана, якщо в процесі десеріалізації має бути проініціалізовано невизначений клас. (для запобігання отриманню неповного об'єкта (object) "PHPIncompleteClass"). Використовуйте php.ini, [iniset()](function.ini-set.html) або .htaccess для визначення функції [unserializecallbackfunc](var.configuration.html#ini.unserialize-callback-func). Ця функція буде викликатися щоразу, коли має бути проініціалізований невизначений клас. Щоб вимкнути цю можливість, просто залиште значення директиви порожнім.

`options`

Будь-які опції **unserialize()** у вигляді асоціативного масиву.

**Коректні опції**

| Имя | Тип | Описание |
| --- | --- | --- |
| `allowed_classes` | [mixed](language.types.declarations.html#language.types.declarations.mixed) | Масив імен класів, які мають бути прийняті, **`false`** для вказівки не приймати жодних класів або **`true`** для прийому всіх. Якщо ця опція задана та **unserialize()** виявить об'єкт неприйнятного класу, то він не буде прийнятий, а натомість інстанцується як об'єкт класу **PHPIncompleteClass**. Якщо опція не задана, то вона буде вважатися встановленою в **`true`**: PHP намагатиметься інстанцувати об'єкти будь-якого класу |

### Значення, що повертаються

Повертається перетворене значення, яке набуває одного з типів bool, int, float, string, array або object.

Якщо переданий рядок не піддається десеріалізації, повертається **`false`** та генерується **`E_NOTICE`**

### Помилки

Об'єкти можуть викидати [Throwable](class.throwable.md) у своїх оброблювачах десеріалізації.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер елемент `allowed_classes` параметра `options` строго типізований, тобто якщо що-небудь передано, крім array і bool, **unserialize()** поверне **`false`** та викличе помилку **`E_WARNING`** |

### Приклади

**Приклад #1 Приклад використання **unserialize()****

```php
<?php
// Мы используем функцию unserialize() для загрузки сессионных данных в Масив
// $session_data из строки, извлекаемой из базы данных.
// Данный пример дополняет пример, описывающий использование serialize().

$conn = odbc_connect("webdb", "php", "chicken");
$stmt = odbc_prepare($conn, "SELECT data FROM sessions WHERE id = ?");
$sqldata = array($_SERVER['PHP_AUTH_USER']);
if (!odbc_execute($stmt, $sqldata) || !odbc_fetch_into($stmt, $tmp)) {
    // если процедура извлечения данных не удалась, то инициализируем пустой Масив
    $session_data = array();
} else {
    // сейчас у нас должны быть сериализованные данные в $tmp[0].
    $session_data = unserialize($tmp[0]);
    if (!is_array($session_data)) {
        // что-то пошло не так, инициализируем пустой Масив
        $session_data = array();
    }
}
?>
```

**Приклад #2 Приклад використання unserializecallbackfunc**

```php
<?php
$serialized_object='O:1:"a":1:{s:5:"value";s:3:"100";}';

ini_set('unserialize_callback_func', 'mycallback'); // определяем свою callback-функцию

function mycallback($classname)
{
    // просто подключаете файл, содержащий определение класса
    // $classname указывает, для какого класса требуется определение
}
?>
```

### Примітки

**Увага**

**`false`** повертається як у разі виникнення помилки, так і у разі, якщо десеріалізується серіалізоване значення **`false`**. Цей особливий випадок можна відловити, використовуючи порівняння `data` зі значенням `serialize(false)`, або перехопивши згенеровану помилку **`E_NOTICE`**

### Дивіться також

-   [jsonencode()](function.json-encode.html) - Повертає JSON-подання даних
-   [jsondecode()](function.json-decode.html) - Декодує рядок JSON
-   [hashhmac()](function.hash-hmac.html) - Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [serialize()](function.serialize.md) - Генерує придатне для зберігання подання змінної
-   [Автоматичне завантаження класів](language.oop5.autoload.md)
-   [unserializecallbackfunc](var.configuration.html#ini.unserialize-callback-func)
-   [wakeup()](language.oop5.magic.html#object.wakeup)
-   [serialize()](language.oop5.magic.html#object.serialize)
-   [unserialize()](language.oop5.magic.html#object.unserialize)