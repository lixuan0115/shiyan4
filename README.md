一、实验目的

掌握Java中抽象类和抽象方法的定义；

掌握Java中接口的定义，熟练掌握接口的定义形式以及接口的实现方法

了解异常的使用方法，并在程序中根据输入情况做异常处理

二、实验内容

某学校为了给学生提供勤工俭学机会，也减轻授课教师的部分压力，准许博士研究生参与课程的助教工作。此时，该博士研究生有双重身份：学生和助教教师。

设计两个管理接口：学生管理接口和教师管理接口。学生接口必须包括缴纳学费、查学费的方法；教师接口包括发放薪水和查询薪水的方法。

设计博士研究生类，实现上述的两个接口，该博士研究生应具有姓名、性别、年龄、每学期学费、每月薪水等属性。要求

编写测试类，并实例化至少两名博士研究生，统计他们的年收入和学费。根据两者之差，算出每名博士研究生的年应纳税金额。
三、实验要求

在博士研究生类中实现各个接口定义的抽象方法;

对年学费和年收入进行统计，用收入减去学费，求得纳税额；

国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用static final修饰定义。

实例化研究生类时，可采用运行时通过main方法的参数args一次性赋值，也可采用Scanner类实现运行时交互式输入。

根据输入情况，要在程序中做异常处理。

四、实验步骤

1.定义两个接口teacher student 并声明方法

2.在Graduate类中写出研究生应有的属性及学费和工资的算法并实现两个接口中的方法

3.在test中写出纳税额的算法输入月工资和学费，经过计算输出结果

五、核心代码

package gongzi;

public class Graduate implements StudentInterface, TeacherInterface{
    private String name;
    private String sex;
    private int age;
    private double xuefei;
    private double salary;
    public void setName(String a) {
        name = a;
    }
    public void setSex(String a) {
        sex = a;
    }
    public void setAge(int a) {
        age = a;
    }
    public void setmoney(double a, double b) {
        xuefei = a;
        salary = b;
    }
    public double setxuefei(){
        return 0;
    }
    public double getxuefei(){//返回每学年的费用
        return xuefei * 2;
    }
    public double setsalary(){
        return 0;
    }
    public double getsalary(){//返回年收入
        return salary * 12;
    }

}
六、实验截图
https://github.com/lixuan0115/shiyan4/blob/main/%E5%AE%9E%E9%AA%8C4%E7%BB%93%E6%9E%9C.jpg


七、实验感想
