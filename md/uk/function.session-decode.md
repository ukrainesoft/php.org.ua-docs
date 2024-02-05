---
navigation:
  - function.session-create-id.md: « session\_create\_id
  - function.session-destroy.md: session\_destroy »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_decode

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_decode — Декодує дані сесії із закодованого рядка сесії

### Опис

```methodsynopsis
session_decode(string $data): bool
```

**session\_decode()** декодує серіалізовані дані сесії, передані в `$data` і заповнює суперглобальний масив $\_SESSION отриманим результатом.

За замовчуванням використовується внутрішній метод десеріалізації PHP, і результат відрізнятиметься від формату, що повертається функцією [unserialize()](function.unserialize.md). Метод серіалізації може бути встановлений за допомогою [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)

### Список параметрів

`data`

Закодовані дані, які потрібно зберегти.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [session\_encode()](function.session-encode.md) \- кодує дані поточної сесії у форматі рядка сесії
-   [session.serialize\_handler](session.configuration.md#ini.session.serialize-handler)
