# Monogdb
**Install**
建议还是使用yum安装,yum安装的不需要修改ulimit values
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/
安装简单，但是后面的设置和配置写的很多,主要是说ulimit，其实照着后面的改几个ulimit就行了，如果是yum安装，那么不需要改也行

建议不要自行安装，会出一堆问题，比如：
1)
/var/lib/mongo 找到配置文件，在里面找到dbpath，
然后：
sudo chown -R mongod:mongod /var/lib/mongo（dbpath）
2) /tmp 下有个 *.sock  这个也要修改，和上面一样
如果还报错的话，体现在无法打开mongodb服务，那么看一下输出日至，很有可能说 是/data/db文件没有（就是这个根目录下的），自己创建一个，再修改权限，再启动。


**查看使用的是upstart/systemd **

1）stat /proc/1/exe可以查看
或者
2）根据/usr/lib/systemd /usr/share/upstart /etc/init.d这3个目录是否存在来判断
注意由于systemd和upstart都向后兼容，因此一个系统中可能安装了多个初始化系统


**Use**
mongo --host 127.0.0.1:27017
具体指导见：https://blog.csdn.net/wen_3370/article/details/54236011
https://blog.csdn.net/weixin_43453386/article/details/83347385
