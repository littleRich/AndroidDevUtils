##Android开发之常用工具类
****
为了方便代码重复利用，已大致分类成各个功能模块，其目录如下所示：
>- **APP相关→[AppUtils.java][app.java]**
>  - 安装APP
>  - 卸载指定包名的APP
>  - 获取当前APP的包名
>  - 获取所有已安装APP信息
>  - 根据包名判断APK是否已安装
>  - 打开指定包名的APP
>  - 打开指定包名的App应用信息界面
>  - 可用来做APP信息分享
>  - 判断当前APP处于前台还是后台
>  
> - **常量相关→[ConstUtils.java][const.java]**
>  - 存储相关常量
>  - 时间相关常量
>  - 正则相关常量

> - **转换相关→[ConvertUtils.java][convert.java]→[Test][convert.test]**
>  - 每1个byte转为2个hex字符 *bytes2HexString*
>  - 每2个hex字符转为1个byte *hexString2Bytes*
>  - charArr转byteArr *chars2Bytes*
>  - byteArr转charArr *bytes2Chars*

> - **设备相关→[DeviceUtils.java][device.java]** 
>  - 获取设备MAC地址 *getMacAddress*
>  - 获取设备厂商，如Xiaomi *getManufacturer*
>  - 获取设备型号，如MI2SC *getModel*

> - **编码解码相关→[EncodeUtils.java][encode.java]→[Test][encode.test]**
>  - URL编码 *urlEncode*
>  - URL解码 *urlDecode*
>  - Base64编码 *base64Encode* *base64Encode2String*
>  - Base64解码 *base64Decode*
>  - Base64URL安全编码 *base64UrlSafeEncode*
>  - Html编码 *htmlEncode*
>  - Html解码 *htmlDecode*

> - **数字指纹相关**
>  - 。。。

> - **加解密相关**
>  - 。。。

> - **文件相关→[FileUtils.java][file.java]→[Test][file.test]**
>  - 根据文件路径获取文件 *getFileByPath*
>  - 判断文件是否存在 *isFileExists*
>  - 判断是否是目录 *isDir*
>  - 判断是否是文件 *isFile*
>  - 判断目录是否存在，不存在则判断是否创建成功 *createOrExistsDir*
>  - 判断文件是否存在，不存在则判断是否创建成功 *createOrExistsFile*
>  - 判断文件是否存在，存在则在创建之前删除 *createFileByDeleteOldFile*
>  - 复制目录 *copyDir*
>  - 复制文件 *copyFile*
>  - 移动目录 *moveDir*
>  - 移动文件 *moveFile*
>  - 删除目录 *deleteDir*
>  - 删除文件 *deleteFile*
>  - 获取目录下所有文件 *listFilesInDir*
>  - 获取目录下所有文件包括子目录 *listFilesInDir*
>  - 获取目录下所有后缀名为suffix的文件 *listFilesInDirWithFilter*
>  - 获取目录下所有后缀名为suffix的文件包括子目录 *listFilesInDirWithFilter*
>  - 获取目录下所有符合filter的文件 *listFilesInDirWithFilter*
>  - 获取目录下所有符合filter的文件包括子目录 *listFilesInDirWithFilter*
>  - 获取目录下指定文件名的文件包括子目录 *searchFileInDir*
>  - 将输入流写入文件 *writeFileFromIS*
>  - 将字符串写入文件 *writeFileFromString*
>  - 简单获取文件编码格式 *getFileCharsetSimple*
>  - 获取文件行数 *getFileLines*
>  - 指定编码按行读取文件到List *readFile2List*
>  - 指定编码按行读取文件到StringBuilder中 *readFile2SB*
>  - byte单位转换（单位：unit） *byte2Unit*
>  - 获取文件大小 *getFileSize*
>  - 关闭IO *closeIO*
>  - 根据全路径获取最长目录 *getDirName*
>  - 根据全路径获取文件名 *getFileName*
>  - 根据全路径获取文件名不带拓展名 *getFileNameNoExtension*
>  - 根据全路径获取文件拓展名 *getFileExtension*

> - **图片相关→[ImageUtils.java][image.java]**
>  - 完善ing

> - **键盘相关→[KeyboardUtils.java][keyboard.java]**
>  - 避免输入法面板遮挡
>  - 动态隐藏软键盘 *hideSoftInput*
>  - 点击屏幕空白区域隐藏软键盘(注释萌萌哒) *clickBlankArea2HideSoftInput0*
>  - 动态显示软键盘 *showSoftInput*
>  - 切换键盘显示与否状态 *toggleSoftInput*

