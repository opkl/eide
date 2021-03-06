# Change Log

All notable changes to the "eide" extension will be documented in this file.

***

### [v1.13.1]
- 更改: 调整 ARM-GCC 的编译配置格式，旧的配置格式将不再有效
- 更改: 使用相对路径完成项目编译生成
- 优化: 视图的显示
- 优化: 减少命令行的长度
- 优化: 移除无用的功能
- 修复: 自定义的 jflash 路径被覆盖
***

### [v1.13.0]
- 新增: IAR for STM8 工具链支持
- 新增: STM8-Debug 调试配置生成
- 新增: JLink 支持使用自定义的 jflash 文件
- 修复: 无法删除头文件包含路径的问题
***

### [v1.12.2]
- 修复: ARMCC V5 C++ 参数问题
- 修复: 一些细节问题
***

### [v1.12.1]
- 更改: 移除不必要的功能
- 更改: 修改视图结构
- 修复: 不必要的路径检查导致的问题
- 修复: 一些细节问题
***

### [v1.12.0]
- 新增: 可生成 LIB，通过修改编译配置选择
- 新增: 自动加载多工作区项目
- 新增: 可排除目录（非递归的）
- 新增: 可生成 bat 脚本，需要在设置中开启
- 更改: 调整 SDCC 的一些参数
- 更改: 为 Keil_C51 增加了一些链接器选项
- 修复: GCC 语法检查无法找到内置的头文件的问题
- 修复: stcgal 输出问题
- 修复: 修复一些细节
***

### [v1.11.0]
- 新增: 可排除源文件, 使其不加入到编译流程中
- 新增: SDCC 可选择生成 s19, elf
- 修复: GCC 工具链语法提示不完整的问题
- 更改: 移除 SDCC 中不常用的选项
- 优化: 优化一些细节
***

### [v1.10.1]
- 移除: 导入时的 utf8 转换选项
- 优化: 导入时为源文件创建更加完整的目录结构
- 优化: 切换项目时可直接打开工作区
- 优化: 提升使用体验
- 修复: STM8 下载问题
- 修复: 一些细节问题
***

### [v1.10.0]
- 新增: STLink 烧录支持
- 新增: 相关工具资源的下载
- 优化: 构建工具的输出
- 修复: 一些其他问题
***

### [v1.9.3]
- 新增: 显示 RAM 和 Flash 占比
- 更改: 使用树形视图显示项目文件结构
- 修复: 无效的宏导致的错误参数
- 修复: 多线程编译输出流阻塞导致的进程死锁问题
***

### [v1.9.2]
- 修复: 当编译选项的 json 配置格式错误时会被强制刷新为默认配置
- 更改: 可以一次性添加多个宏定义，宏之间用 ';' 分隔
- 新增: 一键转换 C51 关键字、寄存器定义到 SDCC 所需的格式
- 优化了一些细节
***

### [v1.9.0]
- 新增：GCC for ARM 工具链，使用前需要到`插件设置`设置好工具链安装目录
- 新增：可选择在编译时要使用的线程数
- 修复：工作区配置被强制刷新的问题
***

