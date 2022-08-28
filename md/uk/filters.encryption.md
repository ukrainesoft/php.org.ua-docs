Шифруючі фільтри

-   [« Компрессионные фильтры](filters.compression.html)
    
-   [Список поддерживаемых транспортных протоколов »](transports.html)
    
-   [PHP Manual](index.html)
    
-   [Список доступных фильтров](filters.html)
    
-   Шифруючі фільтри
    

## Шифруючі фільтри

Фільтри, що шифрують, дуже добре підходять для шифрування файлів і потоків.

## mcrypt. та mdecrypt.

**Увага**

Ця можливість була оголошена *застарілої*починаючи з PHP 7.1.0. Вкрай не рекомендується покладатися на цю можливість у майбутньому.

`mcrypt.*` і `mdecrypt.*` забезпечують симетричне шифрування та дешифрування за допомогою libmcrypt. Обидва набори фільтрів підтримують ті ж алгоритми, що й [модуль mcrypt](ref.mcrypt.html) у вигляді `mcrypt.ciphername`, де `ciphername` - це назва шифру, якби вона передавалася функції [mcrypt\_module\_open()](function.mcrypt-module-open.html). Також доступні такі п'ять параметрів:

**Параметри фільтра mcrypt**

| Параметр      | Обязателен? | По умолчанию                   | Пример значения                                                |
|---------------|-------------|--------------------------------|----------------------------------------------------------------|
| mode          | Ні          | cbc                            | cbc, cfb, ecb, nofb, ofb, stream                               |
| algorithmsdir | Ні          | iniget('mcrypt.algorithmsdir') | Шлях до модулів алгоритмів                                     |
| modesdir      | Ні          | iniget('mcrypt.modesdir')      | Шлях до модулів режимів                                        |
| верб          | Так         | N/A                            | Зазвичай 8, 16 або 32 байти бінарних даних. Залежить від шифру |
| key           | Так         | N/A                            | Зазвичай 8, 16 або 32 байти бінарних даних. Залежить від шифру |

**Приклад #1 Шифрування/розшифрування за допомогою Blowfish**

```php
<?php
// примем, что $key  уже сформирован
$iv_size = mcrypt_get_iv_size(MCRYPT_BLOWFISH, MCRYPT_MODE_CBC);
$iv = mcrypt_create_iv($iv_size, MCRYPT_DEV_URANDOM);
$fp = fopen('encrypted-file.enc', 'wb');
fwrite($fp, $iv);
$opts = array('mode'=>'cbc','iv'=>$iv, 'key'=>$key);
stream_filter_append($fp, 'mcrypt.blowfish', STREAM_FILTER_WRITE, $opts);
fwrite($fp, 'message to encrypt');
fclose($fp);

//расшифровка...
$fp = fopen('encrypted-file.enc', 'rb');
$iv = fread($fp, $iv_size = mcrypt_get_iv_size(MCRYPT_BLOWFISH, MCRYPT_MODE_CBC));
$opts = array('mode'=>'cbc','iv'=>$iv, 'key'=>$key)
stream_filter_append($fp, 'mdecrypt.blowfish', STREAM_FILTER_READ, $opts);
$data = rtrim(stream_get_contents($fp));//trims off null padding
fclose($fp);
echo $data;
?>
```

**Приклад #2 Шифрування файлу за допомогою AES-128 CBC з SHA256 HMAC**

