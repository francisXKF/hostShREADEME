### 主机空间查看脚本
#### 功能
检查各主机指定目录的空间
#### 方法
* 使用`shell+expect`
* 通过`expect`自动填充密码
* 通过`bash shell`对结果格式化
#### 使用文件说明
* `viewStorageStatus.sh` 空间监控脚本
* `host_info` 主机信息文件：主机IP、用户名、密码、待监控挂载点
* `storage_info_temp` 空间检查日志(未格式化)，默认删除
* `storage_info_mid` 空间检查日志(初步格式化)，默认删除
* `storage_info` 空间检查日志(格式化)，默认先清空再写入
#### 使用
1. 配置`host_info` 
2. 修改`viewStorageStatus.sh`中绝对路径
3. 执行`viewStorageStatus.sh`
4. 查看`storage_info` 
