Зашифровує значення за допомогою солі

-   [« radius\_request\_authenticator](function.radius-request-authenticator.html)
    
-   [radius\_send\_request »](function.radius-send-request.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Зашифровує значення за допомогою солі
    

# radiussaltencryptattr

(PECL radius >= 1.3.0)

radiussaltencryptattr - Зашифровує значення за допомогою солі

### Опис

```methodsynopsis
radius_salt_encrypt_attr(resource $radius_handle, string $data): string|false
```

Застосовує алгоритм шифрування RADIUS до заданого значення.

Як правило, це робиться автоматично шляхом надання опції **`RADIUS_OPTION_SALT`** функцію встановлення атрибута, але цю функцію можна використовувати, якщо потрібно створення низькорівневого запиту.

### Список параметрів

`data`

Дані, які потрібно зашифрувати за допомогою солі.

### Значення, що повертаються

Повертає дані, зашифровані за допомогою солі або **`false`** у разі виникнення помилки.

### Дивіться також

-   [radius\_put\_addr()](function.radius-put-addr.html) - Приєднує атрибут IP-адреси
-   [radius\_put\_attr()](function.radius-put-attr.html) - приєднує бінарний атрибут
-   [radius\_put\_int()](function.radius-put-int.html) - Приєднує цілісний атрибут
-   [radius\_put\_string()](function.radius-put-string.html) - Приєднує рядковий атрибут