

[CS61B](https://csdiy.wiki/%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E4%B8%8E%E7%AE%97%E6%B3%95/CS61B/#_1)

[sp21](https://sp21.datastructur.es/)

[答案](https://github.com/InsideEmpire/CS61B-PathwayToSuccess)

[课程](https://sp24.datastructur.es/)

[gradescope](https://www.gradescope.com/courses/137626/assignments/1473073/submissions/315627984)


## 配置在wsl中java环境

`sudo apt install openjdk-11-jdk`

`sudo nano /etc/environment`

add: 
~~~
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
PATH=$PATH:$JAVA_HOME/bin
~~~

~~~
source /etc/environment
~~~

编译：
`javac HelloWorld.java
`
执行：

`java HelloWorld

java的执行过程：

![[java工作流.png]]


... 了解了java的一些语法


### HW0

#### Exercixe4

~~~
This is a particularly challenging exercise, but strongly recommended.

Write a function `windowPosSum(int[] a, int n)` that replaces each element a[i] with the sum of a[i] through a[i + n], but only if a[i] is positive valued. If there are not enough values because we reach the end of the array, we sum only as many values as we have.

For example, suppose we call `windowPosSum` with the array `a = {1, 2, -3, 4, 5, 4}`, and `n = 3`. In this case, we’d:

- Replace a[0] with a[0] + a[1] + a[2] + a[3].
- Replace a[1] with a[1] + a[2] + a[3] + a[4].
- Not do anything to a[2] because it’s negative.
- Replace a[3] with a[3] + a[4] + a[5].
- Replace a[4] with a[4] + a[5].
- Not do anything with a[5] because there are no values after a[5].
~~~


#### questions：

```java
public class windowPosSum {
  public static void windowPosSum(int[] a, int n) {
  for(int i = 0;i < a.length;i = i + 1) {
    if (a[i] < 0) {
    continue;
  }

  int sum =0;
  for(int temp = i; temp <=  n + i ; temp = temp + 1){
    if (temp >= a.length){
      break;
      }
    sum = sum + a[temp];
      }
       a[i] = sum;
    }
  }

  public static void main(String[] args) {
    int[] a = {1, 2, -3, 4, 5, 4};
    int n = 3;
    windowPosSum(a, n);

    // Should print 4, 8, -3, 13, 9, 4
    System.out.println(java.util.Arrays.toString(a));
  }
}
```

我第一次写的时候犯的很多错误：

1. `sum` 变量的作用域错误
2. `a[i] = sum;` 位置错误
3. 数组越界，索引判断错误
4. 我觉得我写的太过于冗余了

---

**NOTE：**`==` 与 `String`s 的行为很奇怪，原因我们将在本课程后面看到。您应该在 Java 中使用 `s1.equals（s2）` 检查字符串 `s1` 和 `s2` 是否相等。


---

调好了CS61B的环境配置，并且添加了自己的仓库

`git push -u Whuichenggong main` 把lab01更改推送到我github的仓库

---

#### lab 2：

学会调试， 通过理解代码 找出正确的代码并且传入