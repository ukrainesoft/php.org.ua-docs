- [«Зумовлені константи](enchant.constants.md)
- [Функції Enchant »](ref.enchant.md)

- [PHP Manual](index.md)
- [Enchant](book.enchant.md)
- Приклади

# Приклади

**Приклад #1 Приклад використання Enchant**

` <?php$tag = 'en_US';$r = enchant_broker_init();$bprovides = enchant_broker_describe($r);echo "Доступні наступні бекенди:
";print_r($bprovides);$dicts==enchant_broker_list_dicts($r);print_r($dicts);if(enchant_broker_dict_exists($r,$tag)) {    $d = enchant_broker_request| enchant_dict_describe($d);   echo "словник $tag:
";    $wordcorrect = enchant_dict_check($d, "soong");    print_r($dprovides);    if (!$wordcorrect) {        $suggs = enchant_dict_suggest($d, "soong");        echo "Предложения для 'soong':" ;   print_r($suggs);    }   enchant_broker_free_dict($d);}else {}enchant_broker_free($r);?> `
