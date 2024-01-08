---
title: java
---

#### 其他

```java
//	Boolean 返回值用来判断输赢---->把判断和打印赢输赢分开(逻辑性更强)

//	复制:	type[] newArrarName = Arrays.copyOf(ArrayName,ArrayName.length);
//	eg(复制arr2数组给新数组arr3):
	int[] arr2 = {1,2,3,3,4};
	int[] arr3 = Arrays.copyOf(arr2,5);

//	字段应该是私有的


```

**主方法入口：所有的 Java 程序由 public static void main(String[] args) 方法开始执行**
ctrl+句点 中英文切换

#### 快捷键

[eclipse 快捷键]!(https://qqe2.com/java/post/3405.html)

```
1. 查找java路径:cmd 在弹出的命令提示符中输入“java -version“用来查看 Java 是否安装
2. 替换:ctrl+f
3. 调出对象,变量:ctrl+o
4. 自动排版: 选中需要排版的代码，然后按下 快捷键 ctrl+shift+F 即可
```

#### Java 语言支持的变量类型有：

```java
1.  类变量：独立于方法之外的变量，用 static 修饰。
2.  实例变量：独立于方法之外的变量，不过没有 static 修饰。
3.  局部变量：类的方法中的变量。
4.  实例


public class Variable{
    static int allClicks=0;    // 类变量
    String str="hello world";  // 实例变量
    public void method(){
        int i =0;  // 局部变量
    }
}
```

#### if-switch

```java
system.exit(0)	关闭程序
scanner scan = new scanner(system.in);

    **对measureRectangle()的解释*****>(document comments)
	/**
	 * Function name:measureRectangle
	 * @param length (double)
	 * @param width (double)
	 * @return	(double)
	 * Inside the function:
	 * @exception
	 * 1.输入长度和宽度
	 * 2.打印面积
	 * if-switch
	 */

	public static double measureRectangle(double length,double width,String option) {
		if (length<0 || width<0) {
			System.out.println("length orwidth cannot be negative");
			System.exit(0);
		}

		switch (option) {
		case "area": return length*width;
		default: return 404;
	}
    }

```

#### this 关键字

1. this 意味着当前对象
2. 引入 this:目的是区分字段和参数
3. 主方法入口函数中对于类中变量的赋值是
   类.变量名 = " ";
4. 下面给以构造函数举例 -------------- this 关键字的使用:
   在构造函数中利用 this 关键字完成给类变量的传值:
   (1)和(2)的效果是相同的:

```java
	//	(1):
		String make;
		public Car(String make){
			this.make = make	//相当于(Car.make = make),构造函数public Car(String make)中的make是形参可以自定义命名.
		}

	//	(2):
		String make
		public Car(String mk){
			this.make = mk
		}
```

#### 内置函数

```java
Math.sin();
Math.cos();
Math.radom();
```
