## 2023/03/04

更细 节点选择可以更加 准确选择到需要节点
去除 不常用功能 优化
---------------------------
# 订阅地址
https://raw.githubusercontent.com/IC58G/QuantumultX/main/quantumult_202303-cn.conf
---------------------------
常用定时示例：

### 1、定点运行的几种常用格式

#### 每天0：00运行一次
0 0 * * *

#### 每天凌晨1:00运行一次
0 1 * * *

#### 每天凌晨1:30运行一次
30 1 * * *

#### 每天下午13:30分运行一次
30 13 * * *

#### 对照以上，可以凑出想要的定点格式了

-------------

### 2、按小时定点频率运行的几种格式

#### 每小时运行1次

0 0-23/1 * * *   每个小时运行一次，运行时间示例：1:00、2:00、3:00.....直到第二天1:00 循环

0 * * * *        和上面那个一样，每个小时运行一次，运行时间示例：1:00、2:00、3:00.....直到第二天1:00 循环

0 0-23/2 * * *   每2个小时运行一次，运行时间示例：2:00、4:00、6:00.....直到第二天2:00 循环

0 */2 * * *     每2个小时运行一次，运行时间示例：2:00、4:00、6:00.....直到第二天2:00 循环

0 2-4/1 * * *    每天凌晨2点到4点之间，每小时运行一次。 运行示例：2:00、3:00、4:00 ，第二天的2:00、3:00、4:00，循环

#### 比照以上规律，可写出按任意小时定点的格式

-------------

### 3、按分钟定点频率运行的几种格式

*/10 * * * *   每10分钟 运行1次   ，示例22:30、22:40类推

3,15 * * * *   每个小时的第3分钟和第15分钟运行 一次

3,15 8-11 * * *  每天早上8-11点间，每小时的第3分钟和第15分钟运行一次
