Командний рядок PHP у Microsoft Windows

-   [« Сборка из исходных кодов](install.windows.building.html)
    
-   [Apache 2.x в Microsoft Windows »](install.windows.apache2.html)
    
-   [PHP Manual](index.html)
    
-   [Установка в системах Windows](install.windows.html)
    
-   Командний рядок PHP у Microsoft Windows
    

## Командний рядок PHP у Microsoft Windows

Цей розділ містить примітки та підказки, які стосуються запуску PHP з командного рядка для Windows.

> **Зауваження**
> 
> Спочатку слід прочитати [шаги ручной установки](install.windows.manual.html)

Запуск PHP з командного рядка можна виконати без внесення будь-яких змін до Windows.

```
C:\php\php.exe -f "C:\PHP Scripts\script.php" -- -arg1 -arg2 -arg3
```

Але є кілька кроків, які допоможуть спростити цей процес. Деякі з цих кроків вже мали бути зроблені, але вони повторюються тут, щоб мати можливість надати повну покрокову послідовність.

> **Зауваження**
> 
> І PATH, і PATHEXT є важливими змінними, які спочатку існували у Windows, і слід подбати про те, щоб не перезаписувати жодну зі змінних, а лише додавати до них.

-   Додайте розташування файлу PHP (php.exe, php-win.exe або php-cli.exe залежно від вашої версії PHP і переваг відображення) в змінну оточення PATH. Докладніше про те, як додати каталог PHP до PATH, читайте в [соответствующей записи часто задаваемых вопросов](faq.installation.html#faq.installation.addtopath)
    
-   Додати розширення `.PHP` до змінної оточення PATHEXT. Це можна зробити одночасно із зміною змінної оточення PATH. Виконайте ті ж дії, що і в [ЧАВО](faq.installation.html#faq.installation.addtopath), але змініть змінну оточення PATHEXT, а не PATH.
    
    > **Зауваження**
    > 
    > Позиція, в яку ви поміщаєте `.PHP`, визначатиме, який скрипт чи програма виконуватиметься при збігу імен файлів. Наприклад, розміщення `.PHP` перед `.BAT` призведе до запуску вашого скрипта, а не пакетного файлу, якщо існує пакетний файл з тим самим ім'ям.
    
-   Зв'яжіть розширення `.PHP` із типом файлу. Це робиться за допомогою наступної команди:
    
    ```
    assoc .php=phpfile
    ```
    
-   Зв'яжіть тип файлу `phpfile` з відповідним файлом PHP, що виконується. Це робиться за допомогою наступної команди:
    
    ```
    ftype phpfile="C:\php\php.exe" -f "%1" -- %~2
    ```
    

Виконання цих кроків дозволить запускати скрипти PHP з будь-якого каталогу без необхідності вводити файл PHP або розширення, що виконується. `.PHP`, і всі параметри буде передано скрипту для обробки.

У наведеному нижче прикладі описано подробиці про деякі зміни в реєстрі, які можна зробити вручну.

**Приклад #1 Зміни у реєстрі**

```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Classes\.php]
@="phpfile"
"Content Type"="application/php"

[HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile]
@="PHP Script"
"EditFlags"=dword:00000000
"BrowserFlags"=dword:00000008
"AlwaysShowExt"=""

[HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\DefaultIcon]
@="C:\\php\\php-win.exe,0"

[HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\shell]
@="Open"

[HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\shell\Open]
@="&Open"

[HKEY_LOCAL_MACHINE\SOFTWARE\Classes\phpfile\shell\Open\command]
@="\"C:\\php\\php.exe\" -f \"%1\" -- %~2"
```

З цими змінами цю команду можна записати як:

```
"C:\PHP Scripts\script" -arg1 -arg2 -arg3
```

або, якщо ваш шлях `"C:\PHP Scripts"` знаходиться в змінному оточенні PATH:

```
script -arg1 -arg2 -arg3
```

> **Зауваження**
> 
> Є невелика проблема, якщо ви збираєтеся використовувати цю техніку і використовувати свої скрипти PHP як фільтр командного рядка, як у прикладі нижче:
> 
> ```
> dir | "C:\PHP Scripts\script" -arg1 -arg2 -arg3
> ```
> 
> або
> 
> ```
> dir | script -arg1 -arg2 -arg3
> ```
> 
> Ви можете виявити, що сценарій просто зависає і нічого не виводиться. Щоб це запрацювало, необхідно внести ще одну зміну до Реєстру.
> 
> ```
> Windows Registry Editor Version 5.00
> 
> [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\policies\Explorer]
> "InheritConsoleHandles"=dword:00000001
> ```
> 
> Додаткову інформацію щодо цієї проблеми можна знайти в цій [»  статье базы знаний Microsoft : 321788](http://support.microsoft.com/default.aspx?scid=kb;en-us;321788). У Windows 10 цей параметр змінено на протилежний, і стандартне встановлення Windows 10 підтримує успадковані дескриптори консолі. Це [»  сообщение на форуме Microsoft](https://social.msdn.microsoft.com/Forums/en-US/f19d740d-21c8-4dc2-a9ab-d5c0527e932b/nasty-file-association-regression-bug-in-windows-10-console?forum=windowssdk) надає пояснення.