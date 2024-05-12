# RL for Study(강화학습 공부 내용)
### Slot_Machine_RL_0310
    슬롯머신을 통한 강화학습
    중요한 것:ε-greedy 알고리즘(가끔씩 아무거나 뽑기)
    놀랍게도 저 엡실론그리디 알고리즘이 2번째로 좋단다..
    강화학습 구조는 그래도 DNN보단 나은 것 같다
### RL_HighSchool
    일반계 고등학교의 슬픈 인생을 강화학습을 통해 구현하였다
    처음에는 답을 아는 상태에서 코드를 짰고,
    두번째엔 가능한 경우의 수를 다 도전해보고, ε-greedy 알고리즘을 적용해보았다
### Become_a_SON + png files
    손흥민이 되어 골을 넣어보자!
    수비수가 앞에 있다
        앞으로간다->공뺏김 r=-50
        제친다 r=1
        옆으로 간다 r=0
    손흥민존에 왔다
        슛을한다 r=50
    볼 아웃 r=-50
### neural_network
    MLP를 짜보며 예전에 ResNet을 직접 구현한 기억이 났다. 당시의 기억을 떠올리며 코드를 작성해보려 했지만 막상 쉽게 되지는 않았다
    오늘 다시 복습한 내용이다
    nn.Linear(x,y) : x개의 뉴런에서 y개의 뉴런으로 이어주는 코드
    MSELoss : weight의 정답과 예측의 차의 제곱의 합을 구하는 코드
    CrossEntropyLoss : 확률의 차를 계산하는 코드
    
    코드 기본적인 구현
    
    네트워크 구현 코드
    class Net(nn.Module):
        def __init__(self):
            super(Net,self).__init__()
        def forward(self,x)
            x = ...
            return x
    
    
    훈련 코드
    optimizer.zero_grad() # 초기화
    output = model(x) # 예측
    loss = criterion(output,y) # 손실함수 계산
    loss.backward() # 손실함수 미분
    optimizer.step() # 경사에서 한 단계 하강하기
