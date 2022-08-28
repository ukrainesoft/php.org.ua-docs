Стартує нову сесію або відновлює існуючу

-   [« session\_set\_save\_handler](function.session-set-save-handler.html)
    
-   [session\_status »](function.session-status.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Стартує нову сесію або відновлює існуючу
    

# sessionstart

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionstart — Стартує нову сесію або відновлює існуючу

### Опис

```methodsynopsis
session_start(array $options = []): bool
```

Функція **sessionstart()** створює сесію, або відновлює існуючу, ґрунтуючись на ідентифікаторі сесії, переданому через GET або POST-запит, або переданий через cookie.

Коли викликана функція **sessionstart()** або коли сесія створюється автоматично, PHP викликає відкриття та читання обробників запису сесії. Це можуть бути як вбудовані обробники, так і модулі (наприклад, SQLite або Memcached); або взагалі визначений користувачем обробник, заданий функцією [session\_set\_save\_handler()](function.session-set-save-handler.html). Callback-функція читання витягне всі існуючі дані сесії (збережені у спеціальному серіалізованому вигляді), десеріалізує їх і занесе до суперглобального масиву $SESSION, після чого поверне збережені дані обробнику сесій PHP.

Для використання іменованих сесій, використовуйте [session\_name()](function.session-name.html) перед **sessionstart()**

Якщо дозволено опцію [session.use\_trans\_sid](session.configuration.html#ini.session.use-trans-sid), функція **sessionstart()** реєструє внутрішній обробник виводу для перезапису URL-адрес.

Якщо користувач використовує `ob_gzhandler` або щось подібне спільно з функцією [ob\_start()](function.ob-start.html), Порядок функцій важливий для правильного виведення. Наприклад, `ob_gzhandler` має бути зареєстрований до старту сесії.

### Список параметрів

`options`

Якщо поставлено, то має бути асоціативним масивом, що перевизначає поточні [директивы конфигурации сессий](session.configuration.html). Ключі не повинні мати префіксу `session.`

На додаток до звичайного набору конфігураційних директив може бути додана опція `read_and_close`. Якщо встановлена ​​в **`true`**сесія буде закрита відразу ж після прочитання, теоретично дозволяючи уникнути блокування, якщо дані сесії не будуть змінюватися.

### Значення, що повертаються

Функція повертає **`true`**, якщо сесія успішно стартована, інакше **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | **sessionstart()** тепер повертає **`false`** і більше не ініціалізує [$\_SESSION](reserved.variables.session.html)коли вона не змогла запустити сесію. |

### Приклади

#### Простий приклад сесії

**Приклад #1 page1.php**

```php
<?php
// page1.php

session_start();

echo 'Добро пожаловать на страницу 1';

$_SESSION['favcolor'] = 'green';
$_SESSION['animal']   = 'cat';
$_SESSION['time']     = time();

// Работает, если сессионная cookie принята
echo '<br /><a href="page2.php">page 2</a>';

// Или можно передать идентификатор сессии, если нужно
echo '<br /><a href="page2.php?' . SID . '">page 2</a>';
?>
```

Після перегляду page1.php, друга сторінка page2.php чудово отримає всі дані сесії. Читайте розділ [работа с сессиями](ref.session.html), там розповідається про [передачу идентификаторов сессий](session.idpassing.html). Зокрема там розповідається про те, що таке константа **`SID`**

**Приклад #2 page2.php**

```php
<?php
// page2.php

session_start();

echo 'Добро пожаловать на страницу 2<br />';

echo $_SESSION['favcolor']; // green
echo $_SESSION['animal'];   // cat
echo date('Y m d H:i:s', $_SESSION['time']);

// Можете тут использовать идентификатор сессии, как в page1.php
echo '<br /><a href="page1.php">page 1</a>';
?>
```

#### Передача опцій у **sessionstart()**

**Приклад #3 Перевизначення часу життя cookie**

```php
<?php
// Устанавливаем срок действия cookie одному дню.
session_start([
    'cookie_lifetime' => 86400,
]);
?>
```

**Приклад #4 Читання та закриття сесії**

```php
<?php
// Если мы знаем, что в сессии не надо ничего изменять,
// мы можем просто прочитать её переменные и сразу закрыть,
// чтобы не блокировать файл сессии, который может понадобиться другим сессиям
session_start([
    'cookie_lifetime' => 86400,
    'read_and_close'  => true,
]);
```

### Примітки

> **Зауваження**
> 
> Для використання сесій на основі cookie, функція **sessionstart()** повинна бути викликана перед виведенням чогось у браузер.

> **Зауваження**
> 
> Використовуйте [zlib.output\_compression](zlib.configuration.html#ini.zlib.output-compression) замість [ob\_gzhandler()](function.ob-gzhandler.html)

> **Зауваження**
> 
> Ця функція надсилає кілька заголовків HTTP, залежно від налаштувань. Дивіться опис функції [session\_cache\_limiter()](function.session-cache-limiter.html) для керування цими заголовками.

### Дивіться також

-   [$\_SESSION](reserved.variables.session.html)
-   Директива конфігурації [session.auto\_start](session.configuration.html#ini.session.auto-start)
-   [session\_id()](function.session-id.html) - Отримує та/або встановлює ідентифікатор поточної сесії