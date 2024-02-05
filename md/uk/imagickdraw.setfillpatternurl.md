---
navigation:
  - imagickdraw.setfillopacity.md: '« ImagickDraw::setFillOpacity'
  - imagickdraw.setfillrule.md: 'ImagickDraw::setFillRule »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFillPatternURL'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFillPatternURL

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFillPatternURL — Встановлює URL-адресу для використання як зразка заливки для заливки об'єктів

### Опис

```methodsynopsis
public ImagickDraw::setFillPatternURL(string $fill_url): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює URL-адресу для використання як зразка заливки для об'єктів. В даний час підтримуються лише локальні URL-адреси ("#identifier"). Ці локальні URL-адреси зазвичай створюються шляхом визначення іменованого зразка заливки за допомогою DrawPushPattern/DrawPopPattern.

### Список параметрів

`fill_url`

URL-адреса, яка використовується для отримання зразка заливки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
