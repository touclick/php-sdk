# 点触验证码 PHP-SDK

#####[其他语言SDK以及JS API https://github.com/touclick/captcha-demo](https://github.com/touclick/captcha-demo)

##开发环境

* PHP环境(PHP 5 >= 5.2.0, PECL json >= 1.2.0, PHP 7)
* CURL扩展

## 文件说明

* activate/ 点触验证码公钥激活。请访问 activate/activate.html，并按照要求输入公钥和私钥，要求必须和 activate/check.php放在同一个目录下
* captcha-demo/ web项目调用示例
* captcha-php-sdk/ SDK源码

##公钥激活
	
`为了公钥能正常使用，请务必进行激活，如更换SDK，则需要使用新SDK的激活程序重新进行激活`

`激活过后，建议删除 activate/ 文件夹`

`请访问 activate/activate.html , 然后根据引导进行激活`

## 如何使用

1. 初始化验证码类

	```php
	/*$PUBKEY 、 $PRIKEY 从http://admin.touclick.com注册获取 */
	$PUBKEY = "";
	$PRIKEY = "";

	var touclick = new TouClick($PUBKEY,$PRIKEY);
	```

2. 二次验证

	```php
	$res = touclick->check($sid, $checkAddress, $token);
	//$res['code'] 的详细说明请看README.md
	if ($res) {
            var_dump ($res);
	} else {
            var_dump('验证成功');
	}	
	```

3. 运行

启动PHP服务器，访问 `captcha-demo/index.html` 就可体验

### 联系我们：

（客户服务）官Q1：<a href="https://touclick.com/?service=0" target="_blank">800161394</a> ，电话010-53608568

（技术支持）官Q1：<a target="_blank" href="http://shang.qq.com/wpa/qunwpa?idkey=eae024d881e951c69bb4bbb41d1af9be9f4b861eb86bf48e8f35cf27cc24d98e">205658675</a>
