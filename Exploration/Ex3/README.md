# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 김국화
- 리뷰어 : 이호창


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부  
            - 셀카 사진에 고양이 수염 스티커가 매우 잘 들어가 있습니다!  
              ![image](https://github.com/user-attachments/assets/a9a255f9-b8fd-46b3-8de2-18ca3c7d275d)  

    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
            - 이미지 범위에 벗어났을 경우 어떻게 조정했는지 그 작동 원리를 이해하기 쉽게 주석을 달았습니다!  
              ![image](https://github.com/user-attachments/assets/65b97da9-840d-4209-b0bb-d1d93cf9b566)  


- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부  
            - 없습니다..ㅎ  
        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
            - 회고 작성 안 하셨습니다!  
        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
            - 반복문을 통해 중복 작업을 최소화하였습니다!  
              ![image](https://github.com/user-attachments/assets/4bd1bb67-3b47-4275-919e-5000c83b7561)



-----  
### 회고(참고 링크 및 코드 개선)

##### 리뷰어의 회고를 작성합니다.
##### 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
##### 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.  

#### 개선한 코드!
```
POS = landmark[30]
for dlib_rect, landmark in zip(dlib_rects, list_landmarks):
    print(POS)    # 코의 index값
    x = POS[0]    # 이미지에서 코의 x축 좌표값
    y = POS[1]    # 이미지에서 코의 y축 좌표값
    w = dlib_rect.width()    # bounding box의 가로 픽셀수
    h = dlib_rect.height()    # bounding box의 세로 픽셀수
    print (f'(x,y) : ({x},{y})')
    print (f'(w,h) : ({w},{h})')
```
list_landmarks의 경우 크기가 1이라 현재 코드에서 이상한 점이 발생하지 않았지만, 사진 내에 사람이 여러명이라면 list_landmarks의 크기가 사람 수가 됩니다. 그럴 경우 위에서 저장된 landmark에 해당되는 사람의 위치가 중복으로 들어가서 결과가 이상하게 나올 수 있습니다.  
따라서 아래와 같이 수정해야합니다!
```
for dlib_rect, landmark in zip(dlib_rects, list_landmarks):
    print(landmark[30])   # 코의 index값
    x = landmark[30][0]    # 이미지에서 코의 x축 좌표값
    y = landmark[30][1]    # 이미지에서 코의 y축 좌표값
    w = dlib_rect.width()    # bounding box의 가로 픽셀수
    h = dlib_rect.height()    # bounding box의 세로 픽셀수
    print (f'(x,y) : ({x},{y})')
    print (f'(w,h) : ({w},{h})')
```
