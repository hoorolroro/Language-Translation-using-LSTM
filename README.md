# LSTM 기반 번역기
## LSTM(Long Short-Term Memory)의 구조  
● RNN의 한계(Long-term dependency) : 중요한 정보가 recurrent step이 계속됨에 따라 희석되는 문제 해결  
● RNN과는 달리 Cell이란 구조를 만들어 gate에 의해서 중요한 정보만 선택하고 다음 state에 전달하는 구조이다.  

<img src="https://user-images.githubusercontent.com/98728682/153707834-2ae2ae2d-3a19-4ce7-ba83-c38967ad4dff.png" width="450" height="350">  

## Basic NMT
