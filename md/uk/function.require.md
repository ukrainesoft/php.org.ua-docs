---
navigation:
  - function.return.md: « return
  - function.include.md: include »
  - index.md: PHP Manual
  - language.control-structures.md: Управляющие конструкции
title: require
---
## require

(PHP 4, PHP 5, PHP 7, PHP 8)

`require` аналогічно [include](function.include.md), крім того, що у разі виникнення помилки він також видасть фатальну помилку рівня **`E_COMPILE_ERROR`**. Іншими словами, він зупинить виконання скрипту, тоді як [include](function.include.md) тільки видав би попередження \*\*`E_WARNING`\*\*що дозволило б скрипту продовжити виконання.

Дивіться документацію з [include](function.include.md), щоб дізнатися, як він працює.
