---
navigation:
  - function.eio-grp.md: « eio\_grp
  - function.eio-link.md: eio\_link »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_init

(PECL eio = 1.0.0)

eio\_init - (Ре-)ініціалізує Eio

### Опис

```methodsynopsis
eio_init(): void
```

**eio\_init()** (не-) ініціалізує Eio. Резервується пам'ять для внутрішніх структур libaio та Eio. Можна викликати **eio\_init()** перед використанням Eio-функцій. У будь-якому випадку ініціалізація буде виконана при першому виклику Eio-функції.

> **Зауваження** :
> 
> Функція була видалена у версії 3.0.0RC1 модуля eio для версії PHP 8 і вище.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
