FAST版本：2.0
修改时间：2018-10-24
修改内容：
1、GAC模块采用寄存器读写方式配置RAM。
2、cmd控制信号贯串五级流水线。
3、每个模块。包括data_cache，都设有模块计数和状态信号。
4、从um顶层分下来6条locslbus到每个模块，用于读取模块计数和状态。
5、um中寄存器读写地址偏移2位。

修改记录：
2018-09-12 
模块的计数和状态信号不再输出到UM顶层，直接通过寄存器读写方式读取。
2018-09-13
修改了goe模块，加入模块计数，利用cmd控制消息读取计数。
2018-09-30
修改了goe模块，根据分组流ID计数，调整环形通路读取计数的地址。
2018-10-16
修改了gme模块，添加index计数，可用环形控制通路读取,操作地址为0，8 ，10，1f8。
修改了goe模块，修改了流表计数读取方式，采用寄存器读写方式操作。
2018-10-23
修正了gke模块中对IPv4类型分组解析的错误。
2018-10-25
调整了gke模块提取的关键字组成数据位宽，FRAG由4位改成2位，INPORT为6位。
