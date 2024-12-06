# 实验五 数组
##一、实验目的
1、掌握一维数组和二维数组的定义、赋值和输入输出的方法。
2、掌握字符数组和字符串函数的使用。
3、掌握与数组有关的算法（特别是排序算法）。
##二、实验准备
1、复习数组的基本知识。
2、复习字符串数组的特点和常用的字符串处理函数。
##三、实验内容
#include <stdio.h>

int main() {
    int numbers[10] = {2, 4, 6, 8, 10, 12, 14, 16, 18, 20};
    int sum = 0;
    // 遍历数组计算总和
    for (int i = 0; i < 10; i++) {
        sum += numbers[i];
    }
    double average = (double)sum / 10;
    printf("这组数字的平均值是：%.2lf\n", average);
    return 0;
}
问题：在示例二计算一组数平均值的 C 语言代码中，如果数组numbers中的元素个数发生了改变，比如变为了 20 个元素，代码需要做哪些调整才能正确计算平均值呢？
解答：
#include <stdio.h>

int main() {
    int numbers[20] = {......};  // 填入具体的20个整数值
    int sum = 0;
    for (int i = 0; i < 20; i++) {
        sum += numbers[i];
    }
    double average = (double)sum / 20;
    printf("这组数字的平均值是：%.2lf\n", average);
    return 0;
}
