Читає дані сесії

-   [« SessionHandlerInterface::open](sessionhandlerinterface.open.html)
    
-   [SessionHandlerInterface::write »](sessionhandlerinterface.write.html)
    
-   [PHP Manual](index.html)
    
-   [SessionHandlerInterface](class.sessionhandlerinterface.html)
    
-   Читає дані сесії
    

# SessionHandlerInterface::read

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::read — Читає дані сесії

### Опис

```methodsynopsis
public SessionHandlerInterface::read(string $id): string|false
```

Читає дані сесії зі сховища сесій та повертає результат. Викликається відразу після старту сесії або коли викликана [sessionstart()](function.session-start.html). Зверніть увагу, що перед викликом цього методу буде викликано функцію [SessionHandlerInterface::open()](sessionhandlerinterface.open.html)

Цей метод викликається PHP, коли стартує сесія. Цей метод має отримати дані сесії зі сховища за вказаним її ідентифікатором. Рядок, що повертається цим методом, повинен мати той же серіалізований формат, що й вихідний, який передавався функції [SessionHandlerInterface::write()](sessionhandlerinterface.write.html). Якщо запис не знайдено, повертається **`false`**

Дані, що повертаються цим методом, будуть розшифровані всередині PHP, використовуючи метод десеріалізації, зазначений у [session.serializehandler](session.configuration.html#ini.session.serialize-handler). Отримані дані будуть використані для заповнення суперглобального масиву [SESSION](reserved.variables.session.html)

Зверніть увагу, що схема серіалізації даних не така, як у функції [unserialize()](function.unserialize.html), і отримати доступ до даних можна за допомогою функції [sessiondecode()](function.session-decode.html)

### Список параметрів

`id`

Ідентифікатор сесії

### Значення, що повертаються

Повертає закодований рядок прочитаних даних. Якщо нічого не прочитано, повертається **`false`**. Зауважте, що це значення передається для обробки всередині PHP.

### Дивіться також

-   INI-директива [session.serializehandler](session.configuration.html#ini.session.serialize-handler)