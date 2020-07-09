# -  
＃此文件是TrinityCore项目的一部分。请参阅作者文件以获取版权信息
＃
＃此文件是免费软件；作为一个特殊的例外，作者给出了
＃无限制地复制和/或分发它，无论有无
＃修改，只要保留此通知即可。
＃
＃分发此程序是希望它会有用，但是
＃在法律允许的范围内，不作任何担保；甚至没有
＃暗示对特定目的的适销性或适用性的保证。

如果（不是 MYSQL_FOUND）
  消息（FATAL_ERROR  “在您的系统上未找到MySQL，但需要构建服务器！”）
endif（）

add_library（MySQL的STATIC  IMPORTED  GLOBAL）

set_target_properties（mysql
  性质
    IMPORTED_LOCATION
      “ $ {MYSQL_LIBRARY} ”
    INTERFACE_INCLUDE_DIRECTORIES
      “ $ {MYSQL_INCLUDE_DIR} ”）
