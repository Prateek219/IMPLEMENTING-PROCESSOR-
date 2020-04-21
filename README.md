# IMPLEMENTING PROCESSOR
## About The Guide:-
Aim of this guide is to implement a microblaze processor in Xilinx FPGA using an example of a
counter counting at interval of 1 sec.
#### Get Started:-
1. Open Xilinx ISE create new project->new source->Embedded Processor give a name click next then
finish ISE will automatically open Xilinx Platform Studio EDK.

1.
![Screenshot (69)](https://user-images.githubusercontent.com/64007722/79830462-0db44200-83c3-11ea-947f-7a4893079d0c.png)

![Screenshot (70)](https://user-images.githubusercontent.com/64007722/79830682-90d59800-83c3-11ea-98e2-8ae68173fae1.png)

3. Go to your project directory search for a file "download.cmd" change 1 in that file by 5.
4.
![Screenshot (71)](https://user-images.githubusercontent.com/64007722/79830979-2ffa8f80-83c4-11ea-8e2b-abd92eb42b16.png)
![Screenshot (72)](https://user-images.githubusercontent.com/64007722/79831181-8962be80-83c4-11ea-8d1b-aaf67815aa0e.png)
5.
![Screenshot (73)](https://user-images.githubusercontent.com/64007722/79831368-e8283800-83c4-11ea-9f9a-e97d7046477a.png)

_Then copy and paste following lines into that
#### # _GENERIC TEMPLATE_

```
Net fpga_0_clk_1_sys_clk_pin TNM_NET = sys_clk_pin;
TIMESPEC TS_sys_clk_pin = PERIOD sys_clk_pin 100000 kHz;
Net fpga_0_clk_1_sys_clk_pin LOC=AH15;
Net fpga_0_rst_1_sys_rst_pin TIG;
Net fpga_0_rst_1_sys_rst_pin LOC=T25;
Net fpga_0_rst_1_sys_rst_pin PULLUP;
Net xps_gpio_0_GPIO_IO_pin<0> LOC=H18; # Bank 3, Vcco=2.5V, No DCI
Net xps_gpio_0_GPIO_IO_pin<1> LOC=L18; # Bank 3, Vcco=2.5V, No DCI
Net xps_gpio_0_GPIO_IO_pin<2> LOC=G15; # Bank 3, Vcco=2.5V, No DCI
Net xps_gpio_0_GPIO_IO_pin<3> LOC=AD26; # Bank 21, Vcco=1.8V, DCI using 49.9 ohm resistors
Net xps_gpio_0_GPIO_IO_pin<4> LOC=G16; # Bank 3, Vcco=2.5V, No DCI
Net xps_gpio_0_GPIO_IO_pin<5> LOC=AD25; # Bank 21, Vcco=1.8V, DCI using 49.9 ohm resistors
Net xps_gpio_0_GPIO_IO_pin<6> LOC=AD24; # Bank 21, Vcco=1.8V, DCI using 49.9 ohm resistors
Net xps_gpio_0_GPIO_IO_pin<7> LOC=AE24; # Bank 21, Vcco=1.8V, DCI using 49.9 ohm resistors


```
6.


