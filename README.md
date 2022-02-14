# LSTM 기반 번역기
## LSTM(Long Short-Term Memory)의 구조  
● RNN의 한계(Long-term dependency) : 중요한 정보가 recurrent step이 계속됨에 따라 희석되는 문제가 있다.

● LSTM에서는 Cell이란 구조를 만들어 gate에 의해서, 중요한 정보만 선택하고 다음 state에 전달하는 구조로 RNN의 문제점을 개선하였다.

<img src="https://user-images.githubusercontent.com/98728682/153707834-2ae2ae2d-3a19-4ce7-ba83-c38967ad4dff.png" width="430" height="320">

#

<img src="https://user-images.githubusercontent.com/98728682/153808548-77bebf4b-d719-4a1d-82f4-404772f92b48.png" width="520" height="360">  

● Forget gate layer은 Cell state에서 어떤 정보를 지워버릴지 결정한다.  

● Candidate laye에서 모은 일부 정보만 Cell state에 들어간다.

● Input gate layer은 Candidate vector에서 뭘 넣어줄지 결정한다.  

● 마지막으로 Cell state에서 저장된 핵심 데이터를 hidden state로 정보가 전달된다.

## Basic NMT(Neural Machine Translation)의 구조
<img src="https://user-images.githubusercontent.com/98728682/153708836-a425b499-08de-4125-8074-7f3616e96217.png" width="610" height="400">
● Encoder  

- 입력으로 들어오는 문장을 LSTM을 이용해 잘 압축한다.  

- 입력의 마지막 단어를 통해 나온 hidden state가 최종적으로 사용될 encoded layer이다.  

● Decoder  
- Encoding된 정보 vector를 이용해 출력 문장으로 하나하나 풀어낸다.  

- 입력의 마지막 hidden state를 초기값으로 사용한다.  

## 프로그램 시현  
● 영어와 프랑스어 쌍으로 이루어진 sequence to sequence dataset를 학습한다.  

● 학습한 모델로 아래와 같은 결과가 나왔다.  
\
<img src="https://user-images.githubusercontent.com/98728682/153710493-9f1f8b76-80cd-479c-a2d9-b31043cb05a3.png" width="500" height="100">
