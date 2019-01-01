# spell

## [spell.run](spell.run) 사이트를 이용해 클라우드 머신 러닝 시스템을 구동할 수 있음. 
### 작업 순서  
1. Python을 컴퓨터에 먼저 설치해야 하는데 Python의 경우 2.버전과 3.버전이 있음. 요즘은 기본적으로 두 버전이 모두 설치되어 있는 경우가 있는데, 이것이 pip에서도 유효하기 때문에 pip를 설치하고나서 spell을 설치할 때 문제를 유발함  
2. 이 문제를 해결하기 위해 spell 홈페이지에 나온 것처럼 그냥 pip install spell 명령을 사용하면 spell이 제대로 설치되지 않음  
3. 따라서 Python이 설치된 상태에서 아래와 같은 명령으로 pip -> spell 순서로 설치를 하되 두 번째 명령어에서 꼭 pip3를 사용해야 함  

~~~~
  sudo easy_install pip  
  pip3 install spell  
  spell login  
~~~~


### github와 연동하면 github에 올라와 있는 머신러닝 프로그램을 활용해 spell을 run할 수 있음  
1. [git-scm.com](git-scm.com) 사이트에 접속해 내 컴퓨터에 git을 설치함  
2. 윈도우의 cmd나 맥OSX의 terminal에서 내 작업폴더로 이동한 다음 아래 명령어를 이용해 해당 폴더를 git폴더로 전환함

~~~~
  git init
~~~~

3. 프로그래밍 도구(Atom, Sublime 등)를 이용해 해당폴더에 작업 파일을 만들어냄  
