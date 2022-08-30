Оновити позначку часу

-   [« SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.md)
    
-   [SessionUpdateTimestampHandlerInterface::validateId »](sessionupdatetimestamphandlerinterface.validateid.md)
    
-   [PHP Manual](index.md)
    
-   [SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.md)
    
-   Оновити позначку часу
    

# SessionUpdateTimestampHandlerInterface::updateTimestamp

(PHP 7, PHP 8)

SessionUpdateTimestampHandlerInterface::updateTimestamp — Оновити позначку часу

### Опис

```methodsynopsis
public SessionUpdateTimestampHandlerInterface::updateTimestamp(string $id, string $data): bool
```

Оновлює позначку часу останньої зміни сеансу. Функція автоматично виконується під час оновлення сеансу.

### Список параметрів

`id`

Ідентифікатор сесії

`data`

Дані сесії.

### Значення, що повертаються

Повертає **`true`**, якщо мітку часу оновлено, **`false`** в іншому випадку. Зауважте, що це значення повертається всередині PHP для обробки.