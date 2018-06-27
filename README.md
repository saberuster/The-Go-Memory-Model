# The-Go-Memory-Model
https://golang.org/ref/mem 译文

版本：May 31, 2014

## 目录

## 概述

Go 内存模型具体说明了在不同 goroutine 中分别读写时的具体状况。

## 建议

多个 goruntine 对同一数据的修改必须序列化进行。

为了保证序列化，我们可以使用 channel 或其他像 `sync` 和 `sync/atomic` 包中的同步原语。

## 事件发生之前

