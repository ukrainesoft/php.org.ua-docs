---
navigation:
  - function.session-commit.md: « sessioncommit
  - function.session-decode.md: sessiondecode »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessioncreateід
---
# sessioncreateід

(PHP 7> = 7.1.0, PHP 8)

sessioncreateid — Створює новий ідентифікатор сесії

### Опис

```methodsynopsis
session_create_id(string $prefix = ""): string|false
```

**sessioncreateid()** використовується створення нового ідентифікатора поточної сесії. Повертає ідентифікатор сесії, який не схильний до колізій.

За неактивної сесії перевірка на колізії не здійснюється.

Ідентифікатор сесії створюється відповідно до налаштувань php.ini.

Важливо використовувати той самий ідентифікатор користувача на вашому веб-сервері, що і для скрипту завдання сміття. В іншому випадку у вас можуть виникнути проблеми доступу, особливо з дескриптором збереження файлів.

### Список параметрів

`prefix`

Якщо вказано параметр `prefix`, то новий ідентифікатор сесії буде з префіксом `prefix`. Не всі символи можна використовувати в ідентифікаторі сесії. Дозволяється використовувати лише символи з діапазону: `a-z A-Z 0-9 , (запятая)` і `- (минус)`

### Значення, що повертаються

**sessioncreateid()** повертає новий, не схильний до колізій, ідентифікатор поточної сесії. Якщо використовується під час неактивної сесії, перевірка на колізії пропускається. У разі невдачі повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **sessioncreateid()** з функцією [sessionregenerateid()](function.session-regenerate-id.md)**

```php
<?php
// Функция My session start с управлением на основе временных меток
function my_session_start() {
    session_start();
    // Не разрешать использование слишком старых идентификаторов сессии
    if (!empty($_SESSION['deleted_time']) && $_SESSION['deleted_time'] < time() - 180) {
        session_destroy();
        session_start();
    }
}

// Функция My session regenerate id
function my_session_regenerate_id() {
    // Вызов session_create_id() пока сессия активна, чтобы
    // удостовериться в отсутствии коллизий.
    if (session_status() != PHP_SESSION_ACTIVE) {
        session_start();
    }
    // ВНИМАНИЕ: Никогда не используйте конфиденциальные строки в качестве префикса!
    $newid = session_create_id('myprefix-');
    // Установка временной метки удаления. Данные активной сессии не должны удаляться сразу же.
    $_SESSION['deleted_time'] = time();
    // Завершение сессии
    session_commit();
    // Убеждаемся в возможности установки пользовательского идентификатора сессии
    // ЗАМЕЧАНИЕ: Вы должны включать опцию use_strict_mode для обычных операций.
    ini_set('session.use_strict_mode', 0);
    // Установка нового пользовательского идентификатора сессии
    session_id($newid);
    // Старт сессии с пользовательским идентификатором
    session_start();
}

// Убеждаемся, что опция use_strict_mode включена.
// Опция use_strict_mode обязательна по соображениям безопасности.
ini_set('session.use_strict_mode', 1);
my_session_start();

// Идентификатор сессии должен генерироваться заново при:
//  - Входе пользователя в систему
//  - Выходе пользователя из системы
//  - По прошествии определённого периода времени
my_session_regenerate_id();

// Далее основной код программы
?>
```

### Дивіться також

-   [sessionregenerateid()](function.session-regenerate-id.md) - Генерує та оновлює ідентифікатор поточної сесії
-   [sessionstart()](function.session-start.md) - Стартує нову сесію, або відновлює існуючу
-   [session.usestrictmode](session.configuration.md#ini.session.use-strict-mode)
-   [SessionHandler::createsid()](sessionhandler.create-sid.md) - Повертає новий ідентифікатор сесії
