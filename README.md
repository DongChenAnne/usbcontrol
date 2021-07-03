#### **libusb - A cross-platform user library to access USB devices**  
 github website: https://github.com/libusb/libusb  
 libusb examples https://github.com/libusb/libusb/tree/master/examples  
 libusb API  https://libusb.sourceforge.io/api-1.0/index.html  
 libusb Modules  https://libusb.sourceforge.io/api-1.0/modules.html  
 libusb synchronous device I/O  常用函数：libusb_control_transfer, libusb_bulk_transfer, libusb_interrupt_transfer

#### **Install libusb-1.0-0 in Ubuntu 18.04**  
 sudo apt update  
 sudo apt install libusb-1.0-0  
 sudo apt-get install libusb-1.0-0-dev  

#### **Install libusb-1.0.24**  
 website: https://www.linuxfromscratch.org/blfs/view/svn/general/libusb.html  

#### **用libusb做Linux下的通讯**  
1. 使用命令行工具lsusb，查看当前设备的通信端点的通信方式。lsusb -v后，在Endpoint中的Transfer Type可以看到，usb_data_transfer.c里写的是interrupt模式。  
2. 使用lsusb查看输出端点和输入端点，记录端点号。一般情况为，写设备为0x01，读设备为0x81。
3. 查看输出缓冲区的大小，在写设备时会用到。 

#### **Compile and run tutorial**  
1. listdevs.c 和 testlibusb.c 是官方的example, 代码专门挑出来方便学习，若要编译运行要下载libusb-1.0.24, 按照 [libusb开发指南](https://blog.csdn.net/u012247418/article/details/82960889?utm_medium=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromMachineLearnPai2~default-3.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromMachineLearnPai2~default-3.nonecase)   
2. usb_data_tranfer.c 主要参考  [linux下的用libusb读写自定义HID设备](https://www.cnblogs.com/youyipin/p/12733125.html)所写，编译用 gcc -o xx xx.c -lusb-1.0  
3. 运行要在terminal下，不能在vscode里，以免系统崩溃  

#### **Website examples**  
 [libusb开发指南](https://blog.csdn.net/u012247418/article/details/82960889?utm_medium=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromMachineLearnPai2~default-3.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2~default~BlogCommendFromMachineLearnPai2~default-3.nonecase)
 [libusb的使用教程和例子](https://blog.csdn.net/zb774095236/article/details/83651995?utm_term=libusb&utm_medium=distribute.pc_aggpage_search_result.none-task-blog-2~all~sobaiduweb~default-9-83651995&spm=3001.4430)  
 [linux下的用libusb读写自定义HID设备](https://www.cnblogs.com/youyipin/p/12733125.html)  
 [linux下 libusb使用--打开usb设备进行通信](https://blog.csdn.net/u011598479/article/details/82705496)  
 [Android USB HID bulkTransfer()参数解析](https://blog.csdn.net/gd6321374/article/details/78045101)  
 [Linux 下使用libusb 与USB-HID 设备通讯之控制传输](https://blog.csdn.net/gd6321374/article/details/79935186?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_title-3&spm=1001.2101.3001.4242)  

