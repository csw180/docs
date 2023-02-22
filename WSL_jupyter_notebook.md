### WSL2 이용한 Python Jupyter 설치 및 내·외부에서 접속
---------------------------------------------------------

1. pip 설치
```
sudo apt install python3-pip
```

2. jupyter 설치
```
sudo pip3 install jupyter
```

3. jupyter 설치 확인
```
jupyter --version


Selected Jupyter core packages...
IPython          : 8.8.0
ipykernel        : 6.20.2
ipywidgets       : 8.0.4
jupyter_client   : 7.4.9
jupyter_core     : 5.1.5
jupyter_server   : 2.1.0
jupyterlab       : not installed
nbclient         : 0.7.2
nbconvert        : 7.2.9
nbformat         : 5.7.3
notebook         : 6.5.2
qtconsole        : 5.4.0
traitlets        : 5.8.1
```
4. notebook 실행
```
jupyter notebook
...
..
    To access the notebook, open this file in a browser:
        file:///home/romantic/.local/share/jupyter/runtime/nbserver-1142-open.html
    Or copy and paste one of these URLs:
        http://localhost:8888/?token=9aed81671d4d6e3647a81981100c964181509ac705fdabf8
     or http://127.0.0.1:8888/?token=9aed81671d4d6e3647a81981100c964181509ac705fdabf8
...


```
* 위 URL 을 브라우져에서 입력하여 접속
* jupyter notebook을 백그라운드로 실행시키기 위해서는 
```
nohup jupyter notebook & 
```
* cat nohup.out 를 해서 접속 URL 확인할것


