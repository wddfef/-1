# 实验三 分支结构程序设计
##一、实验目的
1、了解 C 语言表示逻辑量的方法（以 0 代表“假”，以 1 代表“真”）。
2、学会正确使用逻辑运算符和逻辑表达式。
3、熟练掌握 if 语句和 switch 语句。
4、熟悉分支结构程序设计。
##二实验准备
1、复习关系、逻辑、条件运算符和表达式。
2、复习 if 语句的三种形式。
3、复习 if 语句的嵌套并能正确分析。
4、复习多分支选择 switch 语句。
##三、实验内容
#include <stdio.h>

int main() {
    int num1 = 10;
    if (num1 > 0) {
        printf("这个数 %d 是正数\n", num1);
    } else if (num1 < 0) {
        printf("这个数 %d 是负数\n", num1);
    } else {
        printf("这个数是0\n");
    }
    int day = 3;
    switch (day) {
        case 1:
            printf("星期一\n");
            break;
        case 2:
            printf("星期二\n");
            break;
        case 3:
            printf("星期三\n");
            break;
        case 4:
            printf("星期四\n");
            break;
        case 5:
            printf("星期五\n");
            break;
        case 6:
            printf("星期六\n");
            break;
        case 7:
            printf("星期日\n");
            break;
        default:
            printf("输入的数字不符合要求\n");
    }
    return 0;
}
问题
在这段代码中switch语句部分，如果忘记写break语句会出现什么情况呢？
解答
如果在switch语句里的case分支中忘记写break语句，当匹配到对应的case值开始执行代码后，程序不会自动跳出switch结构，而是会继续顺序执行后面case分支里的代码，直到遇到break或者整个switch语句结束为止。
