# BestTrace
转自doubi大佬
mkdir besttrace && cd besttrace
wget -N --no-check-certificate https://github.com/zhangweiqiandy/BestTrace/raw/master/BestTrace-Linux.tar.gz
tar -xzf BestTrace-Linux.tar.gz && chmod +x *
然后就可以通过 ./besttrace x.x.x.x 来路由追踪了。

默认是测试3次的，所以有时候会显示很乱，你可以加上 -q 1 ，比如  ./besttrace -q 1 x.x.x.x 。

这个参数指的是只测试一次，当然之所以测试3次就为因为可能会丢包等情况，三次可以比较准确。

使用示例：

root@doub.io:~/bash/besttrace# ./besttrace -q 1 14.215.116.1
traceroute to 14.215.116.1 (14.215.116.1), 30 hops max, 60 byte packets
 1  *
 2  192.254.84.153  0.72 ms  AS21859  美国 加利福尼亚州 洛杉矶 zenlayer.com
 3  te-0-0-0-2.cr1.lax3.us.zenlayer.net (192.254.81.69)  3.17 ms  AS21859  美国 加利福尼亚州 洛杉矶 zenlayer.com
 4  te-0-3-0-0.cr1.lax2.us.zenlayer.net (192.254.81.5)  3.25 ms  AS21859  美国 加利福尼亚州 洛杉矶 zenlayer.com
 5  218.30.48.173  1.29 ms  AS4134  美国 加利福尼亚州 洛杉矶 CHINATELECOM
 6  59.43.182.102  152.68 ms  *  中国 广东 广州 电信
 7  59.43.244.138  182.57 ms  *  中国 广东 广州 电信
 8  202.97.91.209  148.06 ms  *  中国 广东 广州 电信
 9  202.97.33.229  150.07 ms  AS4134  中国 广东 广州 电信
10  183.59.13.161  157.65 ms  AS58543  中国 广东 广州 电信
11  183.56.128.10  155.98 ms  AS58543  中国 广东 广州 电信
12  14.215.116.1  150.62 ms  AS58543  中国 广东 广州 电信
相似的路由追踪软件还很多，我也不一一列举了，各软件都有优缺点，自己看着用。

BestTrace 路由追踪，必须进入文件目录 或 加上文件目录（比如 bash /root/besttrace/besttrace x.x.x.x ）才能使用。
