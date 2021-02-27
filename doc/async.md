# Async

rust 异步设计文档
https://github.com/rust-lang/rfcs/blob/master/text/2592-futures.md

并发

并行

并行 说的 是 一种 方式、

一些事情 同时 被多个处理单元做 

仅强调 被同时被做


并发 说的是 一些事情 要同时被处理



## multitasking 多任务

一个 处理单元上的 多个任务 同时要 执行

原理 是 处理单元的 速度 大于 人类 感受到的 速度 、把不能感知到的速度、利用起来、去做别的事情、使用cpu串行、让人类感到并行、

做法、快速切换

## 抢占 多任务

一个人 在 做事情时 、是否允许 被打断、可以被打断 就可以抢占

不可以被打断 不可以抢占

## 保存状态

你在 打游戏 时 、被叫去学习、这时候 你要给游戏存档、好学习完毕、回来接着玩、这就是保存状态、然后切换 要做的事

## 协作 多任务


与 强行 打断 任务 相反的是协作多任务、

任何执行的任务不会被强行打断、只能由当前任务 主动放弃、每个任务也都很自觉和守规则的尽可能短而快的放弃、让别人来运行

一般 用 异步 

异步 

Future{
    type Output
    fn poll(self:Pin<&mut self>,cx :&mut Context) -> Poll<Self::Output>
}



# Fat pointer