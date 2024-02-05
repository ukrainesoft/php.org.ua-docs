---
navigation:
  - spoofchecker.setchecks.md: '« Spoofchecker::setChecks'
  - class.transliterator.md: Transliterator »
  - index.md: PHP Manual
  - class.spoofchecker.md: Spoofchecker
title: 'Spoofchecker::setRestrictionLevel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Spoofchecker::setRestrictionLevel

(PHP 7 >= 7.3.0, PHP 8)

Spoofchecker::setRestrictionLevel — Встановлює рівень обмеження

### Опис

```methodsynopsis
public Spoofchecker::setRestrictionLevel(int $level): void
```

Устанавливает уровень ограничения метода[SpoofChecker::isSuspicious()](spoofchecker.issuspicious.md)

### Список параметрів

`level`

Устанавливает уровень ограничения метода[SpoofChecker::isSuspicious()](spoofchecker.issuspicious.md)Одна из констант:**`Spoofchecker::ASCII`** **`Spoofchecker::SINGLE_SCRIPT_RESTRICTIVE`** **`Spoofchecker::HIGHLY_RESTRICTIVE`** **`Spoofchecker::MODERATELY_RESTRICTIVE`** **`Spoofchecker::MINIMALLY_RESTRICTIVE`**или**`Spoofchecker::UNRESTRICTIVE`**Значение по умолчанию**`Spoofchecker::HIGHLY_RESTRICTIVE`**

### Значення, що повертаються

Функція не повертає значення після виконання.
