---
navigation:
  - function.radius-request-authenticator.html: « radiusrequestauthenticator
  - function.radius-send-request.html: radiussendrequest »
  - index.md: PHP Manual
  - ref.radius.md: Функции Radius
title: radiussaltencryptattr
---
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

-   [radiusputaddr()](function.radius-put-addr.md) - Приєднує атрибут IP-адреси
-   [radiusputattr()](function.radius-put-attr.md) - приєднує бінарний атрибут
-   [radiusputint()](function.radius-put-int.md) - Приєднує цілісний атрибут
-   [radiusputstring()](function.radius-put-string.md) - Приєднує рядковий атрибут
