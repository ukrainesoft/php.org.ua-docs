---
navigation:
  - function.ui-quit.md: « UI\\quit
  - class.ui-draw-text-font-weight.md: UI\\Draw\\Text\\Font\\Weight »
  - index.md: PHP Manual
  - ref.ui.md: Функції UI
title: UI\\run
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\run

(UI 2.0.0)

UI\\run — Увійти до циклу UI

### Опис

```methodsynopsis
UI\run(int $flags = ?): void
```

Наказує PHP увійти до головного циклу, за замовчуванням контроль не повертається до ініціатора

### Список параметрів

`flags`

Вимушує UI\\Loop повернути управління, а UI\\Wait повернути керування після очікування

### Значення, що повертаються
