---
navigation:
  - yaf-controller-abstract.getviewpath.html: '« YafControllerAbstract::getViewpath'
  - yaf-controller-abstract.initview.html: 'YafControllerAbstract::initView »'
  - index.md: PHP Manual
  - class.yaf-controller-abstract.html: YafControllerAbstract
title: 'YafControllerAbstract::init'
---
# YafControllerAbstract::init

(Yaf >=1.0.0)

YafControllerAbstract::init — Ініціалізатор контролера

### Опис

```methodsynopsis
public Yaf_Controller_Abstract::init(): void
```

[YafControllerAbstract::construct()](yaf-controller-abstract.construct.html) - Остаточний (final) метод, це означає, що користувачі не можуть перевизначити його. Але користувачі можуть визначити **YafControllerAbstract::init()**, який буде викликатись після створення екземпляра об'єкта контролера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

### Дивіться також

-   [YafControllerAbstract::construct()](yaf-controller-abstract.construct.html) - Конструктор класу YafControllerAbstract
