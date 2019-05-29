###task任务语法
一般的创建Task的语法为：
```
task hello{
    group '任务组'
    description '任务描述'
    dependsOn hello
    doLast{
        println "I'm Gradle"
    }
}
```
```
这看起来像是一种声明，task为关键字，hello为方法名，大括号里为方法属性
然而groovy是一种脚本语言所以这里的所有含义都有所不同
task：创建任务的方法名，也就是project上下文的一个方法，调用这个方法才能创建一个任务
hello：创建任务的第一个参数，任务名称
大括号：闭包，一段代码，创建任务的第二个参数
group：设置任务组的方法名，后面跟任务组名称参数
doLast：任务最后执行的闭包代码
```