---
navigation:
  - yaf-request-abstract.setdispatched.md: '« Yaf\_Request\_Abstract::setDispatched'
  - yaf-request-abstract.setparam.md: 'Yaf\_Request\_Abstract::setParam »'
  - index.md: PHP Manual
  - class.yaf-request-abstract.md: Yaf\_Request\_Abstract
title: 'Yaf\_Request\_Abstract::setModuleName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Request\_Abstract::setModuleName

(Yaf >=1.0.0)

Yaf\_Request\_Abstract::setModuleName — Встановлює ім'я модуля

### Опис

```methodsynopsis
public Yaf_Request_Abstract::setModuleName(string $module, bool $format_name = true): void
```

Встановлює ім'я модуля для запиту, зазвичай використовується маршрутизатором, що налаштовується для встановлення імені модуля результату маршруту.

### Список параметрів

`module`

string ім'я модуля, має бути в CamelCase, наприклад, "Index" або "Foo\_Bar"

`format_name`

Добавлено в Yaf 3.2.0, по умолчанию Yaf отформатирует имя в CamelCase, если для него установлено значение\*\*`false`\*\*, Yaf встановить оригінальне ім'я на запит.

### Значення, що повертаються
