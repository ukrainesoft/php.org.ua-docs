---
navigation:
  - function.ui-quit.html: « UIquit
  - class.ui-draw-text-font-weight.html: ОЙDrawTextFontWeight »
  - index.md: PHP Manual
  - ref.ui.md: Функции UI
title: ОЙrun
---
# ОЙrun

(UI 2.0.0)

ОЙrun — Увійти до циклу UI

### Опис

```methodsynopsis
UI\run(int $flags = ?): void
```

Наказує PHP увійти до головного циклу, за замовчуванням контроль не повертається до ініціатора

### Список параметрів

`flags`

Вимушує UILoop повернути управління, а UIWait повернути керування після очікування

### Значення, що повертаються
