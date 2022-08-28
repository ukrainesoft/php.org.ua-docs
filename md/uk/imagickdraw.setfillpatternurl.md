Встановлює URL-адресу для використання як зразка заливки для заливки об'єктів

-   [« ImagickDraw::setFillOpacity](imagickdraw.setfillopacity.html)
    
-   [ImagickDraw::setFillRule »](imagickdraw.setfillrule.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Встановлює URL-адресу для використання як зразка заливки для заливки об'єктів
    

# ImagickDraw::setFillPatternURL

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFillPatternURL — Встановлює URL-адресу для використання як зразка заливки для заливки об'єктів

### Опис

```methodsynopsis
public ImagickDraw::setFillPatternURL(string $fill_url): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює URL-адресу для використання як зразка заливки для об'єктів. В даний час підтримуються лише локальні URL-адреси ("#identifier"). Ці локальні URL-адреси зазвичай створюються шляхом визначення іменованого зразка заливки за допомогою DrawPushPattern/DrawPopPattern.

### Список параметрів

`fill_url`

URL-адреса, яка використовується для отримання зразка заливки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.