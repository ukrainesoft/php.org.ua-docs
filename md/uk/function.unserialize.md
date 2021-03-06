- [«strval](function.strval.md)
- [unset »](function.unset.md)

- [PHP Manual](index.md)
- [Функції для роботи зі змінними](ref.var.md)
- Створює PHP-значення зі збереженого уявлення

# unserialize

(PHP 4, PHP 5, PHP 7, PHP 8)

unserialize — Створює PHP-значення зі збереженого уявлення

### Опис

**unserialize**(string `$data`, array `$options` = []): [mixed](language.types.declarations.md#language.types.declarations.mixed)

**unserialize()** приймає одну серіалізовану змінну та
конвертує її назад у значення PHP.

**Увага**

Не передавайте неперевірені дані користувача в
**unserialize()**, навіть якщо в `options` задано `allowed_classes`.
Десеріалізація може створити код, який виконається під час створення
об'єкта або при автоматичному завантаженні коду, чим можуть скористатися
несумлінні користувачі. Краще використовувати безпечніші
стандартні формати обміну даними, такі як JSON (за допомогою функцій
[json_decode()](function.json-decode.md) та
[json_encode()](function.json-encode.md)), якщо вам потрібно передати
серіалізовані дані користувачеві.

Якщо вам потрібно десеріалізувати дані із зовнішніх джерел, використовуйте
функцію [hash_hmac()](function.hash-hmac.md) для перевірки цих даних.
Переконайтеся, що ці дані, крім вас, ніхто не змінював.

### Список параметрів

`data`
Серіалізований рядок.

Якщо змінна, яка потребує десеріалізації, є об'єктом, то після
успішного відновлення об'єкта PHP автоматично спробує викликати
магічний метод
[\_\_unserialize()](language.oop5.magic.md#object.unserialize) або
[\_\_wakeup()](language.oop5.magic.md#object.wakeup) (якщо він
існує).

> **Примітка**: **Директива unserialize_callback_func**
>
> Існує можливість вказати функцію зворотного дзвінка, яка буде
> викликана, якщо у процесі десеріалізації має бути проініціалізований
> невизначений клас. (для запобігання отриманню неповного об'єкта
> (object) "\_\_PHP_Incomplete_Class"). Використовуйте `php.ini`,
> [ini_set()](function.ini-set.md) або `.htaccess` для визначення
> функції
> [unserialize_callback_func](var.configuration.md#ini.unserialize-callback-func).
> Ця функція буде викликатися щоразу, коли має бути
> проініціалізований невизначений клас. Для відключення цієї
> можливості просто залиште значення директиви порожнім.

`options`
Будь-які опції **unserialize()** у вигляді асоціативного масиву.

| Ім'я Тип        | Опис                                                                      |
| --------------- | ------------------------------------------------------------------------- |
| allowed_classes | [mixed](language.types.declarations.md#language.types.declarations.mixed) | Масив імен класів, які мають бути прийняті, **false** для вказівки не приймати жодних класів або **true** для прийому всіх. Якщо ця опція задана і **unserialize()** виявить об'єкт неприйнятного класу, він не буде прийнятий, а замість цього інстанцується як об'єкт класу **\_\_PHP_Incomplete_Class**. Якщо опція не задана, вона буде вважатися встановленою в **true**: PHP намагатиметься інстанцювати об'єкти будь-якого класу. |      

**Коректні опції**

### Значення, що повертаються

Повертається перетворене значення, яке набуває одного з типів
bool, int, float, string, array або об'єкт.

У разі, якщо переданий рядок не піддається десеріалізації,
повертається **`false`** та генерується **`E_NOTICE`**.

### Помилки

Об'єкти можуть викидати [Throwable](class.throwable.md) у своїх
обробників десеріалізації.

### Список змін

| Версія | Опис                                                                                                                                                                                         |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 7.1.0  | Тепер елемент allowed_classes параметру options строго типізований, тобто якщо передано що-небудь, крім array та bool, **unserialize()** поверне **false** і викличе помилку **E_WARNING** . |

### Приклади

**Приклад #1 Приклад використання **unserialize()****

` <?php// Мы используем функцию unserialize() для загрузки сессионных данных в массив// $session_data из строки, извлекаемой из базы данных.// Данный пример дополняет пример, описывающий использование serialize().$conn = odbc_connect("webdb ", "php", "chicken");$stmt==odbc_prepare($conn, "SELECT data FROM sessions WHERE id = ?");$sqldata = array($_SERVER['PHP_AU! $stmt, $sqldata) || !odbc_fetch_into($stmt, $tmp)) {    // если процедура извлечения данных не удалась, то инициализируем пустой массив    $session_data = array();} else {    // сейчас у нас должны быть сериализованные дані в $tmp[0]. $session_data==unserialize($tmp[0]); if (!is_array($session_data)) {         // щось пішло не так, ініціалізуємо пустий масив         $session_day }}?> `

**Приклад #2 Приклад використання unserialize_callback_func**

` <?php$serialized_object='O:1:"a":1:{s:5:"value";s:3:"100";}';ini_set('unserialize_callback_func', 'mycallback'); // визначаємо свою callback-функціюfunction mycallback($classname){    /// просто підключаєте файл, містить визначення класу     // $classname вказує, для > 

### Примітки

**Увага**

**`false`** повертається як у разі виникнення помилки, так і в
у випадку, якщо десеріалізується серіалізоване значення **`false`**. Цей
особливий випадок можна відловити, використовуючи порівняння `data` зі значенням
`serialize(false)`, або перехопивши згенеровану помилку
**`E_NOTICE`**.

### Дивіться також

- [json_encode()](function.json-encode.md) - Повертає
JSON-подання даних
- [json_decode()](function.json-decode.md) - Декодує рядок JSON
- [hash_hmac()](function.hash-hmac.md) - Генерація хеш-коду на
основі ключа, використовуючи метод HMAC
- [serialize()](function.serialize.md) - Генерує придатне для
зберігання уявлення змінної
- [Автоматичне завантаження класів](language.oop5.autoload.md)
- [unserialize_callback_func](var.configuration.md#ini.unserialize-callback-func)
- [\_\_wakeup()](language.oop5.magic.md#object.wakeup)
- [\_\_serialize()](language.oop5.magic.md#object.serialize)
- [\_\_unserialize()](language.oop5.magic.md#object.unserialize)
