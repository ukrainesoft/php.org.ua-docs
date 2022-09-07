---
navigation:
  - book.mailparse.md: « Mailparse
  - mailparse.setup.md: Встановлення та налаштування »
  - index.md: PHP Manual
  - book.mailparse.md: Mailparse
title: Вступ
---
# Вступ

Mailparse – це модуль для аналізу та роботи з поштовими повідомленнями. Модуль працює з повідомленнями, сумісними з [» RFC 822](http://www.faqs.org/rfcs/rfc822) і [» RFC 2045](http://www.faqs.org/rfcs/rfc2045) `MIME`

Mailparse не тримає в пам'яті копії файлів, що обробляються, що дуже ефективно з точки зору ресурсів при обробці об'ємних повідомлень.

> **Зауваження**
> 
> Для Mailparse потрібна наявність модуля [mbstring](book.mbstring.md) і він повинен бути завантажений перед mailparse.
