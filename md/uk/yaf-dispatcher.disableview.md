---
navigation:
  - yaf-dispatcher.construct.md: '« YafDispatcher::construct'
  - yaf-dispatcher.dispatch.md: 'YafDispatcher::dispatch »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: YafDispatcher
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
