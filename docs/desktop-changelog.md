## v2.3.1

- **新功能**

    1. 用户可以在串口终端中使用回车键发送数据。
    2. 提高 esp32/8266 的默认上传波特率以提高上传速度。
    3. 删除 esp32 不常使用的 sensor 目录中的积木。
    4. 串口终端新增 Ctrl+A/B/C/D 快捷键支持，以更好的与 micrpython repl 界面交互。
    5. 移除不常用的 arduino mini 控制板。
    6. 修改 arduino nano 下载参数使用旧的引导加载程序，并添加缺少的 A6 A7 引脚。
    7. 加宽上传窗口。
    8. 屏蔽 esp32/8266 内部 flash 使用的管脚。
    9. 增加 esp32 引脚模式的下拉输入模式。

- **修复错误**

    1. 许可证文件未打包在安装包中。
    2. 修复 microbit 终端积木外框与本体颜色相同的问题
    3. 修复部分int类型输入可以设置为小数的问题。
    4. Microbit 的设置像素在 XX 位置亮度积木的亮度参数没有生效。
    5. 修复 microbit v2 下载程序失败的问题。

## v2.3.0

- **新功能**

    1. 应用程序可以自动更新了。
    2. 支持同时打开多个应用。
    3. 增加繁体中文翻译。
    4. 增加软件加载界面。
    5. 新增代码编辑支持，解锁代码区后可进行代码编辑。
    6. 在上传模式下隐藏角色和声音选项卡。
    7. 在上传模式下禁用菜单栏中的编辑按钮。
    8. 在 micropython 的上传模式下，自定义列表变量的积木可以生成代码。
    9. 优化和减小外部资源文件大小。
    10. 合并windows版本的32位和64位安装文件。
    11. 在没有硬件设备的情况下保存工程时，转换成 scratch3 支持的格式，这样 scratch3 就可以打开 openblock 创建的纯 scratch 工程。 （保存格式还是 .ob 但是 scratch 可以强制打开）

- **修复错误**

    1. 修复软件首次启动需要复制缓存，导致长时间不显示的问题。用户多次点击启动图标后，多个程序同时对缓存进行操作，导致缓存文件损坏，然后程序无法启动。
    2. 修复开启和关闭加速模式按钮翻译错误。
    3. 选择 arduino uno 再选择 mega2560 后，pin 菜单没有更新。
    4. arduino pin 中断功能的代码错误。
    5. python 变量增加积木在输入超过两位数后会截掉第一位。
    6. 在起始类积木后使用重复积木而不是硬件设备启动事件积木后时，生成的代码逻辑不正确。
    7. arduino 的包含积木的代码应该是 'indexOf' 而不是 'indexof'。
    8. arduino 的比较积木在输入为一对字符串或单个字符时生成不符合C语言规则的代码。
    9. 在 micropytho n中，由于自定义函数或事件定义的函数中没有对自定义变量的全局声明，所以在这些块下使用自定义变量块时会报错。
    10. 调整 micropython 代码生成结构，防止变量和函数在定义声明前被调用。
    11. 积木从工具栏拖出但尚未放入工作区时会生成代码。
    12. 修复 arduino 设备编译完成后有时等待十多秒才开始上传的问题。

## v2.2.9

- **新功能**

    1. 优化windows nsis安装脚本，现在首次安装路径会被设置到c盘根目录，之后的安装路径则会自动探测并修改为首次安装时选择的安装目录。
    2. 添加对scratch原版工程文件的支持。
    3. 在角色选择等资源库中加入恶魔小鸟。

- **修复错误**

    1. 在角色说话时切换编程模式会导致界面崩溃。
    2. 加载含有自定义列表变量的工程文件时会报错无法完成加载。
    3. 自定义函数的参数积木在切换模式时会被禁用。
    4. 终端中不显示esp32和microbit串口数据。
    5. 修正esp32/8266的编程语言图标。
    6. 修正恶魔小鸟旋转运动的中心坐标。

## v2.2.8

- **新功能**

    1. 在设备配置中加入默认编程模式的设置。

- **修复错误**

    1. 加载新工程后旧的设备连接没有被断开。
    2. 加载新工程后，如果工程内没有设备扩展，代码区会是空的。
    3. 在连接没有 firmata 服务的设备后，不会弹窗提示下载固件。
    4. 优化 firmata 通讯构架修复一些潜在的问题。
    5. 修复设备配置中拼写错误的名称从 leanMore 到 learnMore。
    6. 修复了 Arduino 积木块不准确含义的名称从 whole number 到 integer。
    7. 修复M icrobit V2 进入REPL失败后， 尝试下载固件时失败的问题。

## v2.2.7

- **修复错误**

    1. 加载工程文件后，再次保存工程文件并再加载，会报错无法加载工程。
    2. 加载工程文件后，点击新建工程按钮，界面会崩溃。
    3. 在上传模式下打开扩展界面时，会卡顿1~2秒后才能加载出插件选项。

## v2.2.6

