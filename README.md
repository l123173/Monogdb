# Monogdb

1)
/var/lib/mongo 找到配置文件，在里面找到dbpath，
然后：
sudo chown -R mongod:mongod /var/lib/mongo（dbpath）
2) /tmp 下有个 *.sock  这个也要修改，和上面一样
