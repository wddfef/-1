# 实验七 指针
##一、实验目的
1、熟练掌握指针、地址、指针类型、void 指针、空指针等概念。
2、熟练掌握指针变量的定义和初始化、指针的间接访问、指针的加减运算和指针表达式。
3、会使用数组的指针和指向数组的指针变量。
4、会使用字符串的指针和指向字符串的指针变量。
##二、实验准备
1、复习变量、变量的地址、指针变量的概念并明确区分这三个不同的概念。
2、复习指针和数组的结合应用。
3、复习指针的其他理论知识。
##三、实验内容
#include <stdio.h>

// 交换两个整数的函数，使用指针作为参数
void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int num1 = 5, num2 = 10;
    printf("Before swap: num1 = %d, num2 = %d\n", num1, num2);
    swap(&num1, &num2);  // 传递变量的地址给函数
    printf("After swap: num1 = %d, num2 = %d\n", num1, num2);

    return 0;
}
问题：在 swap 函数中，如果不使用中间变量 temp ，能否实现交换两个变量的值呢？如果可以，该怎么做呢？
解答：
#include <stdio.h>

// 交换两个整数的函数，使用指针作为参数，利用异或运算实现无中间变量交换
void swap(int *a, int *b) {
    *a = *a ^ *b;
    *b = *a ^ *b;
    *a = *a ^ *b;
}

int main() {
    int num1 = 5, num2 = 10;
    printf("Before swap: num1 = %d, num2 = %d\n", num1, num2);
    swap(&num1, &num2);  // 传递变量的地址给函数
    printf("After swap: num1 = %d, num2 = %d\n", num1, num2);

    return 0;
}
