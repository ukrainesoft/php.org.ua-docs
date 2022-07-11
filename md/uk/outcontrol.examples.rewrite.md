- [« Базове використання](outcontrol.examples.basic.md)
- [Функції контролю виведення»](ref.outcontrol.md)

- [PHP Manual](index.md)
- [Приклади](outcontrol.examples.md)
- Використання перезапису виводу

## Використання перезапису виводу

Починаючи з PHP 7.1.0,
[output_add_rewrite_var()](function.output-add-rewrite-var.md) та
[output_reset_rewrite_vars()](function.output-reset-rewrite-vars.md)
використовують окремий буфер виводу, тобто не використовують буфер виводу
[прозорої підтримки sid](session.configuration.md#ini.session.use-trans-sid).

**Приклад #1 Приклад перезапису виведення**

` <?php// Цей код працює с PHP 7.1.0, 7.0.10, 5.6.25 і вище.// HTTP_HOST - цільовий хост за замовчуванням. Задамо самі, щоб код прикладу заробив.$_SERVER['HTTP_HOST'] = 'php.net';// Перезаписувач висновку перезаписує тільки "form". Додамо a=href.// Теги повинні вказуватися як tag_name=url_attr, є є img=src,iframe=src//Між настройками пробіли|неприпустимі.// Тег 'url_rewriter.tags','a=href,form=');var_dump(ini_get('url_rewriter.tags'));// Це додано в URL і "form"output_add_rewrite_var('test', 'u ><a href="//php.net/index.php?bug=1234">bug1234</a><form action="https://php.net/?bug=1234&edit=1" action="post "> <input type="text" name="title" /></form>`

Результат виконання цього прикладу:

<a href="//php.net/?bug=1234&test=value">bug1234</a>
<form action="https://php.net/?bug=1234&edit=1" method="post"><input type="hidden" name="test" value="value" />
<input type="text" name="title" />
</form>

З PHP 7.1.0 функції перезапису виводу мають свої власні
INI-налаштування.
[url_rewriter.tags](outcontrol.configuration.md#ini.url-rewriter.tags)
і
[url_rewriter.hosts](outcontrol.configuration.md#ini.url-rewriter.hosts).
