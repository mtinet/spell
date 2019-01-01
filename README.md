# spell

## 1. [spell.run](spell.run) 사이트를 이용해 클라우드 머신 러닝 시스템을 구동할 수 있음. 
### 작업 순서  
#### 가. Python을 컴퓨터에 먼저 설치해야 하는데 Python의 경우 2.버전과 3.버전이 있음. 요즘은 기본적으로 두 버전이 모두 설치되어 있는 경우가 있는데, 이것이 pip에서도 유효하기 때문에 pip를 설치하고나서 spell을 설치할 때 문제를 유발함  
#### 나. 이 문제를 해결하기 위해 spell 홈페이지에 나온 것처럼 그냥 pip install spell 명령을 사용하면 spell이 제대로 설치되지 않음  
#### 다. 따라서 Python이 설치된 상태에서 아래와 같은 명령으로 pip -> spell 순서로 설치를 하되 두 번째 명령어에서 꼭 pip3를 사용해야 함  

~~~~
  sudo easy_install pip  
  
  pip3 install spell  
  
  spell login  
~~~~


## 2. github와 연동하면 github에 올라와 있는 머신러닝 프로그램을 활용해 spell을 run할 수 있음  
### 가. [git-scm.com](git-scm.com) 사이트에 접속해 내 컴퓨터에 git을 설치함  
#### 윈도우의 cmd나 맥OSX의 terminal에서 내 작업폴더로 이동한 다음 아래 명령어를 이용해 해당 폴더를 git폴더로 전환함, 이 명령만으로 우리는 내 컴퓨터 안에서 버전 관리를 위한 git을 사용하게 되었음 

~~~~
  git init
~~~~

#### 이제 프로그래밍 도구(Atom, Sublime 등)를 이용해 해당폴더에 작업 파일을 만들어내고 내 컴퓨터에서 git으로 버전관리를 할 수 있게 되었음  

### 나. git을 사용할 때 사용하는 일반적인 명령어는 다음과 같음
#### 1) 내 컴퓨터에서 git 사용  

~~~~  
  git status     //변경된 파일이나 폴더가 있는지 확인함  
  
  git add *.*    //만들어 낸 파일을 git 시스템의 stage에 추가함, git add . 명령을 이용하면 여러 폴더와 파일을 한 번에 추가 가능  
  
  git commit -m '작업내용 설명'      //작업내용 설명과 함께 stage에 추가된 변경된 작업내용을 commit함, commit은 git시스템의 로컬저장소(*원격저장소 아님)에 변경내용을 최종적으로 업데이트 하는 것을 말함  
~~~~
![git의 버전 관리 구조도](https://git-scm.com/figures/18333fig0201-tn.png)


#### 2) 원격 저장소를 이용해 git 사용    
아래 과정은 github에서 먼저 원격저장소(repository)를 만들고, 그곳에서 만들어진 원격저장소의 주소를 복사하여 사용함, 이 과정을 마치면 github등의 서비스를 이용해 원격저장소를 만들고 이를 활용해 내가 제작한 프로그램의 버전관리를 할 수 있게 됨  

##### - 원격저장소의 내용 가져오기  

~~~~
  git clone github저장소주소     //github 저장소 주소에 해당하는 곳에 들어 있는 모든 폴더와 파일들을 내 컴퓨터에 다운로드 함, 자동으로 원격저장소를 origin이라는 이름으로 추가함   
    ex) git clone https://github.com/mtinet/spell.git    //해당 주소에 있는 모든 파일을 내 컴퓨터로 다운로드 함  
    
  git remote
  
  git remote add 새로운이름 github저장소주소   //이 명령을 수행하면 앞으로 새로운 이름으로 github저장소주소에 연결할 수 있음  
    ex) git remote add spell https://github.com/mtinet/spell.git     //이 작업 후에는 spell이라는 이름으로 사용 가능해짐  
    
  git remote -v  //이 명령을 통해서 현재 원격저장소의 새 이름과 연결되어 있는 주소를 확인할 수 있음  
  
  git fetch     //로컬에는 없지만 원격저장소에 있는 데이터를 모두 가져옴
    ex) git fetch origin     //clone후에 원격저장소에서 수정된 것을 모두 가져옴, 하지만 자동으로 merge를 하지 않음  
  
  git merge     //fetch명령어로 원격저장소에 가져온 데이터를 merge함, merge 할 때 merge내용을 기록하기 위해 파일을 작성하는 화면인 vim으로 넘어가는데 merge내용을 작성하고 저장 후 종료하려면 내용 작성후 esc를 누른 다음 ':wq!'를 누르고 엔터를 누르며 되고, 저장하지 않고 나가려면 esc를 누른다음 ':q!' 를 누르고 엔터를 누르며 됨, 추가 내용은 vim을 검색하길 바람  
    
  git pull     //remote를 한 번 설정하고 나면 다음부터는 이 명령어로 github에서 변경된 내용을 내 컴퓨터로 가져온 다음 자동으로 로컬과 merge함    
~~~~

##### - 내 컴퓨터 작업물을 원격저장소로 보내기  
내 컴퓨터에서 git 사용하는 방법과 동일하게 add(staging), commit작업을 하고나서 push를 해줘야 원격저장소로 정상적으로 올라감, 원격저장소는 처음에 clone했던 저장소를 말함  

~~~~
  git status     //변경된 파일이나 폴더가 있는지 확인함  
  
  git add *.*    //만들어 낸 파일을 git 시스템의 stage에 추가함, git add . 명령을 이용하면 한 번에 추가 가능  
  
  git commit -m '작업내용 설명'      //작업내용 설명과 함께 stage에 추가된 변경된 작업내용을 commit함, commit은 git시스템의 로컬저장소(*원격저장소 아님)에 변경내용을 최종적으로 업데이트 하는 것을 말함  
~~~~

~~~~
  git push       //github에 변경된 폴더와 파일들을 업로드 함, 이 작업을 하기 전에는 반드시 원격연결(remote)을 해줘야 함    
~~~~

#### 다. 일반적으로 내 컴퓨터에 먼저 git을 만들고 원격저장소(github)로 연결하는 것보다, 원격저장소(github)에 먼저 저장소를 만들고 저장소의 주소를 clone하여 작업하고 다시 push하는 것이 remote작업을 해주지 않아도 되서 작업 상 편리함  


  
   

