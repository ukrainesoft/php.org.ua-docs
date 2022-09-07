---
navigation:
  - yaf-request-abstract.setdispatched.md: '« YafRequestAbstract::setDispatched'
  - yaf-request-abstract.setparam.md: 'YafRequestAbstract::setParam »'
  - index.md: PHP Manual
  - class.yaf-request-abstract.md: YafRequestAbstract
title: 'YafRequestAbstract::setModuleName'
---
# YafRequestAbstract::setModuleName

(Yaf >=1.0.0)

YafRequestAbstract::setModuleName — Встановлює ім'я модуля

### Опис

```methodsynopsis
public Yaf_Request_Abstract::setModuleName(string $module, bool $format_name = true): void
```

Встановлює ім'я модуля для запиту, зазвичай використовується маршрутизатором, що налаштовується для встановлення імені модуля результату маршруту.

### Список параметрів

`module`

string ім'я модуля, має бути в CamelCase, наприклад, "Index" або "FooBar"

`format_name`

Додано в Yaf 3.2.0, за умовчанням Yaf відформатує ім'я CamelCase, якщо для нього встановлено значення **`false`**, Yaf встановить оригінальне ім'я на запит.

### Значення, що повертаються
