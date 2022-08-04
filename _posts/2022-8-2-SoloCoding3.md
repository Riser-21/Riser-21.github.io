---
layout: single
title: "나도코딩 기초3 -> 숫자 맞히기 Up & Down"
---

 ```
 #include <stdio.h>


 int main(void)    // 맨 밑에는 return 0; 붙음 ( 여기선 생략함 )
 ```
 
 # 4-0. 버스를 탄다고 가정. 학생/일반인으로 구분 (일반인 : 20 세)
 
  ```
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
  
  ```
  
 
  # 4-1. if , else if , else 알아보기
  
  // 초딩(8-13세) , 중딩(14-16세) , 고딩(17-19세)로 나누면?
  
  ```
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
  ```
  
 
  # 4-2. break , continue 알아보기
  
	1번부터 30번까지 있는 반에서 1번에서 5번까지 조별 발표를 합니다.
 
  ```
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
  
  
  # 4-3.
  
  ```
  for (int i = 1; i <= 30; i++)
	{
		if (i >= 6 && i <= 10)
		{
			if (i == 7)
			{
				printf("%d 번 학생은 아파서 결석입니다\n", i);
				continue;
			}
			printf("%d 번 학생은 조별 발표 준비를 하세요\n", i);
		}
	}
  
  
  실행결과
  6 번 학생은 조별 발표 준비를 하세요
  7 번 학생은 아파서 결석입니다
  8 번 학생은 조별 발표 준비를 하세요
  9 번 학생은 조별 발표 준비를 하세요
  10 번 학생은 조별 발표 준비를 하세요
  ```
  
  # 4-4.  && 와 || 알아보기 && 는 and 이고 || 는 or 의 개념
  
  ```
	int a = 10;
	int b = 10;
	int c = 12;
	int d = 13;
	if (a == b || c == d)
	{
		printf("a 와 b, 혹은 c와 d가 같습니다\n");
	}
	else
	{
		printf("값이 서로 다르네요\n");
	}
  ```

 # 4-5. Switch Case 문 -> break 쓰기
 
  ```
  + #include <time.h>
  
  srand(time(NULL));  // srand : 랜덤으로 숫자뽑기 , srand(time(NULL)); -> 난수 초기화하기
	int i = rand() % 3; // 0 ~ 2 반환 (시작 값이 0부터임)
	switch (i)
	{
	case 0:printf("가위\n"); break;
	case 1:printf("바위\n"); break;
	case 2:printf("보\n"); break;
	default:printf("몰라요\n"); break;
	}
  ```
  
  # 4-6. Up and Down 프로젝트 
  ```
  	
  #include <stdio.h>
  #include <time.h>

  int main(void)
  {  
	srand(time(NULL));
	int num = rand() % 100 + 1; // 1 ~ 100 사이의 숫자
	printf("숫자 : %d\n", num);
	int answer = 0; // 정답
	int chance = 5; // 기회 수
	while (chance > 0)
	{
		printf("남은 기회 %d 번\n", chance--);
		printf("숫자를 맞혀보세요 (1~100) : ");
		scanf_s("%d", &answer);

		if (answer > num)
		{
			printf("DOWN ↓ \n\n");
		}
		else if (answer < num)
		{
			printf("UP ↑ \n\n");
		}
		else if (answer == num)
		{
			printf("정답입니다 !\n\n");
			break;
		}
		else
		{
			printf("알 수 없는 오류가 발생했어요\n"); // 보통은 나올일 없음
		}

		if (chance == 0)
		{
			printf("모든 기회를 다 쓰셨네요. 아쉽게 실패했습니다\n");
			break;
		}
	}
		return 0;
}
  ```
  
  
