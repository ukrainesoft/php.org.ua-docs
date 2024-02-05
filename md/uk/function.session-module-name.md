---
navigation:
  - function.session-id.md: « session\_id
  - function.session-name.md: session\_name »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_module\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_module\_name

(PHP 4, PHP 5, PHP 7, PHP 8)

session\_module\_name — Повертає та/або встановлює модуль поточної сесії

### Опис

```methodsynopsis
session_module_name(?string $module = null): string|false
```

**session\_module\_name()** повертає назву поточного модуля сесії, яка також відома як [session.save\_handler](session.configuration.md#ini.session.save-handler)

### Список параметрів

`module`

Если указан параметр`module`и не равен\*\*`null`\*\*, даний модуль буде використаний замість поточного. Передача значення `"user"` у цей параметр заборонено. Натомість має викликатися функція [session\_set\_save\_handler()](function.session-set-save-handler.md) для встановлення користувальницького оброблювача.

### Значення, що повертаються

Повертає назву поточного модуля сесії або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `module`тепер може бути\*\*`null`\*\* |
| 7.2.0 | На даний момент заборонено встановлювати ім'я модуля на значення `"user"`. . Раніше це ігнорувалося. |
