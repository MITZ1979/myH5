### tp5创建绑定后台模板入口文件admin.php(企业级网站)

``` 1.Composer 下载tp5框架
    composer create-porject topthink/think=5.0.* tp5 --prefer-dist    --创建企业项目tp5
    
    2.在命令行下创建admin模块
    php think build --model admin
    
    3.启用admin模块后台模板入口文件
    1）在public文件夹中copy index.php 为admin.php
    2) 将application 中的入口自动绑定模块改为true
    'auto_bind_module'       => true,
```
