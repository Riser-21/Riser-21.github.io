  ---
  layout: post
  title: "나도코딩 기초"
  ---
  __변수(정수형,실수형)와 상수__
  
  변수--> 변할수 있는 값

  상수--> 변하지 않는 값

  ```
  #include <stdio.h>

  int main(void)
  {
    // 정수형 변수에 대한 예제
    /*
    int age = 12;
    printf("%d\n", age);
    age = 13;
    printf("%d\n", age);
    return 0;
    */

    // 실수형 변수에 대한 예제
    /*
    float f = 46.5f;
    printf("%.2f\n", f);
    double d = 4.428;
    printf("%.2lf\n", d);
    return 0;
    */

    const int YEAR = 2000; // 상수
    printf("태어난 년도 : %d\n" , YEAR);
    return 0;
  }
    ```
