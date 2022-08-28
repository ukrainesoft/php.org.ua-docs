Генерує та оновлює ідентифікатор поточної сесії

-   [« session\_name](function.session-name.html)
    
-   [session\_register\_shutdown »](function.session-register-shutdown.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Генерує та оновлює ідентифікатор поточної сесії
    

# sessionregenerateід

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

sessionregenerateid — Генерує та оновлює ідентифікатор поточної сесії

### Опис

```methodsynopsis
session_regenerate_id(bool $delete_old_session = false): bool
```

**sessionregenerateid()** замінює ідентифікатор поточної сесії знову згенерованим, при цьому зберігає інформацію про поточну сесію.

При ввімкненій опції [session.use\_trans\_sid](session.configuration.html#ini.session.use-trans-sid), висновок має здійснюватися після виклику **sessionregenerateid()**. В іншому випадку використовуватиметься старий ідентифікатор сесії.

**Увага**

Поточна реалізація **sessionregenerateid()** погано працює з мережами з нестабільним з'єднанням, такими як мобільні та WiFi-мережі. Таким чином, є можливість втратити сесію через виклик **sessionregenerateid()**

Ви не повинні знищувати дані старої сесії негайно, а використовувати тимчасові мітки видалення і контролювати доступ до старої сесії. В іншому випадку конкуруючий доступ до сторінки може призвести до неузгодженого стану, втрати сесії або стану гонки на стороні клієнта (браузера), що, у свою чергу, призведе до створення безлічі ідентифікаторів сесії без необхідності. Негайне видалення сесії також унеможливлює виявлення та запобігання атакам при перехопленні сесії.

### Список параметрів

`delete_old_session`

Визначає, чи видаляти старий пов'язаний файл із сесією чи ні. Не слід видаляти стару сесію, якщо потрібно уникати стану гонки через видалення або виявляти/уникати атак під час перехоплення сесії.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sessionregenerateid()****

```php
<?php
// ЗАМЕЧАНИЕ: Это не полностью работающий код, а только пример!

session_start();

// Проверяем временную метку удаления
if (isset($_SESSION['destroyed'])
    && $_SESSION['destroyed'] < time() - 300) {
    // Обычно это не должно происходить. Это может быть атакой или результатом нестабильной сети.
    // Удаляем все статусы аутентификации пользователей этой сессии.
    remove_all_authentication_flag_from_active_sessions($_SESSION['userid']);
    throw(new DestroyedSessionAccessException);
}

$old_sessionid = session_id();

// Устанавливаем временную метку удаления
$_SESSION['destroyed'] = time(); // session_regenerate_id() сохраняет данные старой сессии

// Просто вызов session_regenerate_id() может привести к потере сессии и т.д.
// Смотрите следующий пример.
session_regenerate_id();

// Новой сессии не требуется временная метка удаления.
unset($_SESSION['destroyed']);

$new_sessionid = session_id();

echo "Старая сессия: $old_sessionid<br />";
echo "Новая сессия: $new_sessionid<br />";

print_r($_SESSION);
?>
```

Поточний модуль сесії не працює добре з мережами з нестабільним з'єднанням. Ви повинні керувати ідентифікатором сесії, щоб уникнути втрати сесії в результаті виклику **sessionregenerateid()**

**Приклад #2 Як уникнути втрати сесії під час використання **sessionregenerateid()****

```php
<?php
// ЗАМЕЧАНИЕ: Это не полностью работающий код, а только пример!
// my_session_start() и my_session_regenerate_id() избегают потери
// сессии из-за нестабильной сети. В дополнение, данный код может предотвращать
// использование украденных сессий злоумышленниками.

function my_session_start() {
    session_start();
    if (isset($_SESSION['destroyed'])) {
       if ($_SESSION['destroyed'] < time()-300) {
           // Обычно это не должно происходить. Это может быть атакой или результатом нестабильной сети.
           // Удаляем все статусы аутентификации пользователей этой сессии.
           remove_all_authentication_flag_from_active_sessions($_SESSION['userid']);
           throw(new DestroyedSessionAccessException);
       }
       if (isset($_SESSION['new_session_id'])) {
           // Срок действия ещё не полностью истёк. Cookie могли быть потеряны из-за нестабильной сети.
           // Заново пытаемся установить правильный cookie идентификатора сессиии.
           // ЗАМЕЧАНИЕ: Не пытайтесь заново установить идентификатор сессии если, вы предпочитаете
           // удалить флаг аутентификации.
           session_commit();
           session_id($_SESSION['new_session_id']);
           // Новый идентификатор сессии должен существовать.
           session_start();
           return;
       }
   }
}

function my_session_regenerate_id() {
    // Новый идентификатор сессии необходим для установки правильного идентификатора сессии,
    // когда идентификатор сессии не был установлен из-за нестабильной сети.
    $new_session_id = session_create_id();
    $_SESSION['new_session_id'] = $new_session_id;

    // Устанавливаем временную метку удаления.
    $_SESSION['destroyed'] = time();

    // Записываем и закрываем текущую сессию.
    session_commit();

    // Стартуем сессию с новым идентификатором.
    session_id($new_session_id);
    ini_set('session.use_strict_mode', 0);
    session_start();
    ini_set('session.use_strict_mode', 1);

    // Новой сессии не нужно это.
    unset($_SESSION['destroyed']);
    unset($_SESSION['new_session_id']);
}
?>
```

### Дивіться також

-   [session\_id()](function.session-id.html) - Отримує та/або встановлює ідентифікатор поточної сесії
-   [session\_create\_id()](function.session-create-id.html) - створює новий ідентифікатор сесії
-   [session\_start()](function.session-start.html) - Стартує нову сесію, або відновлює існуючу
-   [session\_destroy()](function.session-destroy.html) - Знищує всі дані сесії
-   [session\_reset()](function.session-reset.html) - реініціалізує сесію оригінальними значеннями
-   [session\_name()](function.session-name.html) - Отримати чи встановити ім'я поточної сесії