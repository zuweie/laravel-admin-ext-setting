# Zuweie Settings 

### Zuweie Setting 是一个laravel-admin后台配置功能。
### 项目背景
- 因为经常在各个项目里面需要使用后台配置，为了不重复编码，把配置做成一个laravel-admin的插件，方便在各个项目使用。找了一堆的settings的模块。一个都没有后台界面，让管理员怎么用～～让管理员怎么用～～让管理员怎么用～～
- 本项目使用数据库作固化，cache做加速。

### 安装
- composer require zuweie/settings

- 执行以下命令
```
php artisan vendor:publish --provider="Zuweie\Setting\SettingServiceProvider"
```
```
php artisan migrate
```
- 若是在publish的过程中没有发生文件的拷贝，请将Zuweie\Setting\SettingServiceProvider注册到 /config/app.php中。
再进行publish和migrate。

- 安装成功后打开连接http://yourhost/admin/setting?tag=xxx, 将会出现以下页面：
![settings](http://cdn.qiniu.midea.bankoo.co/Snip20190818_1.png)

### 使用
#### 写数据
- 打开地址：http://yourhost/admin/setting?tags=xxx, 传入参数tags，则显示当前tags的配置。例如tags=language_zh,打开language_zh的配置。若tags参数为空则返回全部的配置。

- 在配置列表添加你想要的配置。

#### 读数据
- use Zuweie\Setting\Settings
```
   
```


### 完了
