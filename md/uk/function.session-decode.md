Декодує дані сесії із закодованого рядка сесії

-   [« sessioncreateід](function.session-create-id.html)
    
-   [sessiondestroy »](function.session-destroy.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи із сесіями](ref.session.html)
    
-   Декодує дані сесії із закодованого рядка сесії
    

# sessiondecode

(PHP 4, PHP 5, PHP 7, PHP 8)

sessiondecode — Декодує дані сесії із закодованого рядка сесії

### Опис

```methodsynopsis
session_decode(string $data): bool
```

**sessiondecode()** декодує серіалізовані дані сесії, передані в `$data` і заповнює суперглобальний масив $SESSION отриманим результатом.

За замовчуванням використовується внутрішній метод десеріалізації PHP, і результат відрізнятиметься від формату, що повертається функцією [unserialize()](function.unserialize.html). Метод серіалізації може бути встановлений за допомогою [session.serializehandler](session.configuration.html#ini.session.serialize-handler)

### Список параметрів

`data`

Закодовані дані, які потрібно зберегти.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [sessionencode()](function.session-encode.html) - кодує дані поточної сесії у форматі рядка сесії
-   [session.serializehandler](session.configuration.html#ini.session.serialize-handler)