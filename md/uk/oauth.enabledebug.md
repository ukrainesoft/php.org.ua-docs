---
navigation:
  - oauth.disablesslchecks.md: '« OAuth::disableSSLChecks'
  - oauth.enableredirects.md: 'OAuth::enableRedirects »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::enableDebug'
---
# OAuth::enableDebug

(PECL OAuth >= 0.99.3)

OAuth::enableDebug — Включити детальну інформацію про налагодження

### Опис

```methodsynopsis
public OAuth::enableDebug(): bool
```

Включає докладну інформацію про запит, корисний для налагодження. Відлагоджувальна інформація зберігається в полі `debugInfo`. Альтернативно можна встановити полю `debug` значення non-**`false`**, щоб увімкнути режим налагодження.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**

### список змін

| Версия | Описание |
| --- | --- |
| PECL oauth 0.99.8 | Були додані поля `debug` і `debugInfo` |

### Дивіться також

-   [OAuth::disableDebug()](oauth.disabledebug.md) - Вимкнути докладну налагоджувальну інформацію
