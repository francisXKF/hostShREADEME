# 使用范围：
  该脚本主要实现了
  1. 从远程主机获取待发版程序到当前主机；
  2. 备份待发版程序目标主机上对应程序；
  3. 将待发版程序上传到目标主机指定目录下并赋予可执行权限（777）
# 脚本说明：
  * versionReleaseMain.py：主函数，通过运行该函数进行相应程序的发布
  * ./models/*Release.py：相应程序处理函数，每个程序对应一个Release.py函数，对于*.so程序
  * ./programPath/*：相应程序目标主机发版路径
  * newVersionProgramInfo：待发版程序当前主机路径信息
  * ./versionProgram/*：待发版程序存放位置，历史发版程序存在于相应date目录下
  * ./util/*：工具函数，主要包含ftp、pexpect、自定义exception等
# 使用用例：（以发布moloadshm.so为例）
  1. 进入./models目录，查看是否存在moloadshmsoRelease.py，若不存在，执行2，若已存在，执行4
  2. 执行cp ftpcolRelease.py moloadshmsoRelease.py
  3. 打开moloadshmsoRelease.py，将ftpcol替换为moloadshm.so，并检查其他参数是否需要修改（当前设置不远程获取待待发版程序，待发版程序直接上传到当前主机待发版程序存放位置）
  4. 进入./programPath目录，查看是否存在moloadshm.so_path，若不存在，执行5，若已存在，执行7
  5. 执行cp ftpcol_path moloadshm.so_path
  6. 打开moloadshm.so_path，按目标主机ip 用户名 密码 目标主机程序路径 目标主机程序备份路径 当前主机待发版程序路径顺序插入记录
  7. 确认moloadshm.so_path中相应信息正确性
  8. 执行versionReleaseMain.py，按提示输入相应程序名，若备份失败，可选择不备份或终止发布异常退出
# 常见问题：
  1. newVersionProgramInfo说明：各字段的意义为：待发版程序远程主机ip 远程主机用户名 远程主机密码 远程主机待发版程序路径 当前主机待发版程序存放位置
  2. 备份失败：目标主机上没有相应程序，或者目标主机上没有对应备份目录
