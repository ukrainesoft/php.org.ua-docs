Перевірити ідентифікатор

-   [« SessionUpdateTimestampHandlerInterface::updateTimestamp](sessionupdatetimestamphandlerinterface.updatetimestamp.md)
    
-   [Обработка текста »](refs.basic.text.md)
    
-   [PHP Manual](index.md)
    
-   [SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.md)
    
-   Перевірити ідентифікатор
    

# SessionUpdateTimestampHandlerInterface::validateId

(PHP 7, PHP 8)

SessionUpdateTimestampHandlerInterface::validateId — Перевірити ідентифікатор

### Опис

```methodsynopsis
public SessionUpdateTimestampHandlerInterface::validateId(string $id): bool
```

Перевіряє цей ідентифікатор сесії. Ідентифікатор сесії є дійсним, якщо сесія з таким ідентифікатором вже існує. Функція автоматично виконується під час запуску сесії, вказується ідентифікатор сесії та вмикається [session.usestrictmode](session.configuration.html#ini.session.use-strict-mode)

### Список параметрів

`id`

Ідентифікатор сесії

### Значення, що повертаються

Повертає **`true`** для коректного ідентифікатора, **`false`** в іншому випадку. Зауважте, що це значення повертається всередині PHP для обробки.