---
navigation:
  - yaf-response-abstract.appendbody.md: '« YafResponseAbstract::appendBody'
  - yaf-response-abstract.clearheaders.md: 'YafResponseAbstract::clearHeaders »'
  - index.md: PHP Manual
  - class.yaf-response-abstract.md: YafResponseAbstract
title: 'YafResponseAbstract::clearBody'
---
# YafResponseAbstract::clearBody

(Yaf >=1.0.0)

YafResponseAbstract::clearBody — Скидає все існуюче тіло відповіді

### Опис

```methodsynopsis
public Yaf_Response_Abstract::clearBody(string $key = ?): bool
```

Очищає існуючий вміст

### Список параметрів

`key`

Ключ вмісту, якщо ви не вкажете, буде очищено весь вміст.

> **Зауваження**
> 
> Параметр було додано з 2.2.0

### Значення, що повертаються

### Дивіться також

-   [YafResponseAbstract::setBody()](yaf-response-abstract.setbody.md) - Встановлює вміст відповіді
-   [YafResponseAbstract::appendBody()](yaf-response-abstract.appendbody.md) - Додає вміст до тіла відповіді
-   [YafResponseAbstract::prependBody()](yaf-response-abstract.prependbody.md) - Призначення prependBody
-   [YafResponseAbstract::getBody()](yaf-response-abstract.getbody.md) - Отримує наявний вміст
