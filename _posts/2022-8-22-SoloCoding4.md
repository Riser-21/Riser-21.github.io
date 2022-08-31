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

__전달값이 없는 함수__
```
#include <stdio.h>

// 선언
void p(int num);

 void function_without_return();
int function_with_return();
void function_without_params();

int main(void)
{
	// 함수 종류
	// 반환값이 있는 함수
/*	int ret = function_with_return();
	p(ret);
*/	
	// 파라미터(전달값)가 없는 함수
	function_without_params();
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

void function_without_params()
{
	printf("전달값이 없는 함수입니다.\n");
}
```


__전달값이 있는 함수__

```
#include <stdio.h>

// 선언
void p(int num);

void function_without_return();
int function_with_return();
void function_without_params();
void function_with_params(int num1, int num2, int num3);

int main(void)
{
	// 함수 종류
	// 반환값이 있는 함수
/*	int ret = function_with_return();
	p(ret);
*/	
/*	// 파라미터(전달값)가 없는 함수
	function_without_params();
*/
	// 전달값이 있는 함수
	function_with_params(10,20,30);
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

void function_without_params()
{
	printf("전달값이 없는 함수입니다.\n");
}
void function_with_params(int num1, int num2, int num3)
{
	printf("전달값이 있는 함수이며, 전달받은 값은 %d, %d, %d 입니다\n", num1, num2, num3);
}
```

__반환값과 전달값이 있는 함수__

```
#include <stdio.h>

// 선언
void p(int num);

//void function_without_return();

int function_with_return();
void function_without_params();
void function_with_params(int num1, int num2, int num3);

int	apple(int total, int ate); // 전체  total 개에서 ate 개를 먹고 남은 수를 반환

int main(void)
{
	// 함수 종류
	// 반환값이 있는 함수
/*	int ret = function_with_return();
	p(ret);
*/	
/*	// 파라미터(전달값)가 없는 함수
	function_without_params();
*/
/*	// 전달값이 있는 함수
	function_with_params(10,20,30);
*/
	// 파라미터(전달값)도 받고, 반환값이 있는 함수
//	int ret = apple(5, 2); // 5개의 사과 중에서 2개를 먹었어요.
//	printf("사과 5개 중에 2개를 먹으면? %d 개가 남아요\n",ret);
	printf("사과 %d 개 중에 %d 개를 먹으면? %d 개가 남아요\n", 10, 4, apple(10, 4));
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

void function_without_params()
{
	printf("전달값이 없는 함수입니다.\n");
}
void function_with_params(int num1, int num2, int num3)
{
	printf("전달값이 있는 함수이며, 전달받은 값은 %d, %d, %d 입니다\n", num1, num2, num3);
}
int	apple(int total, int ate)
{
	printf("전달값과 반환값이 있는 함수입니다\n");
	return total - ate;
}
```

__함수를 이용한 계산기__

```
#include <stdio.h>

// 선언
void p(int num);

//void function_without_return();

int add(int num1, int num2);
int sub(int num1, int num2);
int mul(int num1, int num2);
int div(int num1, int num2);

int main(void)
{
// 계산기 함수
	int num = 2;
	num = add(num, 3);
	p(num);

	num = sub(num, 1); // 빼기
	p(num);

	num = mul(num, 3); // 곱하기
	p(num);

	num = div(num, 6); // 나누기
	p(num);
	return 0;
}

// 정의
void p(int num)
{
	printf("num 은 %d 입니다\n", num);
}
int add(int num1, int num2)
{
	return num1 + num2;
}
int sub(int num1, int num2)
{
	return num1 - num2;
}
int mul(int num1, int num2)
{
	return num1 * num2;
}
int div(int num1, int num2)
{
	return num1 / num2;
}
```

__함수를 이용한 프로젝트!!__

```
#include <stdio.h>
#include <time.h>

// 선언
int getRandomNumber(int level);
void showQuestion(int level, int num1, int num2);
void success();
void fail();
int main(void)
{
	// 문이 5개가 있고, 각 문마다 점점 어려운 수식 퀴즈가 랜덤으로 출제
	// 맞히면 통과, 틀리면 실패

	srand(time(NULL));
	int count = 0; // 맞힌 문제 개수
	for (int i = 1; i <= 5; i++)
	{
		// x * y = ?
		int num1 = getRandomNumber(i);
		int num2 = getRandomNumber(i);
		showQuestion(i, num1, num2); //	printf("%d x $d ?", num1, num2); 로도 가능

		int answer = -1;
		scanf_s("%d", &answer);
		if (answer == -1)
		{
			printf("프로그램을 종료합니다\n");
			exit(0); // break는 이 for문을 탈출, exit는 프로그램을 바로 끝냄
		}
		else if (answer == num1 * num2)
		{
			// 성공
			success();
			count++;
		}
		else
		{
			// 실패
			fail();
		}
		
	}

	printf("\n\n 당신은 5개의 비밀번호 중 %d 개를 맞췄습니다", count);
	return 0;
}

int getRandomNumber(int level)
{
	return rand() % (level * 7) + 1;
}
void showQuestion(int level, int num1, int num2)
{
	printf("\n\n\n########## %d 번째 비빌번호 ########\n", level);
	printf("\n\t%d x %d 는?\n\n", num1, num2);
	printf("################################\n");
	printf("\n비밀번호를 입력하세요 (종료 : -1) >> ");
}
void success()
{
	printf("\n >> Good! 정답입니다 \n");
}
void fail()
{
	printf("\n >> 땡! 틀렸습니다 \n");
}
```
