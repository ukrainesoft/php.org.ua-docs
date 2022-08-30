З'єднання із зовнішньою базою імен

-   [« GenderGender](class.gender.html)
    
-   [GenderGender::construct »](gender-gender.construct.html)
    
-   [PHP Manual](index.html)
    
-   [GenderGender](class.gender.html)
    
-   З'єднання із зовнішньою базою імен
    

# GenderGender::connect

(PECL gender >= 0.6.0)

GenderGender::connect — З'єднання із зовнішньою базою імен

### Опис

```methodsynopsis
public Gender\Gender::connect(string $dsn): bool
```

Підключення до зовнішнього словника імен. На даний момент підтримуються лише потокові ресурси.

### Список параметрів

`dsn`

DSN для відкриття.

### Значення, що повертаються

**`true`** або **`false`** залежно від успішності.