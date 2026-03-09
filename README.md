# chap02-2-1-



📄 README.md 

````markdown
Computer Vision 과제

1. 과제 설명
OpenCV 라이브러리를 이용하여 이미지 파일을 읽고 화면에 출력하는 프로그램을 작성하였다.

사용 라이브러리  
- OpenCV

개발 환경  
- Visual Studio  
- Windows 10  


2. 프로그램 소스 코드

```cpp
#include <opencv2/opencv.hpp>
#include <iostream>

using namespace cv;
using namespace std;

int main() {

    cout << "Hello OpenCV " << CV_VERSION << endl;

    Mat img;

    img = imread("myphoto.jpg");

    if (img.empty()) {
        cerr << "Image load failed!" << endl;
        return -1;
    }

    namedWindow("image");
    imshow("image", img);

    waitKey();

    return 0;
}
````


3. 코드 설명

1) OpenCV 헤더 파일 포함

```cpp
#include <opencv2/opencv.hpp>
```

OpenCV 라이브러리를 사용하기 위한 헤더 파일을 포함한다.


2) 이미지 객체 선언

```cpp
Mat img;
```

이미지를 저장하기 위한 변수 선언이다.


3) 이미지 파일 읽기

```cpp
img = imread("myphoto.jpg");
```

imread 함수는 이미지 파일을 읽어와 Mat 객체에 저장한다.


4) 이미지 로드 확인

```cpp
if (img.empty())
```

이미지가 정상적으로 읽히지 않았을 경우 오류 메시지를 출력한다.


5) 이미지 창 생성

```cpp
namedWindow("image");
```

이미지를 표시할 창을 생성한다.


6) 이미지 출력

```cpp
imshow("image", img);
```

이미지를 화면에 출력한다.


7) 키 입력 대기

```cpp
waitKey();
```

사용자가 키를 누를 때까지 창이 닫히지 않도록 한다.


4. 실행 결과

프로그램 실행 시 콘솔창에 OpenCV 버전이 출력된다.

```
Hello OpenCV 4.x.x
```

그리고 새로운 창이 생성되며 myphoto.jpg 이미지가 화면에 출력된다.




