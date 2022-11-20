# 实体关系标注平台
# CMeKG_labelingPlatform
# CMeKG_labelingPlatform
本项目是用于对文本标注，直接生成对应文件进行下载
原项目有部分bug，且流程使用和搭建没有说明，所以进行一些完善和修复
0. 配置文件在config.py中， 需要修改数据库链接。创建数据表语句在models.py（最后一行）
1. 首先搭建本地的mysql数据库，创建对应的database，记录用户名密码端口的链接信息
2. 插入管理员数据。 insert into users values('admin', '111@qq.com', 'admin', '管理员');
3. 项目位flask编写，flask run 启动项目， 缺少的依赖包自己安装。
4. 启动成功后，浏览器打开 http://127.0.0.1:5000， admin 进行登陆。
5. 创建上传数据集， txt格式即可。
6. 分组管理中创建分组。
7. 任务管理中创建任务，成功后有标记页面， 点击进入。
8. 配置实体和关系的读取，这里前端有读取文件的bug，不过直接填入数据在文本框中即可（懒得修复）
9. 上面admin_en.txt是实体名称，换行符分割
10. 下面admin_re.json 是关系映射，一行一个关系， 通过空格分割，一个关系一行。（如：转移部位 疾病 部位）
11. 或者直接修改项目中的文件也可 static/labels/admin_re.json
