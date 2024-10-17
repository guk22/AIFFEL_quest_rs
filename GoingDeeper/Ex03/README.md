# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 김국화
- 리뷰어 : 오수연


# PRT(Peer Review Template)
- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - <img width="330" alt="image" src="https://github.com/user-attachments/assets/06d1bf31-42d3-4fbd-9225-c7e5f7ceb309">
    - <img width="457" alt="image" src="https://github.com/user-attachments/assets/37d7a592-0b32-4389-9176-d4c2faa35810">
    - cam과 grad-cam의 bbox, iou까지 다 하셨습니다.
    
- [O]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - <img width="641" alt="image" src="https://github.com/user-attachments/assets/a1f8ba95-2439-4c81-9170-9e56008a2bdf">
    - 데이터 증강 후 적용 모델 비교를 시각화 해서 보기 쉽게 해주셨습니다
    - <img width="657" alt="image" src="https://github.com/user-attachments/assets/2b3199bd-db4d-498d-adba-e45a8a0119c4">
    - grad-cam을 레이어별로 시각화해서 레이어별로 포커싱 된 부분을 이해하기 쉽게 해주셨습니다.
        
- [O]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - <img width="550" alt="image" src="https://github.com/user-attachments/assets/53abf90c-9bbe-491a-90f6-b767513ecb50">
    - grad-cam의 conv5_block3_out레이어가 아닌 다른 부분인거 같다고 구두로 설명주셨습니다.
        
- [O]  **4. 회고를 잘 작성했나요?**
    - <img width="226" alt="image" src="https://github.com/user-attachments/assets/92388331-0461-42dd-bcad-0c7b3ada61c0">
    - 다양한 실험을 하시느라 시간의 부족함이 있으셨던거 같습니다.
        
- [O]  **5. 코드가 간결하고 효율적인가요?**
    - <img width="643" alt="image" src="https://github.com/user-attachments/assets/29a3f52d-96e3-4f8a-a2d2-bb59dcee3c4e">
    - 맨위에 결과내용 정리한 걸 올려주셨는데 이렇게하니깐 보는 입장에서 더 보기 좋은거 같아서 다음부턴 저도 참고해서 작성해야겠습니다:)


# 회고(참고 링크 및 코드 개선)
```
제가 해보고 싶었던 실험(데이터 증강, grad-cam의 레이어별로 보기)등을 다 진행주셔서 제가 해보지 않았는데 볼 수 있어서 좋았습니다.
```
