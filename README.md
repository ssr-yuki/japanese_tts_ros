# japanese_text_to_speech

日本語テキストを音声として出力する ROS node です．

[Open JTalk](http://open-jtalk.sourceforge.net/) を利用しています．

## インストール

Open JTalkとaplayコマンドに依存しています．

```
sudo apt install open-jtalk open-jtalk-mecab-naist-jdic hts-voice-nitech-jp-atr503-m001 alsa-utils
```

catkin workspace内に設置して `catkin_make` してください．

## 使い方

`japanese_text_to_speech` node を起動してください．
この node がサーバとなり，クライアントから受け取ったテキストを音声出力します．

```
rosrun japanese_text_to_speech japanese_text_to_speech
```

この node は [actionlib](http://wiki.ros.org/actionlib) を使って実装されています．
簡単なクライアントのサンプルとして `test_client` nodeを用意してあります．

```
rosrun japanese_text_to_speech test_client
```