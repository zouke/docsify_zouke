# 接口调用方法：
![](/static/upload/showdoc/20180827/4bc2fbb343dd221a426e23109616aff1.png)

# sign生成规则及步骤：
#### 示例（所有参数、参数值均为示例，开发人员参考格式即可）：
#### ①　第一步（获取到的请求参数并按照参数名ASCII码从小到大排序）：
    timestamp=1535335545
    source=app
    data={"agreement_type":1}
    私钥:ppk=#@%^&
    接口请求方式:method=POST/GET/... (转为大写)
    接口访问名:pathinfo=v1/user
	
#### ②　第二步（按规则拼接为字符串strA）：
    strA=POST&v1/user?data={"agreement_type":1}&source=1×tamp=1535335545
	
#### ③　第三步（生成sign）：
##### A. 使用MAC_SHA1算法对上述字符串进行加密
下面的示例为php的函数实现,android的HMAC_SHA1 算法实现可自行baidu

     $str=hash_hmac('sha1', $strA, $ppk);
	 
##### B.对加密串进行base64urlencode，防止签名串被特殊字符分割，导致验证无法通过
下面的示例为php的函数实现,android的base64urlencode算法实现可自行baidu

    $str=base64_encode($str);

####说明:
$ppk为：使用HMAC生成信息摘要时所使用的密钥