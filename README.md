# 并发框架Disruptor介绍

Martin Fowler在自己网站上写了一篇LMAX架构的文章，在文章中他介绍了LMAX是一种新型零售金融交易平台，它能够以很低的延迟产生大量交易。这个系统是建立在JVM平台上，其核心是一个业务逻辑处理器，它能够在一个线程里每秒处理6百万订单。业务逻辑处理器完全是运行在内存中，使用事件源驱动方式。业务逻辑处理器的核心是Disruptor。

![图片](images/Disruptor-300x144.png "参考图片")

Disruptor它是一个开源的并发框架，并获得2011 Duke’s 程序框架创新奖，能够在无锁的情况下实现网络的Queue并发操作。本文是Disruptor官网中发布的文章的译文（现在被移到了GitHub）。

## 下载
- [pdf](https://legacy.gitbook.com/download/pdf/book/lixiangyun/disruptor)
- [mobi](https://legacy.gitbook.com/download/mobi/book/lixiangyun/disruptor)
- [epub](https://legacy.gitbook.com/download/epub/book/lixiangyun/disruptor)

## 剖析Disruptor为什么会这么快

- [(一) 锁的缺点](1.1.md)
- [(二) 神奇的缓存行填充](1.2.md)
- [(三) 伪共享](1.3.md)
- [(四) 揭秘内存屏障](1.4.md)


## Disruptor如何工作和使用
- [(一) Ringbuffer的特别之处](2.1.md)
- [(二) 如何从Ringbuffer读取](2.2.md)
- [(三) 写入Ringbuffer](2.3.md)
- [(四) 解析Disruptor关系组装](2.4.md)
- [(五) Disruptor(无锁并发框架)-发布](2.5.md)
- [(六) LMAX Disruptor 一个高性能、低延迟且简单的框架](2.6.md)
- [(七) Disruptor Wizard已死，Disruptor Wizard永存！](2.7.md)
- [(八) Disruptor 2.0更新摘要](2.8.md)
- [(九) 线程间共享数据不需要竞争](2.9.md)

## Disruptor的应用
- [(一) LMAX的架构](3.1.md)
- [(二) 通过Axon和Disruptor处理1M tps](3.2.md)


## 转载[自并发编程网](http://ifeve.com)
