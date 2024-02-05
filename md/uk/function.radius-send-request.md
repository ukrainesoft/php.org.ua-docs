---
navigation:
  - function.radius-salt-encrypt-attr.md: « radius\_salt\_encrypt\_attr
  - function.radius-server-secret.md: radius\_server\_secret »
  - index.md: PHP Manual
  - ref.radius.md: Функції Radius
title: radius\_send\_request
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# radius\_send\_request

(PECL radius >= 1.1.0)

radius\_send\_request — Надсилає запит і чекає на відповідь

### Опис

```methodsynopsis
radius_send_request(resource $radius_handle): int
```

Після створення запиту Radius надсилає його за допомогою **radius\_send\_request()**

Функция**radius\_send\_request()** відправляє запит і чекає на коректну відповідь, повторюючи спроби з певними серверами в циклічному режимі в міру необхідності.

### Список параметрів

`radius_handle`

Ресурс RADIUS

### Значення, що повертаються

Якщо отримано коректну відповідь, **radius\_send\_request()** повертає код Radius, який вказує тип відповіді. Зазвичай це **`RADIUS_ACCESS_ACCEPT`** **`RADIUS_ACCESS_REJECT`**или**`RADIUS_ACCESS_CHALLENGE`**. Якщо коректної відповіді не отримано, **radius\_send\_request()** повертає **`false`**

### Дивіться також

-   [radius\_create\_request()](function.radius-create-request.md) \- Створює обліковий запис або запит автентифікації
