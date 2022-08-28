Знищує всі дані сесії

-   [« session\_decode](function.session-decode.html)
    
-   [session\_encode »](function.session-encode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Знищує всі дані сесії
    

# sessiondestroy

(PHP 4, PHP 5, PHP 7, PHP 8)

sessiondestroy — Знищує всі дані сесії

### Опис

```methodsynopsis
session_destroy(): bool
```

**sessiondestroy()** знищує всі дані, пов'язані з поточною сесією. Ця функція не видаляє будь-які глобальні змінні, пов'язані з сесією та не видаляє сесійні cookie. Щоб знову використати змінні сесії, слід викликати [session\_start()](function.session-start.html)

> **Зауваження**: Немає необхідності викликати **sessiondestroy()** у звичайному коді. Очищайте масив $SESSION замість видалення сесії даних.

Щоб повністю видалити сесію, також необхідно видалити її ідентифікатор. Якщо для передачі ідентифікатора сесії використовуються cookie (поведінка за умовчанням), сесійні cookie також повинні бути видалені. Для цього можна використати [setcookie()](function.setcookie.html)

При ввімкненій опції [session.use\_strict\_mode](session.configuration.html#ini.session.use-strict-mode)Вам не потрібно видаляти застарілі cookie ідентифікатора сесії. У цьому немає необхідності, тому що модуль сесії не прийме cookie ідентифікатора сесії, якщо з цим ідентифікатором сесії немає пов'язаних даних, і модуль сесії встановить новий cookie ідентифікатора сесії. Рекомендується вмикати опцію [session.use\_strict\_mode](session.configuration.html#ini.session.use-strict-mode) для всіх веб-сайтів.

**Увага**

Негайне видалення сесії може призвести до небажаних наслідків. За наявності конкуруючих запитів інші з'єднання можуть зіткнутися з раптовою втратою даних сесії, наприклад, це можуть бути запити від JavaScript та/або запити з посилань URL.

Навіть якщо поточний модуль сесії не підтримує порожні cookie ідентифікатора сесії, негайне видалення сесії може призвести до порожнього cookie ідентифікатора сесії через стан гонки на стороні клієнта (браузера). Це призведе до того, що клієнт створить багато ідентифікаторів сесії без необхідності.

Щоб цього уникнути, необхідно встановити $SESSION тимчасову мітку видалення та прибрати доступ пізніше. Або переконатися, що ваша програма не має конкуруючих запитів. Це також стосується [session\_regenerate\_id()](function.session-regenerate-id.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Знищення сесії за допомогою [$\_SESSION](reserved.variables.session.html)**

```php
<?php
// Инициализируем сессию.
// Если вы используете session_name("something"), не забудьте добавить это перед session_start()!
session_start();

// Удаляем все переменные сессии.
$_SESSION = array();

// Если требуется уничтожить сессию, также необходимо удалить сессионные cookie.
// Замечание: Это уничтожит сессию, а не только данные сессии!
if (ini_get("session.use_cookies")) {
    $params = session_get_cookie_params();
    setcookie(session_name(), '', time() - 42000,
        $params["path"], $params["domain"],
        $params["secure"], $params["httponly"]
    );
}

// Наконец, уничтожаем сессию.
session_destroy();
?>
```

### Примітки

> **Зауваження**
> 
> Використовуйте [session\_unset()](function.session-unset.html) тільки для застарілого коду, де не використовується [$\_SESSION](reserved.variables.session.html)

### Дивіться також

-   [session.use\_strict\_mode](session.configuration.html#ini.session.use-strict-mode)
-   [session\_reset()](function.session-reset.html) - реініціалізує сесію оригінальними значеннями
-   [session\_regenerate\_id()](function.session-regenerate-id.html) - Генерує та оновлює ідентифікатор поточної сесії
-   [unset()](function.unset.html) - Видаляє змінну
-   [setcookie()](function.setcookie.html) - Надсилає cookie