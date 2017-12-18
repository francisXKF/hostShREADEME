# 国内漫游数据业务相关脚本使用说明
### 1. autoMonitor
日常监控脚本，主要监控文件采集、文件批价、文件下发、主机空间  
[hostMonitor相关说明](https://github.com/francisXKF/hostShREADEME/blob/master/hostMonitor.md)
### 2. storageStatus
主机空间监控脚本，监控各主机设定挂载点的空间、各主机时间查看、各主机内存使用情况
[挂载点空间检查viewStorageStatus.sh](https://github.com/francisXKF/hostShREADEME/blob/master/viewStorageStatus.md)
### 3. fileUpCheck
文件上传监控脚本，主要监控各省分上传已采集文件数、未采集文件数
### 4. versionRelease
版本发布脚本，进行国内漫游数据业务各程序发版  
[versionRelease使用说明](https://github.com/francisXKF/test/blob/master/help.md)
### 5. demo_getbilltag
排重脚本，主要进行排重进程的停、启，状态查看等
### 6. fileStaSchedCronTab_produce
定时统计脚本（原实施使用），目前作为监测是否有统计进程，调用日报表脚本使用
### 7. demo_stat
定时统计脚本（上线使用），通过在本机定时调用该目录下脚本，执行各话单机统计脚本，完成日统计
