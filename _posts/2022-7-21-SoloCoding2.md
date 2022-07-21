---
layout: single
title: "나도코딩 기초2 -> 피라미드 쌓기"
---

```
 #include <stdio.h>


 int main(void)    // 맨 밑에는 return 0; 붙음 ( 여기선 생략함 )
 ```
 
 ```
 int b = 20;
	// ++은 b=b+1 과 같다
	printf(" b 는 %d\n", ++b); // ++을 먼저 수행하고 문장을 끝내라
	printf(" b 는 %d\n", b++); // 다음 문장으로 넘어갈때 ++을 수행
	printf(" b 는 %d\n", b);  // 22가 출력됨
  ```
  
  
  ```
  int i = 1;
	printf("Hello World %d\n", i++); // 1
	printf("Hello World %d\n", i++); // 2
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++);
	printf("Hello World %d\n", i++); //10
  ```
  
  
  ```
  // 반목문
	// for, while, do while 3가지 있음

	// for(선언; 조건; 증감) {	}
	/*
	for (int i = 1; i <= 10; i++)  // i가 10까지만 도출됨
	{
		printf("Hello World %d\n", i);
	}
	*/

	// while (조건) {  }
	/*
	int i = 1;
	while (i <= 10)
	{
		printf("Hello World %d\n", i++);
		// i++; (위에서 printf("Hello World %d\n", i); 로 했을경우 i++ 을 따로 작성
	}
	*/

	// do {  } while (조건);
	
	/*
	int i = 1;
	do {
		printf("Hello World %d\n", i++);
	} while (i <= 10);
	*/
  ```
  
  
  ```
  // 2중 반복문
	/*
	for (int i = 1; i <= 3; i++)
	{
		printf("첫 번째 반복문 : %d\n", i);

		for (int j = 1; j <= 5; j++)
		{
			printf("     두 번째 반복문 : %d\n", j);
		}
	}
	*/
  ```
  ```
  /* 결과 
첫 번째 반복문 : 1
     두 번째 반복문 : 1
     두 번째 반복문 : 2
     두 번째 반복문 : 3
     두 번째 반복문 : 4
     두 번째 반복문 : 5
첫 번째 반복문 : 2
     두 번째 반복문 : 1
     두 번째 반복문 : 2
     두 번째 반복문 : 3
     두 번째 반복문 : 4
     두 번째 반복문 : 5
첫 번째 반복문 : 3
     두 번째 반복문 : 1
     두 번째 반복문 : 2
     두 번째 반복문 : 3
     두 번째 반복문 : 4
     두 번째 반복문 : 5
*/
  ```
  
  
  ```
  // 구구단 만들기
	// 2 x 1 = 2
	// 2 x 2 = 4
	// 2 x 3 = 6
	/*
	for (int i = 2; i <= 9; i++)  // i 는 첫번째 숫자
	{
		printf("%d단 계산\n", i);
		for (int j = 1; j <= 9; j++)  // j는 두번째 숫자
		{
			printf("  %d x %d = %d\n", i, j, i*j);
		}
	}
  ```
  
  
  ```
  /*
  
	*
	**
	***
	****
	*****
  
	*/

	for (int i = 0; i < 5; i++)
	{
		for (int j = 0; j <= i; j++)
		{
			printf("*");
		}
		printf("\n");
	}
  ```
  
  
  ```
  /*
S 는 공백 (앞에 S가 있다고 생각하기

             *                   SSSS*
            **                   SSS**
           ***      ->           SS***
          ****                   S****
         *****                   *****
         
*/

	for (int i = 0; i < 5; i++)
	{
		for (int j = i; j < 5 - 1; j++)
		{
			printf("S"); // printf(" ");
		}
		for (int k = 0; k <= i; k++)
		{
			printf("*");
		}
		printf("\n");
	}
  ```
  
#__피라미드를 쌓아라 - 프로젝트__ 

```
/*  똑같이 앞에 S가 있다 생각하기
             *                   SSSS*
            ***                  SSS***
           *****      ->         SS*****
          *******                S*******
         *********               *********
*/
#include <stdio.h>

int main(void)
{
	int floor;
	printf("몇 층으로 쌓겠느냐?");
	scanf_s("%d\n", &floor);
	for (int i = 0; i < floor; i++)
	{
		for (int j = i; j < floor - 1; j++)
		{
			printf("S");  // printf(" ");
		}
		for (int k = 0; k <= i * 2 + 1; k++)
		{
			printf("*");
		}
		printf("\n");
	}
  ```
  
