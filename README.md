# 250-bugs
突发奇想，就是想记录一下一个人到底能写出多二百五的bug。唉~，就是玩。

# Bugs

## 2021.5.28
语言/框架：React 17

详情：点击a链接跳转到目的地后，后又跳回来了

原因：a 链接绑定了一个onClick事件，路由到目的url，然后 a 的 href 又被我写上了当前路径。

伪代码：

  ```
  <a href="/home" onClick={this.route.push("/next-page")}></a>
  ```

## 2021.6.15
语言/框架：Typescript

详情：if 语句一直返回True

原因：if 语句判断条件写错了。少写了一个 `a ==`， Type enum 类型，所以一直返回true。

伪代码：

  ```
   if(a == Type.Type1 || Type.Type2) return
  ```

## 2021.9.26
语言/框架：Jest

详情：render 中写组件就报错

原因：文件名 test.tsx 创建成了 test.ts 导致不支持 tsx 语法

伪代码：

  ```
   import renderer from 'react-test-renderer'
   renderer.create(<Message />) //报错
  ```
