Перевірити ідентифікатор

-   [« SessionUpdateTimestampHandlerInterface::updateTimestamp](sessionupdatetimestamphandlerinterface.updatetimestamp.html)
    
-   [Обработка текста »](refs.basic.text.html)
    
-   [PHP Manual](index.html)
    
-   [SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.html)
    
-   Перевірити ідентифікатор
    

# SessionUpdateTimestampHandlerInterface::validateId

(PHP 7, PHP 8)

SessionUpdateTimestampHandlerInterface::validateId — Перевірити ідентифікатор

### Опис

```methodsynopsis
public SessionUpdateTimestampHandlerInterface::validateId(string $id): bool
```

Перевіряє цей ідентифікатор сесії. Ідентифікатор сесії є дійсним, якщо сесія з таким ідентифікатором вже існує. Функція автоматично виконується під час запуску сесії, вказується ідентифікатор сесії та вмикається [session.use\_strict\_mode](session.configuration.html#ini.session.use-strict-mode)

### Список параметрів

`id`

Ідентифікатор сесії

### Значення, що повертаються

Повертає **`true`** для коректного ідентифікатора, **`false`** в іншому випадку. Зауважте, що це значення повертається всередині PHP для обробки.