---
navigation:
  - function.return.html: « return
  - function.include.html: include »
  - index.html: PHP Manual
  - language.control-structures.html: Управляющие конструкции
title: require
---
## require

(PHP 4, PHP 5, PHP 7, PHP 8)

`require` аналогічно [include](function.include.html), крім того, що у разі виникнення помилки він також видасть фатальну помилку рівня **`E_COMPILE_ERROR`**. Іншими словами, він зупинить виконання скрипту, тоді як [include](function.include.html) тільки видав би попередження \*\*`E_WARNING`\*\*що дозволило б скрипту продовжити виконання.

Дивіться документацію з [include](function.include.html), щоб дізнатися, як він працює.
