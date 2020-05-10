# java线程和操作系统线程的关系

## 操作系统的线程

### linux 操作系统中的线程
通过如下命令查看linux 如何创建线程

<code language=shell>
man pthread_create
</code>

<pre>
NAME
       pthread_create - create a new thread

SYNOPSIS
       #include <pthread.h>

       int pthread_create(pthread_t *thread, const pthread_attr_t *attr,
                          void *(*start_routine) (void *), void *arg);

       Compile and link with -pthread.

</pre>
可以看出方法有四个参数：

| 参数 | 描述 | 
| :-----| :----: |
| pthread_t *thread | 传出参数，调用之后会传出被创建线程的id. 即pid |
| const pthread_attr_t *attr | 线程属性 |
| void *(*start_routine) (void *) | 线程启动后的主题函数，相当于java 中的run方法 |
| void *arg | 主体函数参数 |


_线程属性_
```c++
typedef struct{

　　　　　　int                                     detachstate;     //线程的分离状态

　　　　　　int                                     schedpolicy;    //线程调度策略

　　　　　　struct sched_param         schedparam;                  //线程的调度参数

　　　　　　int                                     inheritsched; //线程的继承性

　　　　　　int                                     scope;              //线程的作用域

　　　　　　size_t                                guardsize;       //线程栈末尾的警戒缓冲区大小

　　　　　　int                                     stackaddr_set; //线程的栈设置

　　　　　　void*                                 stackaddr;       //线程栈的位置（最低地址）

　　　　　　size_t                                stacksize;        //线程栈的大小

　　　　　　} pthread_attr_t; 

```