---
navigation:
  - yaf-request-abstract.setbaseuri.md: '« Yaf\_Request\_Abstract::setBaseUri'
  - yaf-request-abstract.setdispatched.md: 'Yaf\_Request\_Abstract::setDispatched »'
  - index.md: PHP Manual
  - class.yaf-request-abstract.md: Yaf\_Request\_Abstract
title: 'Yaf\_Request\_Abstract::setControllerName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Request\_Abstract::setControllerName

(Yaf >=1.0.0)

Yaf\_Request\_Abstract::setControllerName — Встановлює ім'я контролера

### Опис

```methodsynopsis
public Yaf_Request_Abstract::setControllerName(string $controller, bool $format_name = true): void
```

Встановлює ім'я контролера для запиту, зазвичай використовується маршрутизатором, що налаштовується для встановлення імені контролера результату маршруту.

### Список параметрів

`controller`

string, ім'я контролера, має бути в CamelCase, наприклад, "Index" або "Foo\_Bar"

`format_name`

Добавлено в Yaf 3.2.0, по умолчанию Yaf отформатирует имя в CamelCase, если для него установлено значение\*\*`false`\*\*, Yaf встановить оригінальне ім'я на запит.

### Значення, що повертаються
