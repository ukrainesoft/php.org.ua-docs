---
navigation:
  - oauth.destruct.md: '« OAuth::\_\_destruct'
  - oauth.disableredirects.md: 'OAuth::disableRedirects »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::disableDebug'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::disableDebug

(PECL OAuth >= 0.99.3)

OAuth::disableDebug — Вимкнути детальну налагоджувальну інформацію

### Опис

```methodsynopsis
public OAuth::disableDebug(): bool
```

Вимикає докладну інформацію про запит (за замовчуванням вимкнено). Альтернативно можна встановити властивості [debug](class.oauth.md#oauth.props.debug)значение\*\*`false`\*\*, щоб вимкнути режим налагодження.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 0.99.8 | Було додано схожу властивість [debug](class.oauth.md#oauth.props.debug) |

### Дивіться також

-   [OAuth::enableDebug()](oauth.enabledebug.md) \- Включити докладну налагоджувальну інформацію
