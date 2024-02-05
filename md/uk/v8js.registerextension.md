---
navigation:
  - v8js.getpendingexception.md: '« V8Js::getPendingException'
  - class.v8jsexception.md: V8JsException »
  - index.md: PHP Manual
  - class.v8js.md: V8Js
title: 'V8Js::registerExtension'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# V8Js::registerExtension

(PECL v8js >= 0.1.0)

V8Js::registerExtension — Реєстрація модуля Javascript для V8Js

### Опис

```methodsynopsis
public static V8Js::registerExtension(    string $extension_name,    string $script,    array $dependencies = array(),    bool $auto_enable = false): bool
```

Реєстрація переданого у `script` Javascript як модуля для використання [V8Js](class.v8js.md)

### Список параметрів

`extension_name`

Ім'я модуля, що реєструється.

`script`

Код Javascript для реєстрації.

`dependencies`

Масив імен модулів, від яких залежить модуль, що реєструється. Кожен із цих модулів буде включений автоматично під час завантаження цього модуля.

> **Зауваження** :
> 
> Усі модулі, включаючи залежності, повинні бути зареєстровані до створення будь-яких [V8Js](class.v8js.md), що їх використовують.

`auto_enable`

Если установлено в\*\*`true`\*\*, модуль буде включений автоматично для будь-якого контексту [V8Js](class.v8js.md)

### Значення, що повертаються

Повертає **`true`** якщо модуль успішно зареєстровано або \*\*`false`\*\*в обратном случае.
