---
navigation:
  - oauth.destruct.md: '« OAuth::destruct'
  - oauth.disableredirects.md: 'OAuth::disableRedirects »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::disableDebug'
---
# OAuth::disableDebug

(PECL OAuth >= 0.99.3)

OAuth::disableDebug — Вимкнути детальну налагоджувальну інформацію

### Опис

```methodsynopsis
public OAuth::disableDebug(): bool
```

Вимикає докладну інформацію про запит (за замовчуванням вимкнено). Альтернативно можна встановити властивості [debug](class.oauth.html#oauth.props.debug) значення **`false`**, щоб вимкнути режим налагодження.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**

### список змін

| Версия | Описание |
| --- | --- |
| PECL oauth 0.99.8 | Було додано схожу властивість [debug](class.oauth.html#oauth.props.debug) |

### Дивіться також

-   [OAuth::enableDebug()](oauth.enabledebug.md) - Включити докладну налагоджувальну інформацію
