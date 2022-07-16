---
layout: single
title: "나도코딩 기초"
---

  # __변수(정수형,실수형)와 상수__
  
변수--> 변할수 있는 값

상수--> 변하지 않는 값

 ```
#include <stdio.h>

int main(void)
{
  // 정수형 변수에 대한 예제
  /*
  int age = 12;
  printf("%d\n", age);  // 정수형엔 %d를 넣는다
  age = 13;
  printf("%d\n", age);
  return 0;
  */

  // 실수형 변수에 대한 예제
  /*
  float f = 46.5f;
  printf("%.2f\n", f); // 실수형엔 %f를 쓰며 소수점 계산할땐 .을 씀 (ex: 소수점 둘째 자리까지 표기 -> .2f -> 셋째 짜리에서 반올림 해서 둘째 자리까지만 표기됨)
  double d = 4.428;
  printf("%.2lf\n", d);
  return 0;
  */

    const int YEAR = 2000; // 상수
    printf("태어난 년도 : %d\n" , YEAR);
    return 0;
  }
 ```
 
 # printf 사용법
 
 ```
 int add = 3 + 7; // 10
	//printf("3 + 7 = %d\n", add);
	printf("%d +%d = %d\n", 3, 7, 3 + 7);
	return 0;
 ```
