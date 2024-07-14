# ネップロ最終制作課題

## 概要  
Pythonのsocketとpygame-guiを用いて作成した  
一対一通信の神経衰弱アプリです。  

## 役割分担
riporippo ... **GUI作成＆連携**   
Haruta-Yamanaka ... **通信機能＆ゲーム内部**     

## プログラム解説
* **main.py**  
  GUIを表示するスクリプト  
  TCPClient.pyのClinetクラスを作って  
  card情報をもらい、画面更新を行います。  
* **main2.py**  
  main.pyと一緒です。
  TCPClient2.pyのClientクラスを使っています。  
* **TCPClient.py**  
  serverとやりとりをします  
  GUIからの入力を受け付けて、server側に送り  
  結果をserverから受け取って、main.pyに情報を提供する役割を担っています。　　
* **TCPClinet2.py**  
  TCPClient.pyと一緒です。  
* **TCPServer.py**
  二つのクライアントからの接続確立  
  ゲーム進行機能、cardクラスやplayerクラス  
  などの定義を行うスクリプト
  ゲームの根幹を担います。

## ゲームの進行方法  
1. Serverを起動
2. main.py,main2.pyを起動し、GUI画面のstartボタンを押す
   ![image](https://github.com/user-attachments/assets/9735e202-5669-4bed-a1e4-b5f9436aaa2f)
3. 接続が確立されると、対戦画面に遷移するのでプレイ
   ![image](https://github.com/user-attachments/assets/58193462-78f8-4a80-9d00-e315fdf6fae5)
4. 