- **修复错误**

    1. Arduino MEGA2560 串口发送积木的换行参数未生效。
    2. 在添加新的角色后，设备选择被清除。
    3. 加载含有多个设备插件的功能后会发生错误。

## v2.2.5

- **修复错误**

    1. 由于openblock资源源代码中的shield拼写错误为sheild，GUI界面中的shield筛选器显示为空。
    2. 在虚拟机中，多写一行startheartbeat函数调用，startheartbeat重复返回，导致实时通信错误。
    3. 增加rtscts流量控制配置，修复打开rtscts流量控制时部分三方兼容板无法使用的情况。
    4. 弹出警告或确认窗口后，无法编辑输入框。
    5. 创建新项目后，设备选择未清除。
    6. 创建新项目后，旧的设备没有断开连接。

## v2.2.4

- **修复错误**

    1. 对于Arduino UNO等控制板的读取数字引脚块，没有A0~A5选项。
    2. 使用快捷键Ctrl+Z修改块后，右侧的代码不会更新。

## v2.2.3

- **修复错误**

    1. 双击以打开带有选择了设备的项目文件时，在加载过程中会报错。
    2. 为设备扩展的积木块添加注释后，保存项目文件。如果在重新启动软件后尝试加载项目，则会出现一个无法删除的注释窗口。

## v2.2.2

- **新功能**

    1. 优化串口终端字体和换行显示效果。
    2. 首先在扩展库中显示加载的扩展。
    3. 修改esp8266默认串口配置为官方默认76800。
    4. 修改esp8266上传速率为921600，加快上传速度。

- **修复错误**

    1. 加载带有扩展名的项目时，会报错无法加载。
    2. 变量增加块的输入框在放置其他块或变量时解析错误。
    3. 偶数角色中，工具箱区域中的移动方块不会自动变为角色当前位置的坐标。
    4. 修复 esp32 和 esp8266 在连接 openblock 时，由于缺少串口启用dtr rts流控，点击reset按钮后无法启动的问题。
    5. 在上传模式下连接和断开设备一次后，无论以何种模式再次连接设备，都将无法与连接固件建立通信。
    6. ESP32 和 ESP8266 在编译和上传之间会卡住很长时间。

## v2.2.1

- **修复错误**

     1. 串口发送的数据有误。
     2. 有时无法双击打开工程文件或加载工程时出错无法加载工程文件。
     3. 连接设备后重复加载项目会导致多个实时模式监听器开始导致错误。

## v2.2.0

- **新功能**

    1. 在设备选择中添加套件过滤器选项。
    2. 增加取消设备选择的选项。
    3. 加载包含未知设备和插件的项目时，会报错详细信息。
    4. 根据新的图片标准更新设备图片。
    5. 自动获取外部扩展中的控制板管脚列表。
    6. 添加滑块类型块。
    7. 优化恶魔鸟svg图片。
    8. 添加返回编辑菜单。

- **修复错误**

    1. 串口发送按钮在小窗口模式下被折叠。
    2. 修改windows桌面版默认安装路径为C盘根目录，而不是用户数据的深层目录。
    3. 如果外接设备列表中有不支持的设备ID，设备型号将为空。
    4. 由于vm构建块在optype前面添加了设备类型，导致无法正常翻译display变量。
    5. esp8266数字管脚不能选择GPIO16。
    6. 勾选复选框，使变量显示在舞台区，切换设备后变量仍然存在。
    7. Arduino ceil 函数名错误。
    8. Microbit 姿态选项未翻译。
    9. Microbit 使用多个不受支持的 while true 语句。
    10. 当使用滚轮移动工具箱时，超出边界的完全显示的块再次被阻挡。
    11. 颜色选择器功能不可用。
    12. 切换模式后断线错误提示闪烁。
    13. 使用第三方设备时，告警使用的是主板，而不是第三方设备板的图片。
    14. 在没有目标但有变量的情况下加载设备时出错。

## v2.1.1

- **新特性**

    1. 加入对 esp8266 和 makeymakey 的支持。
    2. 加入显示所有可连接设备的按钮。避免用户在使用为收录的usb转串口芯片时无法连接设备。
    3. 加入.ob工程文件关联。

- **修复BUG**

    1. 多次切换编辑目标后会严重卡顿。
    2. 配置错误的远程资源地址后点击检查更新的按钮软件会崩溃。
    3. 远程资源使用了openblockcc的地址而非配置中的设定值。
    4. 在工作区使用工具箱中嵌套结构的积木时，在更新禁用状态后，内部嵌套积木会被错误的禁用。
    5. 在打开多个窗口是会报错：地址已经使用。

## v2.1.0

