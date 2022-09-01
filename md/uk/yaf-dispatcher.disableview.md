---
navigation:
  - yaf-dispatcher.construct.html: '« YafDispatcher::construct'
  - yaf-dispatcher.dispatch.html: 'YafDispatcher::dispatch »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.html: YafDispatcher
title: 'YafDispatcher::disableView'
---
# YafDispatcher::disableView

(Yaf >=1.0.0)

YafDispatcher::disableView — Вимикає механізм перегляду

### Опис

```methodsynopsis
public Yaf_Dispatcher::disableView(): bool
```

Вимикає механізм перегляду, який використовується в деяких програмах, які користувач виводить самостійно

> **Зауваження**
> 
> Ви можете просто повернути **`false`** у дії, щоб запобігти автоматичному рендерингу цієї дії

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються
