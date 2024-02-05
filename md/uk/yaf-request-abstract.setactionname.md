---
navigation:
  - yaf-request-abstract.isxmlhttprequest.md: '« Yaf\_Request\_Abstract::isXmlHttpRequest'
  - yaf-request-abstract.setbaseuri.md: 'Yaf\_Request\_Abstract::setBaseUri »'
  - index.md: PHP Manual
  - class.yaf-request-abstract.md: Yaf\_Request\_Abstract
title: 'Yaf\_Request\_Abstract::setActionName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Request\_Abstract::setActionName

(Yaf >=1.0.0)

Yaf\_Request\_Abstract::setActionName — Встановлює ім'я дії

### Опис

```methodsynopsis
public Yaf_Request_Abstract::setActionName(string $action, bool $format_name = true): void
```

Встановлює ім'я дії для запиту, зазвичай використовується маршрутизатором, що налаштовується для встановлення імені контролера результату маршруту.

### Список параметрів

`action`

string, ім'я дії, має бути вказано в нижньому регістрі, наприклад, "index" або "foo\_bar"

`format_name`

Додано в Yaf 3.2.0, за замовчуванням Yaf відформатує ім'я в нижньому регістрі, якщо для цього параметра встановлено значення **`false`**, Yaf встановить оригінальне ім'я на запит.

### Значення, що повертаються
