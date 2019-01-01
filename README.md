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

3. git init 명령만으로 내 컴퓨터 안에서 버전 관리를 위한 git을 사용하게 되었음  
4. 프로그래밍 도구(Atom, Sublime 등)를 이용해 해당폴더에 작업 파일을 만들어냄  
5. 일반적인 명령어는 다음과 같음
~~~~
  git status     //변경된 파일이나 폴더가 있는지 확인함  
  git add *.*    //만들어 낸 파일을 git 시스템의 stage에 추가함, git add . 명령을 이용하면 한 번에 추가 가능  
  git commit -m '작업내용 설명'      //작업내용 설명과 함께 stage에 추가된 변경된 작업내용을 commit함, commit은 git시스템의 저장소에 변경내용을 최종적으로 업데이트 하는 것을 말함  
  git remote
  git remote add 새로운이름 github저장소주소   //이 명령을 수행하면 앞으로 새로운 이름으로 github저장소주소에 연결할 수 있음  
    ex) git remote add spell https://github.com/mtinet/spell.git     //이 작업 후에는 spell이라는 이름으로 사용 가능해짐  
  git remote -v  //이 명령을 통해서 현재 연결되어 있는 원격저장소의 새 이름과 주소를 확인할 수 있음  
  git push       //github에 변경된 폴더와 파일들을 업로드 함, 이 작업을 하기 전에는 반드시 원격연결(remote)을 해줘야 함    
  git clone github저장소주소     //github 저장소 주소에 해당하는 곳에 들어 있는 파일들을 내 컴퓨터에 다운로드 함  
    ex) git clone https://github.com/mtinet/spell.git    //해당 주소에 있는 모든 파일을 내 컴퓨터로 다운로드 함  
  git pull     //remote를 한 번 설정하고 나면 다음부터는 이 명령어로 github에서 변경된 내용을 내 컴퓨터로 가져올 수 있음  
  ~~~~
6. 일반적으로 내 컴퓨터에 먼저 git을 만들고 원격저장소(github)로 연결하는 것보다, 원격저장소(github)에 먼저 저장소를 만들고 저장소의 주소를 clone하여 작업하고 다시 push하는 것이 remote작업을 해주지 않아도 되서 작업 상 편리함  


  
   

