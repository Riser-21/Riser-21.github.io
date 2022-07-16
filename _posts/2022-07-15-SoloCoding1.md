---
layout: single
title: "나도코딩 기초 -> 경찰서 조서  "
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
  int age = 12;  // age 가 변수임
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
 
 printf -> 연산
 ```
 int add = 3 + 7; // 10
	//printf("3 + 7 = %d\n", add);
	printf("%d +%d = %d\n", 3, 7, 3 + 7);  // 이렇게 변수를 사용하지 않고 바로 계산가능
	return 0;
 ```
 
 # scanf 사용법
 
 scanf -> 키보드 입력을 받아서 저장
 ```
 int input;
	printf("값을 입력하세요 : ");
	scanf_s("%d", &input);
	printf("입력값 : %d\n", input);
	return 0;

 int one, two, three;
	printf("3개의 정수를 입력하시오 : ");
	scanf_s("%d %d %d", &one, &two, &three);
	printf("첫번째 값 : %d\n", one);
	printf("두번째 값 : %d\n", two);
	printf("세번째 값 : %d\n", three);
	return 0;
  
  // 문자(한 글자), 문자열(여러 글자)
	char c = 'A'; // 문자
	printf("%c\n", c);

	char str[256]; // 배열을 이용한 문자열
	scanf_s("%s\n", str, sizeof(str));
	printf("%s\n'", str);

	return 0;
  ```
  
 # 프로젝트 
 __// 경찰관이 범죄자의 정보를 입수 (조서 작성)__
  
	// 이름? 나이? 몸무게? 키? 범죄명?
  ```
	char name[256];
	printf("이름이 뭐예요? ");
	scanf_s("%s", name, sizeof(name));

	int age;
	printf("몇살이예요? ");
	scanf_s("%d", &age);

	float weight;
	printf("몸무게는 몇 kg 이예요? ");
	scanf_s("%f", &weight);

	double height;
	printf("키는 몇 cm 인가요? ");
	scanf_s("%lf", &height);

	char what[256];
	printf("무슨 범죄를 저질렀어요? ");
	scanf_s("%s", what, sizeof(what));

	// 조서 내용 출력
	printf("\n\n--- 범죄자 정보 ---\n\n");
	printf(" 이름		: %s\n", name);
	printf(" 나이		: %d\n", age);
	printf(" 몸무게		: %.2f\n", weight);
	printf(" 키			: %.2lf\n", height);
	printf(" 범죄		: %s\n", what);


	return 0;
  
  ```
  
  
  
  
  
  
  
