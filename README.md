# taobao-area-php
根据淘宝国家省市区，自动生成CSV和SQL文件

# 说明

>注意：当前目录下权限必须可写可创建文件夹和文件


执行 `index.php` 程序自动建立 `tmp`目录 ,下载`淘宝省市区js`文件存储为`taobao-area.js`，根据`taobao-area.js`文件 自动生成 `area.csv`和`area.sql`文件，这2个文件 就是你需要的 淘宝全套国家省市区数据


如果你不需要国家数据，把`index.php`中的`$c->setIsCountry(true);`改为`$c->setIsCountry(false);`，重新执行程序就是不包含国家数据的 淘宝全套省市区数据


# csv 使用说明

文件编码为 `UTF-8`格式，不能直接用Excel格式打开，需要用Excel中的`数据导入`功能;步骤如下：

以 Excel 2016 为例

 - 打开`数据`选项卡
 - 在界面中，选择 `从文本`
 - 在弹出的界面中选择 `area.csv`文件，点击确定
 - 会弹出一个 警告 `固定宽度字体 宋体 不存在` ，直接点击 确定  忽略 这个提示
 - 在会话中，选中 `分隔符号`，文件原始格式`Unicode(UTF-8)`,点击 下一步
 - 分隔符选择 `制表符`,点击 下一步
 - 列数据格式 修改，先选择 `ID` 这列，然后 选择 `文本` 格式，再 选择 `上级ID`这列，然后 选择 `文本` 格式，最后点击 完成
 - 最后 直接点击  确定
 
# sql 说明
文件编码为 `UTF-8`格式

会自动创建 2张表 `area`和`area_ext`，其他请看SQL 文件# taobao-area
