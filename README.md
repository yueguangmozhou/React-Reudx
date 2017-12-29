# React-Reudx


## Action

Action(动作) 是从你的应用（Component UI)送往Store存储）的信息负载


Action中的payload 是 负载或有效数据 的意思

> payload 在计算机里是指：
  数据传输时的‘有效数据’部分，也就是不包含传输时的头信息或metadatad等等用于传输其他数据
>它  的英文原本是指飞弹或火箭的搭载的真正有效的负载部分，如炸药或核弹头，不属于payload的部分当然就是火箭传送时用的燃料或控制零件


Action是有一个固定格式，叫做Flux Standard ACtion,FSA(Flux标准动作）

```
 {
   type: 'ADD_TODO',
   payload: {
      text: 'do something'
      }
  }
```

一个描述动作的单纯对象字面定义

Action 必须要有type(类型）,且在一个应用中type名称是不能重复的，他的概念有点类似于数据表中的主键属性

## Action Creactor

  动作生成器
  
  在程序语言的函数库中，英文名词，通常代表数据或对象 格式，如Action就是一个单纯的对象
  
  xxxer或 xxxor的中文翻译是‘器、者’通常就是函数或方法，如reducer 、action creator
  
  
  由Flux架构来的产物，是一种辅助用的函数，用来创建、生成Action(一个对象）
  
  当然它本身是一个函数，在返回Action对象之前可以再针对返回的动作数据先进行运算或整理
  ```
  const ADD_TODO = 'ADD_TODO'
  
  function addTodo(text){
    return { 
      type : ADD_TODO
      payload: {text}
     }
     
     
              