### [v1.8.0]
- 更改：移除内嵌的 JLink 工具，需要自行设置 JLink 安装路径
- 修复：ARM V6 路径 `\` 导致无法编译的问题
- 修复：构建工具 Fast-Mode 无法打开头文件的问题
- 修复：一些其他问题
- 优化：提升多线程的线程数
- 优化：插件大小大大减小
***

### [v1.7.0]
- 更改：C51 配置转移到 json 配置文件
- 新增：增加 SDCC 工具链，使用细节见[手册](https://blog.csdn.net/qq_40833810/article/details/104114921)
- 新增：插件配置 SDCC Install Directory（SDCC 安装目录）
- 修复：工具链安装位置有空格导致的无法编译的问题
- 修复：一些其他问题
- 优化：合并 js 提升插件加载速度
***

### [v1.6.0]
- 新增：加入多线程编译模式，默认开启，当编译的文件数大于 16 时有效；
- 更改：串口调试器`双向模式`的输出转移到虚拟文档, 详见[手册->串口调试器](https://blog.csdn.net/qq_40833810/article/details/104114921)
- 优化：提升快速编译的效率
- 修复：日志记录器引发的崩溃问题
- 修复：同名源文件生成的 obj 冲突的问题
- 修复：无法识别 .asm 后缀的汇编源文件的问题
- 修复：修复了一些其他问题
***

### [v1.5.0]
- 新增：对 ARM V6 工具链的支持，支持所有的编译选项，详见[手册](https://blog.csdn.net/qq_40833810/article/details/104114921)
- 更改：ARM 的编译选项转移到 json 配置文件中，因此对于旧的项目要重新设置编译选项
- 修复：修复了一些其他问题
***

### [v1.4.0]
- 新增：导入 Keil 项目时将编译参数一并导入，导出时自动为 Keil 设置编译参数
- 新增：8051 汇编(A51) 语法高亮，代码片段
- 新增：STC 烧录器，需要 Python3 支持，并安装 [STC 烧录器: stcgal](https://github.com/grigorig/stcgal)，具体用法见[使用手册](https://blog.csdn.net/qq_40833810/category_9688932.html)
  - 安装 stcgal：命令行执行 `pip3 install stcgal --user`
- 修复：C51 优化类型选择无效的问题
- 修复：C51 编译时出现 “拒绝访问” 的问题
- 更改：导出 Keil 项目前不需要安装 Keil pack，但导出后需要在 keil 中手动设置设备型号
- 更改：美化了一下烧录输出，使输出变得更加直观
- 优化：自动选择要用的 shell，无需再设置默认终端为 PowerShell
***

### [v1.3.0]
- 更改：取消勾选默认选项：`导入时自动转换文件为 UTF-8`
- 添加：编译选项：GNU Extension 选项，默认勾选
- 修复：无法生成 .bin 文件的问题
- 修复：生成的 cortex-debug 调试配置不正确的问题
- 修复：C/C++ 混合编译的参数问题
- 修复：导入不完整的问题

***

### [v1.2.2]
- 新增: 串口监视器，串口设置，详见**使用手册**

***

### [v1.2.1]
- 更改: 使用与 Keil 一致的 ROM/RAM 布局
- 修复: Keil package 的一些细节问题
- 修复: 一些编译参数的乱码问题
- 新增: 可以选择自定义的 ARM scatter 链接脚本, 在编译配置中更改

***

### [v1.2.0]
- 修复: 导入失败和模板下载问题

***

### [v1.1.4]
> 烧录注意事项：在烧录时，如果芯片已存在读保护，则首次烧录会失败，需要再尝试一次

- 修复: 烧录后无法自动复位芯片
- 新增: 项目模板，将你的项目框架导出为模板, 方便重复创建, 以提高效率
  - **说明**: 导出的项目模板可从 磁盘/Github公开仓库 导入到工程, 仓库位置在插件中进行设置, [默认仓库位置](https://github.com/github0null/eide-doc)
- 新增: 输出 .bin 文件
- 新增: 烧录读保护（注意：开启读保护后，会屏蔽自动复位选项；因为在烧录完成之后自动复位会触发读保护，导致芯片被擦除）
- 新增: 自动设置烧录文件的路径
- 新增: 插件设置`Convert Axf File To Elf File`: 在编译结束后转换输出的 .axf 为 .elf 以适应 GDB 调试器，默认关闭（这是一个实验性功能）
  - **说明**: .axf（由 Keil 生成）与 .elf（由 GCC 生成）的映像文件链接方式之间存在差异, 因此 .axf 文件在使用GDB调试时，ZI段（未初始化的全局变量、静态变量）可能未被正确置0, 将会是 -1, 开启此选项可能会改善这种情况

***

### [v1.1.3]
- 新增: 显示编译时间戳以及编译所用时间
- 新增: 增量编译(只编译被更改过的文件), 快捷键 <kbd>F9</kbd>
- 新增: 自动生成 cortex-debug 的调试配置

***

### [v1.1.2]
- 修复: ARM 编译时无法找到头文件
- 修复: 头文件搜索路径没有包含 root 目录
- 新增: 编辑器上下文菜单: 手动转换当前打开的 ANSI 格式的文件为 UTF8 格式，（Keil 的默认格式是ANSI，在 vscode 上会乱码）
- 新增: 编辑器上下文菜单: 撤销上次文件编码转换
- 新增: 插件设置: 在导入 Keil 项目时将所有源文件转换为 UTF-8 编码, 默认开启 (如果你的Keil源文件已经是无BOM的UTF-8格式的,可能会导致乱码,这时你需要关闭此选项)
- 新增: 可以复制标签的值，方便其他操作
- 新增: 加入 release/debug 模式，切换这些模式可以自动在编译时加入不同的宏, 用户可以在插件设置里自定义宏列表
***

### [v1.1.1]
- 修复: 无法自动创建 dependence 目录的问题
- 增加: 对 LIB 文件的链接, 可通过点击`添加LIB`按钮 或者 手动复制 LIB 文件到源文件目录完成 LIB 的添加

***

### [v1.1.0]
- 修复: 项目打开后 RTE_Components.h 的内容被删除的问题
- 更改: 更换已安装的 Component 的图标
- 更改: 删除无用的 STD dependence

***

### [v1.0.9]
- 修复: C51宏定义不全导致编译失败的问题

***

### [v1.0.8]
- 修复: ARM构建工具导致的乱码问题
- 修复: C51 编译参数过少的问题
- 修复: 无法创建 dependence 目录的问题

***
 
### [v1.0.7]
- 更改: 将 RAM 和 ROM 布局选项转到到一个单独的本地的 Web 页面
- 增加: 自动生成 “RTE_Components.h” 文件，以及自动更改，可使用插件设置 AutoGenerateRTE_Components 禁用，默认开启
- 增加: 默认的 GNU extensions 选项
- 增加: AutoGenerateRTE_Components 插件设置
- 增加: useMicroLib 选项
- 增加: 硬件浮点选项（只对于 cortex-M4 以及 cortex-M7 有效）
- 修复: C51 增加的宏没有参与编译过程的问题
- 修复: 安装 F4, F7 pack 包失败的问题
- 修复: 导出时 Keil 项目文件被覆盖的问题
- 修复: 使用'修复依赖'功能时删除了其他文件的问题
- 其他: 强化依赖导入的准确性，去除不必要的文件
- 其他: 自动删除包的不必要的部分以减小项目体积

***

### [v1.0.6]
- 修复没有找到 "core_cm.h" 头文件的问题
- 修复在导入 Keil 项目时, 头文件没有复制的问题
- 增加对 Keil 路径的验证
- 为 C51 项目加入了编译模式设置（用以支持更大 RAM 和 ROM 的 8051 芯片）和去除未使用的函数的选项（用以减小 代码 体积）

****

### [v1.0.5]
- 加入 JLink 烧录器, 支持一键烧录，暂不支持 C51
- 增加快捷键: <kbd>F6</kbd>编译 <kbd>F7</kbd>烧录 <kbd>Ctrl</kbd>+<kbd>F1</kbd>上传 eide 日志
- 优化了日志程序，方便上传应用日志，帮助改进此插件
- 修复部分问题

****

### [v1.0.4]
- 优化重复的路径
- 修复了中文路径问题
- 修复了一些其他问题

****

### [v1.0.3]

- 由于许可证问题，这个版本移除了自带的 Keil 编译工具, 安装包大大缩小, 因此如果需要使用编译功能，则需要安装 Keil 并在此软件内设置好路径
- 修复了导入 keil project 失败的问题
- 在导入时自动将 ANSI 编码的文件转换为 UTF8 文件, 避免了乱码
- 优化了构建工具，修复了部分故障
- 修复了一些其他问题

****

### [1.0.2]

- fixed some bugs

****

### [1.0.1]

#### Fixed

- fixed some errors

****

### [1.0.0] official version

#### Add

- add custom dependence for C51 project
- add some compile options for project
- add cpp compile option

#### Fixed

- cannot show C51 custom dependence
- Import error

****

### [0.0.4]

- repaired some problems on module: File.ts
- repaired some problems on module: import project from keil xml 
- open the error display
- add some error hint to display when extension occur a error

****

### [0.0.3]

- repaired some bugs

****

### [0.0.2]

- add a button for uninstall `Keil package`
- repaired the problem of load error without workspace
- repaired the problem of language highlight
- repaired the Log upload module
- cancel bind `ms-vscode-cpptools` extension
- repaired some error

****

### [First Release]

- V 0.0.1