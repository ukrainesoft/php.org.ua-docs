---
navigation:
  - inotify.resources.md: « Типи ресурсів
  - ref.inotify.md: Функції Inotify »
  - index.md: PHP Manual
  - book.inotify.md: Inotify
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**Константи Inotify використовуються функцією [inotify\_add\_watch()](function.inotify-add-watch.md) та/або повертаються [inotify\_read()](function.inotify-read.md)**

**`IN_ACCESS`**(int)

До файлу здійснено доступ (читання) (\*

**`IN_MODIFY`**(int)

Файл було змінено (\*

**`IN_ATTRIB`**(int)

Змінені метадані (такі як permissions, mtime і т.д.) (\*

**`IN_CLOSE_WRITE`**(int)

Файл, відкритий для запису, був закритий (\*

**`IN_CLOSE_NOWRITE`**(int)

Файл, недоступний для запису, був закритий (\*

**`IN_OPEN`**(int)

Файл було відкрито (\*

**`IN_MOVED_TO`**(int)

Файл переміщений у вказану директорію (\*

**`IN_MOVED_FROM`**(int)

Файл переміщений із зазначеної директорії (\*

**`IN_CREATE`**(int)

Файл або директорія створено у зазначеній директорії (\*

**`IN_DELETE`**(int)

Файл або директорія видалена із зазначеної директорії (\*

**`IN_DELETE_SELF`**(int)

Вказаний файл або каталог видалено.

**`IN_MOVE_SELF`**(int)

Вказаний файл або директорія переміщені.

**`IN_CLOSE`**(int)

Еквівалентно IN\_CLOSE\_WRITE | IN\_CLOSE\_NOWRITE.

**`IN_MOVE`**(int)

Еквівалентно IN\_MOVED\_FROM | IN\_MOVED\_TO.

**`IN_ALL_EVENTS`**(int)

Бітова маска зазначених вище констант.

**`IN_UNMOUNT`**(int)

Файлова система, що містить файл, була розмонтована.

**`IN_Q_OVERFLOW`**(int)

Черга подій переповнена (wd (дескриптор спостереження) дорівнює -1 для цієї події).

**`IN_IGNORED`**(int)

Спостереження було вимкнено вручну (пояснюється [inotify\_rm\_watch()](function.inotify-rm-watch.md)) або через відсутність файлу або через розмонтування файлової системи.

**`IN_ISDIR`**(int)

Об'єктом події є директорія.

**`IN_ONLYDIR`**(int)

Використовувати лише зазначену директорію як кінцевий шлях (починаючи з Linux 2.6.15).

**`IN_DONT_FOLLOW`**(int)

Не розіменовувати шлях, якщо це символічне посилання (починаючи з Linux 2.6.15).

**`IN_MASK_ADD`**(int)

Додати події до маски подій для цього шляху, якщо вона вже існує (замість заміщення маски).

**`IN_ONESHOT`**(int)

Відстежувати шлях для однієї події, потім видалити його зі списку спостереження.

> **Зауваження**: Події, що позначені зірочкою (\*), можуть відбуватися з файлами в спостережуваних директоріях.
