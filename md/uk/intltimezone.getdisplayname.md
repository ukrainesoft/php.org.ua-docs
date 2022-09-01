---
navigation:
  - intltimezone.getcanonicalid.html: '« IntlTimeZone::getCanonicalID'
  - intltimezone.getdstsavings.html: 'IntlTimeZone::getDSTSavings »'
  - index.html: PHP Manual
  - class.intltimezone.html: IntlTimeZone
title: 'IntlTimeZone::getDisplayName'
---
# IntlTimeZone::getDisplayName

# intltzgetdisplayname

(PHP 5 >= 5.5.0, PHP 7, PHP 8, PECL >= 3.0.0a1)

IntlTimeZone::getDisplayName -- intltzgetdisplayname — Отримати ім'я часового поясу для відображення користувача

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public IntlTimeZone::getDisplayName(bool $dst = false, int $style = IntlTimeZone::DISPLAY_LONG, ?string $locale = null): string|false
```

Процедурний стиль:

```methodsynopsis
intltz_get_display_name(    IntlTimeZone $timezone,    bool $dst = false,    int $style = IntlTimeZone::DISPLAY_LONG,    ?string $locale = null): string|false
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`dst`

`style`

`locale`

### Значення, що повертаються