- **新特性**

    1. 变更 Arduino 构架工具由 arduino-builder 为 arduino-cli.
    2. 加入外部插件和设备远程升级功能。
    3. 变更默认角色为恶魔小鸟。
    4. 加入对 arduino esp32 控制板的支持。
    5. 加入对 microbit V2 控制板的支持。
    6. 加入清除缓存按钮。
    7. 加入安装驱动按钮。
    8. 移动实时模式连接指示器到舞台区上方。
    9. 为桌面版警告弹窗加入本地化翻译。
    10. 加入上传超时报错。如果卡在上传界面几十秒后，会显示上传超时报错，使得用户可以点击关闭按钮而不是永久卡在上传界面。
    11. 加入 arduino uno ultra基础控制板以支持包含 A6，A7 引脚的定制控制板。
    12. 优化外部插件构架。
    13. 优化固件文件结构。
    14. 优化串口构架。防止在接收到大量的串口数据时导致的界面卡顿。
    15. 加入 QDP ROBOT C02 套件 (arduino esp32)。

- **修复BUG**

    1. 如果在 arduino 构建过程中拔掉 usb 线缆，会卡在上传界面。
    2. 在上传过程中拔掉 usb 线缆，gui 界面却没有显示断开设备，导致用户可以再次点击上传按钮而卡在上传界面。
    3. 在连接和断开几次设备后再次上传程序或固件会导致实时模式通讯故障。
    4. 在上传成功后如果不关闭窗口就拔掉 usb 线，会显示上传失败。

## v2.0.0

- **新特性**

    1. 加入串口终端界面。
    2. 从打包中分离第三方衍生设备代码，现在可通过修改外部配置文件控制设备选择界面中的内容了，而不需要重新打包。
    3. 优化积木在不同编程模式下的禁用逻辑。
    4. 实时模式下可以在插件选择界面中选取原本被屏蔽的实时模式插件了。
    5. 积木在没有连接有效代码生成主体时，其 define、step 等非本体的设置代码，现在不会在代码区生成了。
    6. 调整 Arduino 代码生成器生成代码的结构，使之更符合 Arduino 原生代码格式。
    7. 工程文件会保存当前的编程模式, 加载后自动切换至保存时的模式。
    8. 编程模式下积木不再能被点击执行和发光了。
    9. 实时模式通讯建立成功后不在弹窗，而通过连接图标右侧的通讯图标的暗灭来指示通讯是否成功。仅在尝试通信失败后才会弹出警告窗口并提示下载实时模式固件。
    10. 下载固件且实时通讯建立成功后，实时模式失败警告的弹窗将会自动消失。

- **修复BUG**

    1. 在加载具有多个大型插件的工程文件时，会出现工具栏区重复显示多个插件内容而有些则未被加载等错误。
    2. 在无连接设备时，下载固件的按钮没有被禁用。
    3. 缩短上传信息的显示窗口，以修复在部分设备上窗口显示不完整的问题。
    4. 修复大量有关实时模式通讯的潜在问题。
    5. 代码窗在调整窗口大小后没有重新渲染导致显示缺失一块。
    6. 切换编程模式等后角色会消失。
    7. Arduino 和 Microbit 在编程模式下没有隐藏全部的不支持积木。
    8. Microbit 的 buttonIsPressed 积木转码函数按键B时本应为 b 写成了 n。
    9. Microbit 自定义变量名称异常问题。
    10. Arduino UNO Mega2560 串口0转译代码不正确。
    11. 变量设置增加的积木块的数字解析错误。
    12. 取消1.05倍界面缩放设置，直接改大字体以修复工具栏菜单字体模糊的问题。

## v1.2.2beta

- **新特性**

    1. 添加隐藏代码区按键。
    2. 变更上传按键的外观设计。
    3. 更改一些控制板的描述。
    4. 增加1.05倍界面缩放用以修复部分设备上字体模糊的问题。
    5. 变更工程文件扩展名由 .sb3 为 .ob。

- **修复BUG**

    1. Microbit 代码生成器错误。
    2. Arduino 设置数字输出的引脚菜单中没有模拟引脚选项。

## v1.2.1beta

- **新特性**

    1. 添加隐藏代码区按钮。
    2. 变更上传按钮外观。
    3. 变更一些控制板的描述，以适应中国广告法。
    4. 添加1.05倍缩放以修复字体模糊问题。

- **修复BUG**

    1. Microbit 代码生成不工作。
    2. Arduino 数字输出积木的引脚菜单选项内没有模拟引脚。
    3. 第三方套件由基础控制板继承的积木块代码转译功能错误。

## v1.2.0beta

- **新特性**

    1. 现在大多数弹窗提示将会在5秒后自动消失。
    2. 完成 Microbit 的全部功能实现。
    3. 加入舵机插件作为 Mcrobit 插件的样例。
    4. 在安装新版本的 OpenBlock 软件后，旧版本留存下缓存将被自动清除。

- **新设备/套件**

    1. Arduino Mini
    2. 齐护机器人套件

- **修复BUG**

    1. 错误的CP2102硬件ID。

    2. Microbit翻译错误。
    3. 加载工程后无法扫描到设备。
    4. 选择新的设备后旧设备加载的插件仍然存在。

## v1.1.0beta

- **新特性**

    1. 在鼠标移入工具区后因为过长而隐藏部分显示的积木块会被全部显示。
    2. 在选择设备后会自动加载设定的扩展。

- **新设备/套件**

    1. Microbit
    2. Iron robot kit