```php
<?php
AES_CBC::encryptFile($password, "plaintext.txt", "encrypted.enc");
AES_CBC::decryptFile($password, "encrypted.enc", "decrypted.txt");

class AES_CBC
{
   protected static $KEY_SIZES = array('AES-128'=>16,'AES-192'=>24,'AES-256'=>32);
   protected static function key_size() { return self::$KEY_SIZES['AES-128']; } //default AES-128
   public static function encryptFile($password, $input_stream, $aes_filename){
      $iv_size = mcrypt_get_iv_size(MCRYPT_RIJNDAEL_128, MCRYPT_MODE_CBC);
      $fin = fopen($input_stream, "rb");
      $fc = fopen($aes_filename, "wb+");
      if (!empty($fin) && !empty($fc)) {
         fwrite($fc, str_repeat("_", 32) );//placeholder, SHA256 HMAC will go here later
         fwrite($fc, $hmac_salt = mcrypt_create_iv($iv_size, MCRYPT_DEV_URANDOM));
         fwrite($fc, $esalt = mcrypt_create_iv($iv_size, MCRYPT_DEV_URANDOM));
         fwrite($fc, $iv = mcrypt_create_iv($iv_size, MCRYPT_DEV_URANDOM));
         $ekey = hash_pbkdf2("sha256", $password, $esalt, $it=1000, self::key_size(), $raw=true);
         $opts = array('mode'=>'cbc', 'iv'=>$iv, 'key'=>$ekey);
         stream_filter_append($fc, 'mcrypt.rijndael-128', STREAM_FILTER_WRITE, $opts);
         $infilesize = 0;
         while (!feof($fin)) {
            $block = fread($fin, 8192);
            $infilesize+=strlen($block);
            fwrite($fc, $block);
         }
         $block_size = mcrypt_get_block_size(MCRYPT_RIJNDAEL_128, MCRYPT_MODE_CBC);
         $padding = $block_size - ($infilesize % $block_size);//$padding is a number from 1-16
         fwrite($fc, str_repeat(chr($padding), $padding) );//perform PKCS7 padding
         fclose($fin);
         fclose($fc);
         $hmac_raw = self::calculate_hmac_after_32bytes($password, $hmac_salt, $aes_filename);
         $fc = fopen($aes_filename, "rb+");
         fwrite($fc, $hmac_raw);//overwrite placeholder
         fclose($fc);
      }
   }
   public static function decryptFile($password, $aes_filename, $out_stream) {
      $iv_size = mcrypt_get_iv_size(MCRYPT_RIJNDAEL_128, MCRYPT_MODE_CBC);
      $hmac_raw = file_get_contents($aes_filename, false, NULL,  0, 32);
      $hmac_salt = file_get_contents($aes_filename, false, NULL, 32, $iv_size);
      $hmac_calc = self::calculate_hmac_after_32bytes($password, $hmac_salt, $aes_filename);
      $fc = fopen($aes_filename, "rb");
      $fout = fopen($out_stream, 'wb');
      if (!empty($fout) && !empty($fc) && self::hash_equals($hmac_raw,$hmac_calc)) {
         fread($fc, 32+$iv_size);//skip sha256 hmac and salt
         $esalt = fread($fc, $iv_size);
         $iv    = fread($fc, $iv_size);
         $ekey = hash_pbkdf2("sha256", $password, $esalt, $it=1000, self::key_size(), $raw=true);
         $opts = array('mode'=>'cbc', 'iv'=>$iv, 'key'=>$ekey);
         stream_filter_append($fc, 'mdecrypt.rijndael-128', STREAM_FILTER_READ, $opts);
         while (!feof($fc)) {
            $block = fread($fc, 8192);
            if (feof($fc)) {
               $padding = ord($block[strlen($block) - 1]);//assume PKCS7 padding
               $block = substr($block, 0, 0-$padding);
            }
            fwrite($fout, $block);
         }
         fclose($fout);
         fclose($fc);
      }
   }
   private static function hash_equals($str1, $str2) {
      if(strlen($str1) == strlen($str2)) {
         $res = $str1 ^ $str2;
         for($ret=0,$i = strlen($res) - 1; $i >= 0; $i--) $ret |= ord($res[$i]);
         return !$ret;
      }
      return false;
   }
   private static function calculate_hmac_after_32bytes($password, $hsalt, $filename) {
      static $init=0;
      $init or $init = stream_filter_register("user-filter.skipfirst32bytes", "FileSkip32Bytes");
      $stream = 'php://filter/read=user-filter.skipfirst32bytes/resource=' . $filename;
      $hkey = hash_pbkdf2("sha256", $password, $hsalt, $iterations=1000, 24, $raw=true);
      return hash_hmac_file('sha256', $stream, $hkey, $raw=true);
   }
}
class FileSkip32Bytes extends php_user_filter
{
   private $skipped=0;
   function filter($in, $out, &$consumed, $closing)  {
      while ($bucket = stream_bucket_make_writeable($in)) {
         $outlen = $bucket->datalen;
         if ($this->skipped<32){
            $outlen = min($bucket->datalen,32-$this->skipped);
            $bucket->data = substr($bucket->data, $outlen);
            $bucket->datalen = $bucket->datalen-$outlen;
            $this->skipped+=$outlen;
         }
         $consumed += $outlen;
         stream_bucket_append($out, $bucket);
      }
      return PSFS_PASS_ON;
   }
}
class AES_128_CBC extends AES_CBC {
   protected static function key_size() { return self::$KEY_SIZES['AES-128']; }
}
class AES_192_CBC extends AES_CBC {
   protected static function key_size() { return self::$KEY_SIZES['AES-192']; }
}
class AES_256_CBC extends AES_CBC {
   protected static function key_size() { return self::$KEY_SIZES['AES-256']; }
}
```