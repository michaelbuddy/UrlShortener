# UrlShortener
Url Shortener including principle &amp; Codes
# Algorithm 
## 1 自增序列算法 
* 设置 id 自增，一个 10进制id对应一个 62进制的数值，1对1，也就不会出现重复的情况。这个利用的就是低进制转化为高进制时，字符数会减少的特性。
## 2 摘要算法
* 将长网址 md5 生成 32 位签名串,分为 4 段, 每段 8 个字节
* 对这四段循环处理, 取 8 个字节, 将他看成 16 进制串与 0x3fffffff(30位1) 与操作, 即超过 30 位的忽略处理
* 这 30 位分成 6 段, 每 5 位的数字作为字母表的索引取得特定字符, 依次进行获得 6 位字符串
* 总的 md5 串可以获得 4 个 6 位串,取里面的任意一个就可作为这个长 url 的短 url 地址
