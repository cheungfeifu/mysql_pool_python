# mysql_pool_python
python数据库连接池

使用方式：
from mysql_pool import Mysql_Pool
# 在连接池获取数据库连接
archive = Mysql_Pool()

#正常连接，游标
conn = archive.pool.connection()
cursor = conn.cursor()
#关闭连接并非和数据库关闭连接，而是把连接归还到数据库连接池里，避免每次都需要和数据库创建链接
conn.close()
