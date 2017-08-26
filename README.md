# yii2

cd /var/www/html

wget https://github.com/yiisoft/yii2/releases/download/2.0.12/yii-basic-app-2.0.12.tgz

cd yii2

php yii serve

http://localhost:8080/

## rutas

editamos /controllers/SiteController.php

y añadimos dos funciones

public function actionClientes(){
  return "<h5> <small>Hola Mundo</small></h5>";
}

public function actionCliente($id){
  return "<h5> <small>Hola Mundo</small></h5>".$id;
}

editamos /config/web.php

'urlManager' => [
    'enablePrettyUrl' => true,
    'showScriptName' => false,
    'rules' => [
      'clientes'=>'site/clientes',
      'clientes/<id:\d+>'=>'site/cliente'
    ],
],
