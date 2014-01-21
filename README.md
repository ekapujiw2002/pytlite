pytlite
=======

Control Patlite Signal Tower from Python

パトライト社のネットワーク対応型警告灯"**PHN-3FBE1**"をPythonから操作するためのモジュールです．

"**PHN-3FBE1**"及び，"**PHN-3FB**"を操作することができます．

http://www.patlite.jp/product/phn_3fbe1.html

機能制限等
==========

* TCPのみの対応です，UDPは対応予定ですが現在は対応していません
* 設定変更を行うことはできません
* 接続時の点灯状態は取得できません

利用例
==========

```python
from pytlite import Patlite

p = Patlite("10.0.0.1",10000,"TCP")

# 赤色点灯
p.red = p.ON

# 緑色点滅
p.green = p.BLINK

# ブザー(短い連続音)
p.buzzer = p.OFF

p.close()
```
