---
layout: single
title: "나도코딩 기초4 -> 비밀번호 마스터"
---

```
#include <stdio.h>
int main(void)
{
	// function
	// 계산기

	int num = 2;
	printf("num은 %d 입니다\n", num); // 2

	// 2 + 3 은?
	num = num + 3;
	printf("num은 %d 입니다\n", num); // 5

	// 5 - 1 은?
	num -= 1; // num = num - 1;
	printf("num은 %d 입니다\n", num); // 4

	// 4 x 3 은?
	num *= 3;
	printf("num은 %d 입니다\n", num); // 12

	// 12 / 6 은?
	num /= 6;
	printf("num은 %d 입니다\n", num); // 2

	return 0;
}
```

__함수를 이용해서 간략하게 작성해보기__
```
#include <stdio.h>

// 선언
void p(int num);

int main(void)
{

	// function
	// 계산기

	int num = 2;
	p(num); // p라는 함수를 호출하고 num 라는 변수의 값을 던지겠다

	// 2 + 3 은?
	num = num + 3;
	p(num);

	// 5 - 1 은?
	num -= 1; // num = num - 1;
	p(num);

	// 4 x 3 은?
	num *= 3;
	p(num);

	// 12 나누기 6 은?
	num /= 6;
	p(num);

	return 0;
}

// 정의
void p(int num)
{
	printf("num 은 %d 입니다\n", num);
}
```

__함수의 형태__
```
반환형 함수이름(전달값)       
{
}

예시
void 함수이름(int num1, int num2, char c, float f)
{
}
```

__반환값이 없는 함수__
```
#include <stdio.h>

// 선언
void function_without_return(); // void 는 아무것도 반환하지 않겠다를 뜻함.

int main(void)
{
	// 함수 종류
	// 반환값이 없는 함수
	function_without_return();
	

	return 0;
}

// 정의
void function_without_return()
{
	printf("반환값이 없는 함수입니다");
}
```

__반환값이 있는 함수__
```
#include <stdio.h>

// 선언
//void function_without_return();
int function_with_return();
void p(int num);

int main(void)
{
	// 함수 종류
	// 반환값이 있는 함수
	int ret = function_with_return();
	p(ret);
	

	return 0;
}

// 정의
void p(int num)
{
	printf("num 은 %d 입니다", num);
}

int function_with_return()
{
	printf("반환값이 있는 함수입니다\n");
	return 10;
}
```


