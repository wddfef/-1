# 实验报告二
##一、实验目的
1、掌握 C 语言中使用最多、最基本的一种语句﹣﹣赋值语句的使用。
2、掌握数据的输入输出方法，能正确使用各种格式转换符。
3、熟悉顺序结构的程序设计方法。
4、进一步掌握 C 语言程序的编辑、编译、连接和运行的过程。
##二实验准备
1、复习 C 语言的赋值运算符，同时区分“=”和“==”的区别。
2、复习 printf 和 scanf 的格式及要求。
3、复习程序代码编写规范。
##三、实验内容
#include <stdio.h>
float average(int a, int b) {
    return (float)(a + b) / 2;
}

int main() {
    int num1 = 20;
    int num2 = 30;
    int sum = num1 + num2;
    float avg = average(num1, num2);
    printf("两数之和为: %d\n", sum);
    printf("两数的平均数为: %.2f\n", avg);

    return 0;
}
问题：在示例三的代码中，如果想要在 average 函数里直接输出平均数，而不是返回平均数让 main 函数来输出，代码应该如何修改？
答案：include <stdio.h>
void average(int a, int b) {
    float avg = (float)(a + b) / 2;
    printf("两数的平均数为: %.2f\n", avg);
}

int main() {
    int num1 = 20;
    int num2 = 30;
    int sum = num1 + num2;
    average(num1, num2);

    printf("两数之和为: %d\n", sum);

    return 0;
}
