Відправляє запит і чекає на відповідь

-   [« radiussaltencryptattr](function.radius-salt-encrypt-attr.html)
    
-   [radiusserversecret »](function.radius-server-secret.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Radius](ref.radius.html)
    
-   Відправляє запит і чекає на відповідь
    

# radiussendrequest

(PECL radius >= 1.1.0)

radiussendrequest — Надсилає запит і чекає на відповідь

### Опис

```methodsynopsis
radius_send_request(resource $radius_handle): int
```

Після створення запиту Radius надсилає його за допомогою **radiussendrequest()**

Функція **radiussendrequest()** відправляє запит і чекає на коректну відповідь, повторюючи спроби з певними серверами в циклічному режимі в міру необхідності.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Якщо отримано коректну відповідь, **radiussendrequest()** повертає код Radius, який вказує тип відповіді. Зазвичай це **`RADIUS_ACCESS_ACCEPT`** **`RADIUS_ACCESS_REJECT`** або **`RADIUS_ACCESS_CHALLENGE`**. Якщо коректної відповіді не отримано, **radiussendrequest()** повертає **`false`**

### Дивіться також

-   [radiuscreaterequest()](function.radius-create-request.html) - Створює обліковий запис або запит автентифікації