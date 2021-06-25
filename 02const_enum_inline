// effective.cpp : 此文件包含 "main" 函数。程序执行将在此处开始并结束。
//02、尽量以const，enum，inline替换#define


#include <iostream>
using namespace std;


class GamePlayer {
private:
    //const int Num = 5;    //不合适，不保证至多一份实体，取一个const的地址是合法的
    //static const int Num = 5;//候选，保证至多一份实体，取一个const的地址是合法的
                               //旧式编译器不允许static成员在其声明式上获得初值
    enum //MyEnum
    { Num2 = 5 };           //enum 更像#define，因为不可取址，且不会多份实体.2实用主义
                            //无法用#define创建一个class专属常量 
public:
    int socres[Num2] = { 0 };//使用常量

    void main() {
        //方法不在对象实体里
        cout << sizeof(socres) << "  sizeof(g): " << sizeof(*this) << "\n";
    }
};

template <typename T>//class内的private inline 函数
inline T Max(const T& a, const T& b) {
    f(a > b ? a : b);
}

//请记住
// 对于单纯常量，最好以const对象或enum代替#define
// 对于形似函数的宏定义，最好以inline替换#define



//enum

int main()
{
    GamePlayer g;
    g.main();
}

// 运行程序: Ctrl + F5 或调试 >“开始执行(不调试)”菜单
// 调试程序: F5 或调试 >“开始调试”菜单

// 入门使用技巧: 
//   1. 使用解决方案资源管理器窗口添加/管理文件
//   2. 使用团队资源管理器窗口连接到源代码管理
//   3. 使用输出窗口查看生成输出和其他消息
//   4. 使用错误列表窗口查看错误
//   5. 转到“项目”>“添加新项”以创建新的代码文件，或转到“项目”>“添加现有项”以将现有代码文件添加到项目
//   6. 将来，若要再次打开此项目，请转到“文件”>“打开”>“项目”并选择 .sln 文件
