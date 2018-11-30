# BloomFilterTree
布隆过滤器处理海量数据，缓存穿透等


<pre>
原理
    布隆过滤器的巨大用处就是，能够迅速判断一个元素是否在一个集合中，因此它有如下三个使用场景：
        1）网页爬虫对URL的去重，避免爬取相同的URL地址。
        2）反垃圾邮件，从数十亿个垃圾邮件列表中判断某邮箱是否是垃圾邮箱，垃圾短信等。
        3）缓存穿透，将所有可能存在的数据缓存放到布隆过滤器中，当黑客访问不存在的缓存时迅速
           返回避免缓存及DB挂掉。

    布隆过滤器的原理：
        其内部维护一个全为0的bit数组，需要说明的是，布隆过滤器有一个误判率的概念。误判率越低，
    则数组越长，所占空间越大。误判率越高，数组越小，所占的空间越小。
</pre>