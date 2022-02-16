# Visual-Studio-Code
## python 설치
```
python3.7, 64-bit 설치
cmd에서 Opencv-python 설치
> pip install opencv-python
> pip install opencv-python==4.1.0.25
>python
>>>import cv2
>>>cv2.__version__
>>>exit()
```
## VS Code 설치
```
https://code.visualstudio.com/
다운로드 후 설치 진행
Extensions 뷰에서 Python 설치

[View](보기) -> [Command Palette...]메뉴 선택후 "Python: Select Interprter"입력 & 선택
설치된 Python 인터프리터 선택

Extensions 뷰에서 "Korean" 검색해서 설치

따로 파일을 만들고 새 파일에서 파일 이름 입력(test.py)
-import cv2
-print('Hello OPencv', cv2.__version__)

[실행] -> [디버깅 없이 실행(CTRL+F5)]

사진을 따로 찾은 다음 우클릭 -> (이미지를 다른 이름으로 저장) -> 내PC -> 로컬 디스트 -> 자신의 파일 -> 저장(같은 곳에 저장해야 이미지를 불러올수 있다)
```

## Matplotlib을 이영한 영상 출력
```
-cmd에서 설치
>pip install matplotilb

-Matplotilb을 이용하여 영상 출력하기

import matplotlib.pyplot as plt
import cv2

imgBGR = cv2.imread('cat.bmp')
imgRGB = cv2.cvtColor(imgBGR, cv2.COLOR_BGR2RGB)

plt.axis('off')
plt.imshow(imgRGB)
plt.show()

imgGray = cv2.imread('cat.bmp', cv2.IMREAD_GRAYSCALE)

plt.axis('off')
plt.imshow(imgGray, cmap = 'gray')
plt.show()
-------------영상 출력--------------

-창 하나에 여러 개의 이미지 출력하기

import matplotlib.pyplot as plt
import cv2

imgBGR = cv2.imread('cat.bmp')
imgRGB = cv2.cvtColor(imgBGR, cv2.COLOR_BGR2RGB)
imgGray = cv2.imread('cat.bmp', cv2.IMREAD_GRAYSCALE)

plt.subplot(121), plt.axis('off'), plt.imshow(imgRGB)
plt.subplot(122), plt.axis('off'), plt.imshow(imgGray, cmap='gray')
plt.show()

{subplot(121)에 121은 (1):1줄, (2): 두칸, (1): 첫 칸}
