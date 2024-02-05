---
navigation:
  - xdiff.resources.md: « Типи ресурсів
  - ref.xdiff.md: Функції xdiff »
  - index.md: PHP Manual
  - book.xdiff.md: xdiff
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`XDIFF_PATCH_NORMAL`**(int)

Цей прапор означає, що функції [xdiff\_string\_patch()](function.xdiff-string-patch.md) і [xdiff\_file\_patch()](function.xdiff-file-patch.md) повинні створювати результат шляхом застосування патча до оригінального контенту, таким чином створюючи нову версію файлу. Це є стандартною поведінкою.

**`XDIFF_PATCH_REVERSE`**(int)

Цей прапор означає, що функції [xdiff\_string\_patch()](function.xdiff-string-patch.md) і [xdiff\_file\_patch()](function.xdiff-file-patch.md) повинні створювати результат шляхом відкату патчу з отриманого нового контенту, таким чином відновлюючи оригінальний контент.
