![image](https://github.com/user-attachments/assets/8e6dee47-0363-43e2-ac0a-8069bd3624af)# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 김범모
- 리뷰어 : 이현재


# PRT(Peer Review Template)
- [o]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - Diabetes
       - ![image](https://github.com/user-attachments/assets/691b9832-5a9c-4b8f-9352-ef669c799ff6)
    - Bike Sharing Demand
       - ![image](https://github.com/user-attachments/assets/fedf1b73-3ad7-426a-b626-1f6123c6eda1)


    
- [o]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    - 코드 블럭마다 주석이 잘 달려 있음. 단계별로 markdown까지 첨부해서 가독성이 좋았음.
        - ![image](https://github.com/user-attachments/assets/582c9814-e0d3-4abe-8368-52eb2e99e2e7)
    - 특히 `.info()` method를 사용해서 dataframe의 column들의 자료형을 미리 확인해서 어떤 column들을 int나 float로 변환시켜야하는지 확인한 부분이 인상적이었음.
        - ![image](https://github.com/user-attachments/assets/d84fdd96-9399-43c5-885c-083dcdf78b51)


        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - Iteration 값 조정 과정을 구두로 설명했으나, 기록을 했으면 더 좋았을 것 같다.
        
        
- [x]  **4. 회고를 잘 작성했나요?**
    - 코드 설명 중에 배운 점을 공유했으나, 기록이 있었다면 더 좋았을 것 같다.
        
- [o]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 잘 준수하였음.
    - W 초기값을 임의로 생성할 때 `.rand()` method안에 `x_train.shape[1]`로 범용적으로 사용할 수 있도록 만들어서 인상적이었음.
        - ![image](https://github.com/user-attachments/assets/d675754d-d9c9-4287-bfee-461b0a51f755)

    


# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
리뷰어가 코드베이스를 읽을 때 코드에 대한 간결한 설명이 있어서 가독성이 좋았다.
전반적인 코드베이스의 틀은 비슷했지만, 특정 기능을 구현함에 있어서 리뷰어가 생각하지 못했던 방식으로 구현하는 부분이 인상적이었다.
```

