# Monogdb

1)
/var/lib/mongo 找到配置文件，在里面找到dbpath，
然后：
sudo chown -R mongod:mongod /var/lib/mongo（dbpath）
2) /tmp 下有个 *.sock  这个也要修改，和上面一样

如果还报错的话，体现在无法打开mongodb服务，那么看一下输出日至，很有可能说 是/data/db文件没有（就是这个根目录下的），自己创建一个，再修改权限，再启动。