> - **网络相关→[NetworkUtils.java][network.java]**
>  - 打开网络设置界面 *openWirelessSettings*
>  - 判断网络是否可用 *isAvailable*
>  - 判断网络是否连接 *isConnected*
>  - 判断网络是否是4G *is4G*
>  - 判断wifi是否连接状态 *isWifiConnected*
>  - 获取移动网络运营商名称 *getNetworkOperatorName*
>  - 获取移动终端类型 *getPhoneType*
>  - 获取当前的网络类型(WIFI,2G,3G,4G) *getNetWorkType* *getNetWorkTypeName*

> - **手机相关→[PhoneUtils.java][phone.java]**
>  - 判断设备是否是手机 *isPhone*
>  - 获取手机的IMIE *getPhoneIMEI*
>  - 获取手机状态信息 *getPhoneStatus*
>  - 跳至填充好phoneNumber的拨号界面 *dial*
>  - 拨打phoneNumber *call*
>  - 发送短信 *sendSms*
>  - 获取手机联系人 *getAllContactInfo*
>  - 打开手机联系人界面点击联系人后便获取该号码(注释萌萌哒) *getContantNum*
>  - 获取手机短信并保存到xml中 *getAllSMS*

> - **屏幕相关→[ScreenUtils.java][screen.java]**
>  - 获取手机分辨率 *getDeviceWidth*、*getDeviceHeight*
>  - 设置透明状态栏(api大于19方可使用) *setTransparentStatusBar*
>  - 隐藏状态栏(注释萌萌哒) *hideStatusBar*
>  - 获取状态栏高度 *getStatusBarHeight*
>  - 判断状态栏是否存在 *isStatusBarExists*
>  - 获取ActionBar高度 *getActionBarHeight*
>  - 显示通知栏 *showNotificationBar*
>  - 隐藏通知栏 *hideNotificationBar*
>  - 设置屏幕为横屏(注释萌萌哒) *setLandscape*
>  - 获取屏幕截图 *snapShotWithStatusBar*、*snapShotWithoutStatusBar*
>  - 判断是否锁屏 *isScreenLock*

> - **SD卡相关→[SDCardUtils.java][sdcard.java]**
>  - 获取设备SD卡是否可用 *isSDCardEnable*
>  - 获取设备SD卡路径 *getSDCardPath*
>  - 完善ing

> - **Shell相关→[ShellUtils.java][shell.java]**
>  - 判断设备是否root *isRoot*
>  - 是否是在root下执行命令 *execCmd*

> - **尺寸相关→[SizeUtils.java][size.java]**
>  - dp与px转换 *dp2px*、*px2dp*
>  - sp与px转换 *sp2px*、*px2sp*
>  - 各种单位转换 *applyDimension*
>  - 在onCreate()即可强行获取View的尺寸 *forceGetViewSize*
>  - ListView中提前测量View尺寸(注释萌萌哒) *measureView*

> - **SP相关→[SPUtils.java][sp.java]→[Test][sp.test]**
>  - SPUtils构造函数 *SPUtils*
>  - SP中写入String类型value *putString*
>  - SP中读取String *getString*
>  - SP中写入int类型value *putInt*
>  - SP中读取int *getInt*
>  - SP中写入long类型value *putLong*
>  - SP中读取long *getLong*
>  - SP中写入float类型value *putFloat*
>  - SP中读取float *getFloat*
>  - SP中写入boolean类型value *putBoolean*
>  - SP中读取boolean *getBoolean*
>  - 获取SP中所有键值对 *getAll*
>  - 从SP中移除该key *remove*
>  - 判断SP中是否存在该key *contains*
>  - 清除SP中所有数据 *clear*

> - **字符串相关→[StringUtils.java][string.java]→[Test][string.test]**
>  - 判断字符串是否为null或长度为0 *isEmpty*
>  - 判断字符串是否为null或全为空格 *isSpace*
>  - null转为长度为0的字符串 *null2Length0*
>  - 返回字符串长度 *length*
>  - 首字母大写 *upperFirstLetter*
>  - 首字母小写 *lowerFirstLetter*
>  - 转化为半角字符 *toDBC*
>  - 转化为全角字符 *toSBC*

> - **时间相关→[TimeUtils.java][time.java]→[Test][time.test]**
>  - 将时间戳转为时间字符串 *milliseconds2String*
>  - 将时间字符串转为时间戳 *string2Milliseconds*
>  - 将时间字符串转为Date类型 *string2Date*
>  - 将Date类型转为时间字符串 *date2String*
>  - 将Date类型转为时间戳 *date2Milliseconds*
>  - 将时间戳转为Date类型 *milliseconds2Date*
>  - 毫秒时间戳单位转换（单位：unit） *milliseconds2Unit*
>  - 获取两个时间差（单位：unit） *getIntervalTime*
>  - 获取当前时间 *getCurTimeMills* *getCurTimeString* *getCurTimeDate*
>  - 获取与当前时间的差（单位：unit） *getIntervalByNow*
>  - 判断闰年 *isLeapYear*

[app.java]: https://
[const.java]: https://
[convert.java]： https://