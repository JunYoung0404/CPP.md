# 기말고사 c++문항

○ 바인딩 & 람다함수❤(기말고사 출제)

C++에서 "바인딩(binding)"은 이름을 값에 연결하는 과정을 가리킵니다. 바인딩은 변수가 값에 연결될 때, 함수가 호출되어 실행될 때, 객체가 클래스의 인스턴스로 생성될 때 발생합니다.

람다 함수를 사용하여 특정 값에 바인딩하는 예를 들어보겠습니다:
~~~
#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<int> nums = {1, 2, 3, 4, 5};
    int a = 2;

    // a 값을 '2'로 바인딩하고 nums 벡터의 각 요소에 곱하는 람다 함수
    auto multiply = [a](int b) { return a * b; };

    std::transform(nums.begin(), nums.end(), nums.begin(), multiply);

    for(int num : nums) {
        std::cout << num << " ";
    }

    return 0;
}
~~~

CPoly로 부터 멤버 변수 w,h를 상속받고, CRect와 CTry는 각각 삼각형, 사각형의 클래스 pure virtual함수로 면적을 계산하시오.❤(기말고사 출제)
~~~
#include <iostream>

class CPoly {
protected:
    double w, h;
public:
    CPoly(double w, double h) : w(w), h(h) {}
    virtual double area() const = 0; // pure virtual function
};

class CRect : public CPoly {
public:
    CRect(double w, double h) : CPoly(w, h) {}
    double area() const override {
        return w * h;
    }
};

class CTry : public CPoly {
public:
    CTry(double w, double h) : CPoly(w, h) {}
    double area() const override {
        return w * h / 2;
    }
};

int main() {
    CRect rect(4, 5);
    CTry tr(3, 4);
    std::cout << "Rectangle area: " << rect.area() << '\n';
    std::cout << "Triangle area: " << tr.area() << '\n';
    return 0;
}
~~~
C++언어와 경쟁이 되는 언어들❤(기말고사 출제)
~~~
Rust

Go

Swift

Kotlin
~~~
MFC❤(기말고사 출제)
~~~
GetDlgItemInt(IDC_EDIT1)
~~~
람다함수 쇼팅 문제 제출

퀵쇼트❤(기말고사 출제)
~~~
#include <stdio.h>
#include <stdlib.h>
int static cmp (const void* a, const void* b) 🧡const void* a 이부분 빈칸 출제
{
    if (*(int*)a > *(int*)b)      return  1;
    else if (*(int*)a < *(int*)b) return -1;
    else                          return  0;
}
void main()
{
    int a[] = {3, 1, 2, 5, 4};
    int s = sizeof(a) / sizeof(int);
    int i;
    for (i = 0; i < s; i++) printf("%d ", a[i]);
    printf(":정렬전\n");
    qsort(a, s, sizeof(int), cmp);
    for (i = 0; i < s; i++) printf("%d ", a[i]);
    printf(":정렬후\n");
}
~~~

포인터의 값을 표현 *p

포인터 형 변환
~~~
*(int*)p
~~~

c++ 성적 : A+
열심히 한 보람이 있음!!!!
