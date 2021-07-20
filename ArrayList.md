# ArrayList

## 一、ArrayList的用法

### 1.`public boolean add(E e)`

> 向集合中添加元素，参数的类型与泛型一致。返回值代表添加是否成功。

> 【PS】
>
> a.  对于ArrayList集合来说，add添加动作一定是成功的，所以返回值可用可不用。
>
> b. 但是对于其他集合（今后学习）来说，add添加动作不一定成功。

### 2.`public E get(int index)`

> 从集合中获取元素，参数是索引编号，返回值就是对应位置的元素。

### 3. `public E remove(int index)`

> 从集合中删除元素，参数是索引编号，返回值就是被删除的元素。

### 4.`public int size()`

> 获取集合的尺寸长度，返回值就是集合中包含的元素个数。

## 二、代码演示

```java
public class Demo01ArrayListMethon(){
    public static void main(String[] args){
        ArrayList<String> list = new ArrayList<>();
        System.out.println(list);//[]
        
        //向集合中添加元素：add
        boolean success = list.add("柳岩");
        System.out.println(list);//[柳岩]
        System.out.println("添加的动作是否成功，"+success);//true
        
        list.add("高圆圆");
        list.add("赵又廷");
        list.add("李小龙");
        list.add("冉冰");
        System.out.println(list);//[柳岩，高圆圆，赵又廷，李小龙，冉冰]
        
        //从集合中获取元素：get,索引从0开始
        String name = list.get(2);
        System.out.println("第2号索引位置："+name);//赵又廷
        
        //从集合中删除元素：remove,索引值从0开始
        String whoRemoved = list.remove(index:3);
        System.out.println("被删除的人是："+whoRemoved);//李小龙
        System.out.println(list);//[柳岩，高圆圆，赵又廷，冉冰]
        
    }
}
```



