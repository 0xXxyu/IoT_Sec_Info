# IoT_Sec_Info

记录一下学习的过程

## 硬件
    硬件基础
        电子电路
            电阻
            电容
            电感
            PCB
        通信接口
            UART
            JTAG
            SPI
            CAN
            ISP
            I2C
        芯片
            CPU架构
                MIPC
                ARM
            存储
                ROM
                    ROM
                    PROM
                    EPROM
                Flash
                    NOR Flash
                    NAND Flash
                常见封装格式
                    SOP
                    QFP
                    BGA
                    TQFP

                常见厂商
                    三星
                    展讯
                    海力士


   硬件拆解及焊接
   通信接口调试工具
        J-Link：JTAG仿真器，支持JTAG调试
        USBCAN：USB转CAN总线分析仪     
        物理攻击技术
            侧信道攻击（SCA)
            故障注入攻击(FA)
            侵入式攻击（IA)          

## 软件
    固件安全
        基础知识
            编程语言
                MIPS
                ARM

            固件加载流程
            Bootloader
                uboot
                Blob
                Grub


            文件系统
                基于存储型文件系统
                    squashfs
                    ubifs
                    jffs

                基于逻辑的文件系统
                    devfs
                    sysfs
                    procfs

            操作系统
                嵌入式Linux
                实时操作系统
                    RTOS
                    VxWorks

            常见漏洞
                命令执行
                信息泄露
                未授权访问
                xss
                后门漏洞
                任意文件操作
                堆栈溢出

        固件提取
            RT809H/RT809F等编程器：用于固件提取与烧录
            flashrom           

        固件模拟
            fimadyne 
            FimAE
            QEMU
            基于hook和patch的QEMU固件模拟
            基于unicorn的固件模拟
            基于qiling的固件模拟

        漏洞挖掘
            信息收集
                firmwalker：搜索文件系统种的敏感信息
                trommel：用于识别文件系统种的敏感信息

            自动化分析
                emba：自动化固件分析
                embark：web界面
                FAC_core：自动化固件分析比较工具

            逆向分析
                静态分析
                    IDA
                        flare-ida
                        idaplugins-list

                    Ghidra（常用插件列表：ghidra_scripts)
                    cwe_check：检测CWE的自动化工具，包括IDA和Ghidra插件
                    BinAbslnspector：自动化逆向和二进制文件漏洞静态分析工具
                    ROPgadget：ROP链查找
                    bindiff

                动态分析
                    IDA/Ghidra
                    gdb-multiarch
                    gdb常用插件
                        gef
                        pwndbg
                        peda

                    gdbserver：静态编译的不同架构的gdb服务端

    硬件安全架构
        安全生命周期管理
        调试端口保护
        固件安全
        可信执行环境


## 通信
    常用协议
        CoAP
        MQTT
            mqtt-pwn：mqtt渗透测试工具
        AMQP
        WebSocket
        CANbus
        Modbus
        DNP3
        BACNet
        XMPP
        UPNP
            UPnP​UPnP​

        DNS
        HTTPS
        NB-IoT

    车端
        DDS https://zhuanlan.zhihu.com/p/192981171
        
    近场协议
        RFID：PROXMARK支持RFID嗅探、读取、写入、破解等
            PROXMARK EASY
            PROXMARK 3
            PROXMARK RDV2
            PROXMARK EVO
            PROXMARK RDV4
            ICOPY-X
        NFC
            ​卡片分类​
            ​米家门卡方案.pdf​
        BT
            历史案例
                ​基于无感蓝牙遥控漏洞的蓝牙安全分析​
                ​遥控器蓝牙通信分析​
                ​BIAS​

            工具
                Wireshark
                NRF52**
                gatttool
                hcitool
                SweynTooth：BLE协议模糊测试框架
                expliot
        ZigBee
            ApiMote：可用来烧录killerbee
            killerbee：用于zigbee测试，支持监听、重放、洪水、自定义请求多种功能

        ZWave
        wirelessHART
        WIFI
            菠萝派：wifi钓鱼
            Aircrack：wifi密码破解
            https://www.freebuf.com/articles/wireless/338334.html

    无线电
        GSM
        GPS/卫星通信
        SDR
            HackRF One：无线电接收和发送
            LimeSDR：支持频段广泛，支持蜂窝、WIFI、LoRa、导航、气象等
        3G/4G/5G

## 移动端
    iOS安全
        iOS开发基础：https://github.com/qinjx/30min_guides/blob/master/ios.md
        黑苹果 https://hackintosh.myitnote.com/#_1-macos-%E7%B3%BB%E7%BB%9F%E9%95%9C%E5%83%8F%E5%86%99%E5%85%A5-u-%E7%9B%98
        一个资源汇总：https://github.com/iOSSecurity/iOSSecurity

    网络抓包
        wireshark
        tcpdump
        Fiddler
        Charles
        BurpSuite

    逆向分析
        IDA Pro：动静态调试
        Hopper：静态分析
        GDB：动态调试
        LLDB：动态调试
        Apktool：apk反编译
        jeb：静态反汇编分析
        smail/BakSmail
        JD-GUI
        JADX
        ByteCode Viewer

    Hook
    加固
        VMP
            [Android 逆向】加壳技术识别<https://blog.csdn.net/shulianghan/article/details/121893380>
            VMP加壳(一)：代码混淆原理
            VMP加壳（三）：VMP壳爆破实战-破解某编辑类软件&指令替换原理
            VMP加壳(二)：VMP的虚拟化原理

        脱壳
            DEX 整体加壳 | 函数抽取加壳 | VMP 加壳 | Dex2C 加壳https://developer.aliyun.com/article/865721

    历史漏洞
        Android序列化与反序列化不匹配漏洞详解 https://xz.aliyun.com/t/2364

## CTF
    基础知识
       [CTF Wiki](https://ctf-wiki.org/)
       [Linux PWN从入门到熟练](https://www.jianshu.com/p/695ca7a2cd5f)
       [PWN入门](https://www.jianshu.com/p/187b810e78d2)
       [栈溢出](https://www.zhihu.com/people/Jwizard/posts)
       [缓冲区溢出](https://blog.csdn.net/weixin_39190897/article/details/120529809)
    练习
        BUUCTF

## 安全基础
    C/C++
        不安全的函数
            https://blog.csdn.net/u014465639/article/details/71155515

