# linux-RPCs
Linux进程间通信方式汇总

# 目前已包含的方式
1. 管道
2. FIFO(有名管道)
3. XSI消息队列
4. XSI信号量
5. XSI共享内存
6. POSIX信号量
7. domain socket

其中信号(signal)和信号量(semaphore)本质上并不算是进程间通信方式，应该是进程间同步的方式，但是也可以起到一定的通信作用，故也列在上面。

另外普通的mutex是作用线程间同步用的，但是可以将进程A和进程B共享的内存中初始化一个mutex，这样就可以用将此mutex用作进程间通信用了。
