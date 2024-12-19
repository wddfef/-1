# 实验六 函数
##一、实验目的
1、掌握定义函数的方法。
2、掌握函数实参与形参的对应关系，以及“值传递”的方式。
3、掌握函数的嵌套调用和递归调用的方法。
4、掌握全局变量、局部变量、动态变量和静态变量的概念和使用方法
5、理解和掌握多模块的程序设计与调试的方法
##二、实验准备
1、复习函数调用的基本理论知识。
2、复习函数的嵌套调用和递归调用的方法。
3、复习全局变量、局部变量；静态变量、动态变量；外部变量等概念和具体实用方法。
##三、实验内容
#include <stdio.h>

// 计算一个数的平方的函数
int square(int num) {
    return num * num;
}

// 计算两个数平方和的函数，内部调用了square函数
int sumOfSquares(int a, int b) {
    return square(a) + square(b);
}

int main() {
    int num1 = 2, num2 = 3;
    int sum = sumOfSquares(num1, num2);
    printf("The sum of squares of %d and %d is %d\n", num1, num2, sum);
    return 0;
}
问题：如果在 sumOfSquares 函数中，先调用 square(b) 再调用 square(a)，对最终结果会有影响吗？
解答：不会有影响。因为 square 函数是计算一个数的平方，在 sumOfSquares 函数中无论是先计算 square(a) 还是先计算 square(b)，最终都是将两个数的平方结果相加，加法具有交换律，所以顺序的改变不会影响最终 sumOfSquares 函数返回的两个数平方和的结果。
