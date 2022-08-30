Обумовлені константи

-   [« Типы ресурсов](xdiff.resources.html)
    
-   [Функції xdiff »](ref.xdiff.html)
    
-   [PHP Manual](index.html)
    
-   [xdiff](book.xdiff.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`XDIFF_PATCH_NORMAL`** (int)

Цей прапор означає, що функції [xdiffstringpatch()](function.xdiff-string-patch.html) і [xdifffilepatch()](function.xdiff-file-patch.html) повинні створювати результат шляхом застосування патча до оригінального контенту, таким чином створюючи нову версію файлу. Це є стандартною поведінкою.

**`XDIFF_PATCH_REVERSE`** (int)

Цей прапор означає, що функції [xdiffstringpatch()](function.xdiff-string-patch.html) і [xdifffilepatch()](function.xdiff-file-patch.html) повинні створювати результат шляхом відкату патчу з отриманого нового контенту, таким чином відновлюючи оригінальний контент.