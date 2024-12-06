# 实验四 循环结构程序设计
##一、实验目的
1、熟悉用 while 语句，do-while 语句和 for 语句实现循环的方法。
2、掌握在程序设计中用循环的方法实现各种算法（如穷举、迭代、递推等）。
3、掌握 continue 语句和 break 语句的使用。
4、熟练掌握循环结构的嵌套。
5、练习调试与修改程序。
##二实验准备
1、复习 while、do-while 和 for 语句的特点和适用条件。 2、复习 break 和 continue 的区别。
##三、实验内容
#include <stdio.h>

int main() {
    int guess;
    do {
        printf("请输入你猜的数字（1-10之间）：");
        scanf("%d", &guess);
        if (guess > 5) {
            printf("猜大了，请再试一次\n");
        } else if (guess < 5) {
            printf("猜小了，请再试一次\n");
        }
    } while (guess!= 5);
    printf("恭喜你，猜对了！\n");
    return 0;
}
问题：在上述 “猜数字游戏” 的do-while循环代码示例中，如果用户输入的不是整数，程序会出现什么情况，以及如何改进让程序能更合理地处理这种异常情况呢？
解答：
#include <stdio.h>

int main() {
    int guess;
    do {
        printf("请输入你猜的数字（1-10之间）：");
        // 先清空输入缓冲区中可能残留的字符
        while (getchar()!= '\n');
        if (scanf("%d", &guess)!= 1) {
            printf("输入不合法，请输入整数哦，请再试一次\n");
            continue;
        }
        if (guess > 5) {
            printf("猜大了，请再试一次\n");
        } else if (guess < 5) {
            printf("猜小了，请再试一次\n");
        }
    } while (guess!= 5);
    printf("恭喜你，猜对了！\n");
    return 0;
}
