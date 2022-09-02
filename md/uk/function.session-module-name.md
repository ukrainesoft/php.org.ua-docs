---
navigation:
  - function.session-id.md: « sessionід
  - function.session-name.md: sessionname »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionmodulename
---
# sessionmodulename

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionmodulename — Повертає та/або встановлює модуль поточної сесії

### Опис

```methodsynopsis
session_module_name(?string $module = null): string|false
```

**sessionmodulename()** повертає назву поточного модуля сесії, яка також відома як [session.savehandler](session.configuration.md#ini.session.save-handler)

### Список параметрів

`module`

Якщо вказано параметр `module` і не дорівнює **`null`**, даний модуль буде використаний замість поточного. Передача значення `"user"` у цей параметр заборонено. Натомість має викликатися функція [sessionsetsavehandler()](function.session-set-save-handler.md) для встановлення користувальницького оброблювача.

### Значення, що повертаються

Повертає назву поточного модуля сесії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `module` тепер може бути **`null`** |
|  | На даний момент заборонено встановлювати ім'я модуля на значення `"user"`. Раніше це ігнорувалося. |
