---
layout: single
title: "나도코딩 기초3 -> 숫자 맞히기 Up & Down"
---


 ```
 #include <stdio.h>


 int main(void)    // 맨 밑에는 return 0; 붙음 ( 여기선 생략함 )
 ```
 
 
 ```
 // 버스를 탄다고 가정. 학생/일반인으로 구분 (일반인 : 20 세)
	/*
	int age = 15;
	// if (조건) { ... } else { ... }
	if (age >= 20)
	{
		printf("일반인 입니다\n");
	}
	else
	{
		printf("학생 입니다\n");
	}
	*/
  ```
  
  
  ```
  // 초딩(8~13) / 중딩(14~16) / 고딩(17~19)로 나누면?
	// if , else if , else 알아보기

	/*
	int age = 25;
	if (age >= 8 && age <= 13)
	{
		printf("초딩입니다\n");
	}
	else if (age >= 14 && age <= 16)
	{
		printf("중딩입니다\n");
	}
	else if (age >= 17 && age <= 19)
	{
		printf("고딩입니다\n");
	}
	else
	{
		printf("학생이 아닙니다\n");
	}
	*/
  ```
  
  
  ```
  // break , continue 알아보기
	// 1번부터 30번까지 있는 반에서 1번에서 5번까지 조별 발표를 합니다.
	for (int i = 1; i <= 30; i++)
	{
		if (i >= 6)
		{
			printf("나머지 학생은 집에 가세요\n");
			break;
		}
		printf("%d 번 학생은 조별 발표 준비를 하세요\n", i);
	}
  
  
  실행 결과
  1 번 학생은 조별 발표 준비를 하세요
  2 번 학생은 조별 발표 준비를 하세요
  3 번 학생은 조별 발표 준비를 하세요
  4 번 학생은 조별 발표 준비를 하세요
  5 번 학생은 조별 발표 준비를 하세요
  나머지 학생은 집에 가세요
  ```
  
  
