Включити докладну налагоджувальну інформацію

-   [« OAuth::disableSSLChecks](oauth.disablesslchecks.html)
    
-   [OAuth::enableRedirects »](oauth.enableredirects.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Включити докладну налагоджувальну інформацію
    

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

-   [OAuth::disableDebug()](oauth.disabledebug.html) - Вимкнути докладну налагоджувальну інформацію