# tightvnc
tightvnc


问题1：无法找到下面两个头文件
```c++
#include <d3d11.h>
#include <DXGI1_2.h>
```
下载安装
Windwos 8 SDK： https://go.microsoft.com/fwlink/p/?LinkId=226658

添加文件头
属性页》配置属性》vc++目录》包含目录，添加文件头
"C:\Program Files (x86)\Windows Kits\8.1\Include\shared";"C:\Program Files (x86)\Windows Kits\8.1\Include\um";..

问题2：无2015 c++运行时
安装这两个组件包
工具》获取工具和功能》修改》单个组件》
	MSVC v140 - VS 2015 C++ 生成工具(v14.00)
	对VS207(v141)工具的C++ Windows XP支持（已弃用）
在属性页平台工具集设置为sual Studio 2015 - Windows XP (v140_xp)

问题3：无法打开包括文件: “TimeAPI.h”。
原因：工程中缺少”TimeAPI.h”文件。
解决方法：把”TimeAPI.h”从工程去掉。
解决步骤：
a.把工程中所有的#include “TimeAPI.h” 用”//”屏蔽掉。