
以后再详写

//注意在官方请求实例下加命名空间
//appkey,secretKey 去自己的项目/config/app.php里加配置，这里就不一一说明了

$c = new \TaoKe\TopClient;
$c->appkey = '******';
$c->secretKey = '********';
$req = new \TaoKe\Request\TbkUatmFavoritesGetRequest;
$req->setPageNo("1");
$req->setPageSize("20");
$req->setFields("favorites_title,favorites_id,type");
$req->setType("1");
$resp = $c->execute($req);
return $resp;