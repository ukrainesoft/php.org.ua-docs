---
navigation:
  - imap.resources.md: « Типи ресурсів
  - ref.imap.md: Функції IMAP »
  - index.md: PHP Manual
  - book.imap.md: IMAP
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`NIL`**(int)

Оголошена застарілою починаючи з PHP 8.1.0.

**`OP_DEBUG`**(int)

**`OP_READONLY`**(int)

Відкрити поштову скриньку тільки для читання

**`OP_ANONYMOUS`**(int)

Не використовуйте оновлення .newsrc для новин (тільки для NNTP)

**`OP_SHORTCACHE`**(int)

**`OP_SILENT`**(int)

**`OP_PROTOTYPE`**(int)

**`OP_HALFOPEN`**(int)

Для IMAP та NNTP імен, відкрити з'єднання, але не відкривати поштову скриньку.

**`OP_EXPUNGE`**(int)

**`OP_SECURE`**(int)

**`CL_EXPUNGE`**(int)

Не надаючи жодних попереджень прати повідомлення перед тим, як закрити під час виклику [imap\_close()](function.imap-close.md)

**`FT_UID`**(int)

Параметром є UID

**`FT_PEEK`**(int)

Не встановлювати прапор \\Seen, якщо до цього він ще не встановлений

**`FT_NOT`**(int)

**`FT_INTERNAL`**(int)

Повертається рядок у внутрішньому форматі. Не буде канонізовано до виду CRLF.

**`FT_PREFETCHTEXT`**(int)

**`ST_UID`**(int)

Послідовність аргументів, що містить ідентифікатори UID замість послідовності номерів

**`ST_SILENT`**(int)

**`ST_SET`**(int)

**`CP_UID`**(int)

порядкові номери, що містять ідентифікатори UID

**`CP_MOVE`**(int)

Видалити повідомлення з поточної поштової скриньки після копіювання за допомогою [imap\_mail\_copy()](function.imap-mail-copy.md)

**`SE_UID`**(int)

Повертати ідентифікатори UID замість порядкових номерів

**`SE_FREE`**(int)

**`SE_NOPREFETCH`**(int)

Не виконувати передвиборку знайдених повідомлень

**`SO_FREE`**(int)

**`SO_NOSERVER`**(int)

**`SA_MESSAGES`**(int)

**`SA_RECENT`**(int)

**`SA_UNSEEN`**(int)

**`SA_UIDNEXT`**(int)

**`SA_UIDVALIDITY`**(int)

**`SA_ALL`**(int)

**`LATT_NOINFERIORS`**(int)

Ця поштова скринька не має "нащадків". (Поштові скриньки за цим відсутні)

**`LATT_NOSELECT`**(int)

Це лише контейнер, а не поштова скринька. Ви не можете його відкрити.

**`LATT_MARKED`**(int)

Ця поштова скринька позначена. Використовується лише UW-IMAPD.

**`LATT_UNMARKED`**(int)

Ця поштова скринька не помічена. Використовується лише з UW-IMAPD.

**`LATT_REFERRAL`**(int)

Цей контейнер має напрямки (referral) на віддалену поштову скриньку.

**`LATT_HASCHILDREN`**(int)

Ця поштова скринька має підпорядковані (inferiors).

**`LATT_HASNOCHILDREN`**(int)

Ця поштова скринька не має підлеглі (inferiors).

**`SORTDATE`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): дата написання

**`SORTARRIVAL`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): дата доставки

**`SORTFROM`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): поштова скринька перша у полі "від кого" (поле `from`) .

**`SORTSUBJECT`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): Тема листа

**`SORTTO`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): поштова скринька перша у полі "кому" (поле `to`) .

**`SORTCC`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): поштова скринька перша у полі "копія" (поле `cc`) .

**`SORTSIZE`**(int)

Критерій сортування для [imap\_sort()](function.imap-sort.md): розмір повідомлення в байтах

**`TYPETEXT`**(int)

Первинний тип тіла: неформатований текст

**`TYPEMULTIPART`**(int)

Первинний тип тіла: кілька частин

**`TYPEMESSAGE`**(int)

Первинний тип тіла повідомлення: інкапсульоване повідомлення

**`TYPEAPPLICATION`**(int)

Первинний тип тіла повідомлення: дані програми

**`TYPEAUDIO`**(int)

Первинний тип тіла повідомлення: аудіо

**`TYPEIMAGE`**(int)

Первинний тип тіла повідомлення: статичне зображення

**`TYPEVIDEO`**(int)

Первинний тип тіла: відео

**`TYPEMODEL`**(int)

Первинний тип тіла: модель

**`TYPEOTHER`**(int)

Первинний тип тіла повідомлення: невідомо

**`ENC7BIT`**(int)

Кодування тіла повідомлення: 7-бітові дані в семантиці SMTP

**`ENC8BIT`**(int)

Кодування тіла повідомлення: 8-бітові дані в семантиці SMTP

**`ENCBINARY`**(int)

Кодування тіла повідомлення: 7-бітові двійкові дані

**`ENCBASE64`**(int)

Кодування тіла повідомлення: дані закодовані у base-64

**`ENCQUOTEDPRINTABLE`**(int)

Кодування тіла повідомлення: людино-читані 7-як-8 бітні дані

**`ENCOTHER`**(int)

Кодування тіла повідомлення: невідомо

**`IMAP_OPENTIMEOUT`**(int)

**`IMAP_READTIMEOUT`**(int)

**`IMAP_WRITETIMEOUT`**(int)

**`IMAP_CLOSETIMEOUT`**(int)

**`IMAP_GC_ELT`**(int)

Складальник сміття, очищає елементи кешу повідомлень.

**`IMAP_GC_ENV`**(int)

Складальник сміття, очищає обгортку та тіло повідомлення.

**`IMAP_GC_TEXTS`**(int)

Складальник сміття, очищає текст.
