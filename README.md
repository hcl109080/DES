# DES 加解密

## 安装

- composer require hcl109080/DES

## 使用

- 使用 DES-CBC 加解密

  ```php
  	$key = '33key123456';
  
      $iv = 'iv12345p';
  	
      $des = new AppService($key, 'DES-CBC', AppService::OUTPUT_BASE64, $iv);
  	
      echo $base64Sign = $des->encrypt('Hello DES CBC');	// 加密
  
      echo "\n";
  
      echo($des->decrypt($base64Sign)); 	// 解密
  ```

- 使用 DES ECB 加解密

  ```php
  	$key = '33key123456';
  
      $iv = 'iv12345p';
      
      $des = new AppService($key, 'DES-ECB', AppService::OUTPUT_HEX);
      
      echo $base64Sign = $des->encrypt('Hello DES ECB'); // 加密
      
      echo "\n";
      
      echo $des->decrypt($base64Sign); // 解密
  ```