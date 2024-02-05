---
navigation:
  - yaconf.has.md: '« Yaconf::has'
  - intro.taint.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.other.md: Інші базові модулі
title: Taint
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Taint

-   [Вступ](intro.taint.md)
-   [Встановлення та налаштування](taint.setup.md)
    -   [Вимоги](taint.requirements.md)
    -   [Установка](taint.installation.md)
    -   [Налаштування під час виконання](taint.configuration.md)
    -   [Типи ресурсів](taint.resources.md)
-   [Додаткові подробиці](taint.detail.md)
    -   [Функції та оператори, які можуть поширювати сумнівний символ зіпсованого рядка](taint.detail.basic.md)
    -   [Функції та оператори, які перевіряють зіпсовані рядки](taint.detail.taint.md)
    -   [Функції, які не будуть обробляти зіпсований рядок](taint.detail.untaint.md)
-   [Функції Taint](ref.taint.md)
    -   [is\_tainted](function.is-tainted.md)— Перевіряє, чи зіпсований рядок
    -   [taint](function.taint.md)— Зіпсувати рядок
    -   [untaint](function.untaint.md) \- Виправити рядок
