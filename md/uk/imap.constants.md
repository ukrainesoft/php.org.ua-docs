---
navigation:
  - imap.resources.html: « Типи ресурсів
  - ref.imap.html: Функции IMAP »
  - index.html: PHP Manual
  - book.imap.html: IMAP
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`NIL`** (int)

Оголошена застарілою починаючи з PHP 8.1.0.

**`OP_DEBUG`** (int)

**`OP_READONLY`** (int)

Відкрити поштову скриньку тільки для читання

**`OP_ANONYMOUS`** (int)

Не використовуйте оновлення .newsrc для новин (тільки для NNTP)

**`OP_SHORTCACHE`** (int)

**`OP_SILENT`** (int)

**`OP_PROTOTYPE`** (int)

**`OP_HALFOPEN`** (int)

Для IMAP та NNTP імен, відкрити з'єднання, але не відкривати поштову скриньку.

**`OP_EXPUNGE`** (int)

**`OP_SECURE`** (int)

**`CL_EXPUNGE`** (int)

Не надаючи жодних попереджень прати повідомлення перед тим, як закрити під час виклику [imapclose()](function.imap-close.html)

**`FT_UID`** (int)

Параметром є UID

**`FT_PEEK`** (int)

Не встановлювати прапор Seen, якщо до цього він ще не встановлений

**`FT_NOT`** (int)

**`FT_INTERNAL`** (int)

Повертається рядок у внутрішньому форматі. Не буде канонізована до виду CRLF.

**`FT_PREFETCHTEXT`** (int)

**`ST_UID`** (int)

Послідовність аргументів містить ідентифікатори UID замість послідовності номерів

**`ST_SILENT`** (int)

**`ST_SET`** (int)

**`CP_UID`** (int)

порядкові номери, що містять ідентифікатори UID

**`CP_MOVE`** (int)

Видалити повідомлення з поточної поштової скриньки після копіювання за допомогою [imapmailcopy()](function.imap-mail-copy.html)

**`SE_UID`** (int)

Повертати ідентифікатори UID замість порядкових номерів

**`SE_FREE`** (int)

**`SE_NOPREFETCH`** (int)

Не виконувати передвиборку знайдених повідомлень

**`SO_FREE`** (int)

**`SO_NOSERVER`** (int)

**`SA_MESSAGES`** (int)

**`SA_RECENT`** (int)

**`SA_UNSEEN`** (int)

**`SA_UIDNEXT`** (int)

**`SA_UIDVALIDITY`** (int)

**`SA_ALL`** (int)

**`LATT_NOINFERIORS`** (int)

Ця поштова скринька не має "нащадків". (Поштові скриньки за цим відсутні)

**`LATT_NOSELECT`** (int)

Це лише контейнер, а не поштова скринька. Ви не можете його відкрити.

**`LATT_MARKED`** (int)

Ця поштова скринька позначена. Використовується лише UW-IMAPD.

**`LATT_UNMARKED`** (int)

Ця поштова скринька не помічена. Використовується лише з UW-IMAPD.

**`LATT_REFERRAL`** (int)

Цей контейнер має напрямки (referral) на віддалену поштову скриньку.

**`LATT_HASCHILDREN`** (int)

Ця поштова скринька має підпорядковані (inferiors).

**`LATT_HASNOCHILDREN`** (int)

Ця поштова скринька не має підлеглі (inferiors).

**`SORTDATE`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): дата написання

**`SORTARRIVAL`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): дата доставки

**`SORTFROM`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): поштова скринька перша у полі "від кого" (поле `from`

**`SORTSUBJECT`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): Тема листа

**`SORTTO`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): поштова скринька перша у полі "кому" (поле `to`

**`SORTCC`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): поштова скринька перша у полі "копія" (поле `cc`

**`SORTSIZE`** (int)

Критерій сортування для [imapsort()](function.imap-sort.html): розмір повідомлення в байтах

**`TYPETEXT`** (int)

Первинний тип тіла: неформатований текст

**`TYPEMULTIPART`** (int)

Первинний тип тіла: кілька частин

**`TYPEMESSAGE`** (int)

Первинний тип тіла повідомлення: інкапсульоване повідомлення

**`TYPEAPPLICATION`** (int)

Первинний тип тіла повідомлення: дані програми

**`TYPEAUDIO`** (int)

Первинний тип тіла повідомлення: аудіо

**`TYPEIMAGE`** (int)

Первинний тип тіла повідомлення: статичне зображення

**`TYPEVIDEO`** (int)

Первинний тип тіла: відео

**`TYPEMODEL`** (int)

Первинний тип тіла: модель

**`TYPEOTHER`** (int)

Первинний тип тіла повідомлення: невідомо

**`ENC7BIT`** (int)

Кодування тіла повідомлення: 7-бітові дані в семантиці SMTP

**`ENC8BIT`** (int)

Кодування тіла повідомлення: 8-бітові дані в семантиці SMTP

**`ENCBINARY`** (int)

Кодування тіла повідомлення: 7-бітові двійкові дані

**`ENCBASE64`** (int)

Кодування тіла повідомлення: дані закодовані у base-64

**`ENCQUOTEDPRINTABLE`** (int)

Кодування тіла повідомлення: людино-читані 7-як-8 бітні дані

**`ENCOTHER`** (int)

Кодування тіла повідомлення: невідомо

**`IMAP_OPENTIMEOUT`** (int)

**`IMAP_READTIMEOUT`** (int)

**`IMAP_WRITETIMEOUT`** (int)

**`IMAP_CLOSETIMEOUT`** (int)

**`IMAP_GC_ELT`** (int)

Складальник сміття, очищає елементи кешу повідомлень.

**`IMAP_GC_ENV`** (int)

Складальник сміття, очищає обгортку та тіло повідомлення.

**`IMAP_GC_TEXTS`** (int)

Складальник сміття, очищає текст.
