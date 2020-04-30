# awstips
awstips
如何一次导出多个账号下的用户资源清单？
 
背景：用户有10个账号，全部账号都挂在 aws organizations下管理。
每天的资源都在发生变化，用户运维的需求能导出“全部账号”下的关键资源清单（如EC2，RDS，ELB等），导出后格式为csv或json，便于整理和查看。
尝试用过 AWS Resource Groups导出资源，发现只能导出当前账号下的资源清单，无法一次导出多个账号的；
 
解决方法： 利用对AWS资源的TAG标签 + Cost Explorer 功能，实现一次性多个账号下的用户资源清单（近乎实时）；
 
操作步骤：
1）登陆《付款账号》。因为有账单整合，那就有了payer account，payer account的账单中的月报或详单中有所有（linked accounts）的使用的服务（资源）的信息了。因为全部账号都挂在 aws organizations下管理，有一个付款账户，登陆它。
 
2）打开《Cost Explorer 》功能，如下图示。
 
 
 
3）点击左侧的《Cost Explorer 》，进入界面如下。
 
 
4）开始定制查询范围，比如：我们导出昨天的，付款账号关联的全部AWS账号中， EC2虚机的清单，界面如下：
 
提示：TAG在这里选取：
 
提示：可以限定更多的范围，比如具体关联的账号或区域等信息，导出的资源清单更为准确。
 
 
4）点击《Download CSV》下载清单，用Excel表打开，界面如下：
 
 
5）这个格式不是我们想要的，使用Excel表的行列转换功能，重新排版。
 
 
 
 
更多行列转换教程看这里：https://support.office.com/zh-cn/article/%E5%B0%86%E6%95%B0%E6%8D%AE%E4%BB%8E%E8%A1%8C%E8%BD%AC%E7%BD%AE%E5%88%B0%E5%88%97%EF%BC%8C%E6%88%96%E5%B0%86%E6%95%B0%E6%8D%AE%E4%BB%8E%E5%88%97%E8%BD%AC%E7%BD%AE%E5%88%B0%E8%A1%8C-3419f2e3-beab-4318-aae5-d0f862209744#ID0EAADAAA=Windows
 
6）见证奇迹的时候，重新排版成功。
 


7）如果在界面中找不到某个TAG，很大可能是TAG没有在费用中心开启，请打开《Cost Allocation Tags》开启， 24小时生效后再来尝试。
 
