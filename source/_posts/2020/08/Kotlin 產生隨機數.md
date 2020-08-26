---
title: Kotlin 產生隨機數
date: 2020-08-26 03:47:49
tags: 
    - kotlin
    - random
---

## Kotlin 中的新 Random 類別

``` kotlin
kotlin.random.Random
```

Kotlin 的 Random 類別無須先產生物件，類別中的companion object 就提供許多方法來產生隨機的物件，而且比 JAVA 的來的更直觀。

<!-- more -->

## 產生隨機整數

Random 類別共提供三個方法產生整數

``` kotlin
fun nextInt(): Int
fun nextInt(until: Int): Int
fun nextInt(from: Int, until: Int): Int
```

* 第一個方法回傳在 `Int.MIN_VALUE` 到 `Int.MAX_VALUE` 之間的隨機整數  
* 第二個方法回傳 `0` 到傳傳入的 `until` 之間的非負隨機整數

包含 `0` 但不包含 `until`

* 第三個方法回傳 **from** 到 **until** 之間的隨機整數

包含 `from` 但不包含 `until`
傳入的 `from` 必須小於 `until`

## Refrence

- [參考資料](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.random/-random/)

