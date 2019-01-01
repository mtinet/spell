# spell

## spell.run 사이트를 이용해 클라우드 머신 러닝 시스템으 구동할 수 있음. 
### 작업 순서  
1. Python을 컴퓨터에 먼저 설치해야 하는데 Python의 경우 2.버전과 3.버전이 있음. 요즘은 기본적으로 두 버전이 모두 설치되어 있는 경우가 있는데, 이것이 pip에서도 유효하기 때문에 pip를 설치하고나서 spell을 설치할 때 문제를 유발함  
2. 이 문제를 해결하기 위해 spell 홈페이지에 나온 것처럼 그냥 pip install spell 명령을 사용하면 spell이 제대로 설치되지 않음  
3. 따라서 아래와 같은 순서로 설치를 하되 두 번째 명령어에서 꼭 pip3를 사용해야 함  

  sudo easy_install pip  
  pip3 install spell  
  spell login  
