第一步：scrapy生成project: 

进入Terminal输入： scrapy startproject 项目名称 

如：scrapy startproject jdspider

然后创建一个蜘蛛名称：

cd jdspider 
scrapy genspider jd jd.com


第二步：进入jd.py文件：最后修改为：print response.body

第三步：进入settings.py  修改USER_AGENT 如：USER_AGENT = 'Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:55.0) Gecko/20100101 Firefox/55.0'


运行文件方法：在当前目录下（jdspider同目录下）：DOS命令运行： scrapy crawl jd或在当前目录下创建一个main.py的文件：
main.py内容为：

from scrapy import cmdline
cmdline.execute('scrapy crawl jd'.split())

然后设置一个运行jd.py文件时关联运行main.py文件
