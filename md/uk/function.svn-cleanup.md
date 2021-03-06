- [« svn_checkout](function.svn-checkout.md)
- [svn_client_version »](function.svn-client-version.md)

- [PHP Manual](index.md)
- [Функції SVN](ref.svn.md)
- рекурсивно очищає робочу копію директорії, завершує незакінчені
операції та знімає блокування

# svn_cleanup

(PECL svn \>= 0.1.0)

svn_cleanup - Рекурсивно очищає робочу копію директорії, завершує
незакінчені операції та знімає блокування

### Опис

**svn_cleanup**(string `$workingdir`): bool

Рекурсивно очищає робочу копію директорії `workingdir`, завершує
будь-які незакінчені операції та знімає блокування з робочої копії.
Використовуйте, коли необхідно відновити роботу недоступною робочою
копії.

### Список параметрів

`workingdir`
Шлях до локальної робочої копії для чищення.

> **Примітка**: Відносні шляхи будуть обчислені, наче поточна
> робоча директорія була домашньою папкою самого PHP. Щоб
> використовувати робочу директорію скрипта, що викликає, використовуйте
> [realpath()](function.realpath.md) або dirname(\_\_FILE\_\_).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад**

Цей приклад показує, як очистити робочу копію в директорії help-me:

`<?phpsvn_cleanup(realpath('help-me'));'> `

У зв'язку з дивною поведінкою відносних шляхів у SVN, необхідний
виклик функції [realpath()](function.realpath.md).

### Примітки

**Увага**

Ця функція є ЕКСПЕРИМЕНТАЛЬНОЮ. Поведінка цієї функції, її ім'я
і документація, що відноситься до неї, можуть змінитися в наступних версіях
PHP без попередження. Використовуйте цю функцію на свій страх та ризик.

### Дивіться також

- **update()**
- [»  SVN-документація з svn cleanup](http://svnbook.red-bean.com/en/1.2/svn.ref.svn.c.cleanup.md)
