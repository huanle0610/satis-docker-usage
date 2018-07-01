```bash
cd satis-server
docker-compose -f docker-compose.yml up -d
```

```bash
docker stop satis_server
```


```bash
$ curl -sS http://localhost:8080/api/dump
$ curl -sS http://localhost:8080/api/list
```

```bash
$ curl -sS -d'url=https://github.com/php-amqplib/php-amqplib' http://localhost:8080/api/add
$ curl -sS -d'url=https://github.com/yiisoft/yii2-app-advanced' http://localhost:8080/api/add

                                                                                      
  Your configuration file successfully updated! It's time to rebuild your repository  
                                                                                      

```


```bash
$ curl -sS -d'url=https://github.com/php-amqplib/php-amqplib' http://localhost:8080/api/build
Scanning packages
Reading composer.json of php-amqplib/php-amqplib (v2.7.2)
Importing tag v2.7.2 (2.7.2.0)
Reading composer.json of php-amqplib/php-amqplib (v2.7.1)
......
Selected php-amqplib/php-amqplib (v2.2.1)
Selected php-amqplib/php-amqplib (v2.2.0)
Selected php-amqplib/php-amqplib (v2.1.0)
wrote packages to /etc/satis/output/include/all$d3576dd389b3699ff597dadfdc165ce2c43b10fd.json
Writing packages.json
Pruning include directories
Writing web view
Exit code: 0
$ curl -sS -d'url=https://github.com/yiisoft/yii2-app-advanced' http://localhost:8080/api/build
```


```bash
[amtf@amtf-s3 self-composer-repo]$ curl -sS http://localhost:8080/api/list
PACKAGE NAME                            PACKAGE URL                                             LAST BUILT
php-amqplib/php-amqplib                 https://github.com/php-amqplib/php-amqplib              Sun Jul  1 03:47:21 2018
```


```bash
curl -sS http://localhost:8080/api/build-all
```