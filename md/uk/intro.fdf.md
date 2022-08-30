Вступ

-   [« FDF](book.fdf.html)
    
-   [Встановлення та налаштування »](fdf.setup.html)
    
-   [PHP Manual](index.html)
    
-   [FDF](book.fdf.html)
    
-   Вступ
    

# Вступ

Формат даних форм (FDF) – це формат для обробки форм у документах PDF. Докладніше цей формат описаний у документації на сайті [» http://www.adobe.com/devnet/acrobat/fdftoolkit.html](http://www.adobe.com/devnet/acrobat/fdftoolkit.html)

Головна ідея FDF схожа на форми HTML. Відмінність тільки у форматі передачі даних на сервер після натискання кнопки "Надіслати" (якраз про це і FDF) та форматі самої форми (а це PDF). Обробка даних форми - це з можливостей, наданих функціями fdf. Інша можливість – можна автоматично заповнити існуючу форму даними. У цьому випадку ми можемо створити документ FDF ([fdfcreate()](function.fdf-create.html)), встановити значення для кожного поля введення ([fdfsetvalue()](function.fdf-set-value.html)) та зв'язати його з формою PDF ([fdfsetfile()](function.fdf-set-file.html)). У результаті вона буде відправлена ​​браузеру з Mime-типом `application/vnd.fdf`. Плагін "Acrobat reader" у вашому браузері впізнає Mime-тип, прочитає пов'язану форму PDF та заповнить її даними з документа FDF.

Якщо ви подивитеся на документ FDF у простому текстовому редакторі, ви побачите каталог об'єктів з ім'ям `FDF`. Такий об'єкт може містити набір таких елементів, як `Fields` `F` `Status` і т.д. Найчастіше використовується запис - це `Fields`, яка містить список полів введення, та `F`, яка містить ім'я PDF-файлу, для якого призначені дані. Ці записи називаються у документації PDF як /F-Key або /Status-Key. Зміна цих записів виконується такими функціями як [fdfsetfile()](function.fdf-set-file.html) і [fdfsetstatus()](function.fdf-set-status.html). Поля модифікуються функціями [fdfsetvalue()](function.fdf-set-value.html) [fdfsetopt()](function.fdf-set-opt.html) і т.д.