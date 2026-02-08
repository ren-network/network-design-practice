## 利便機能

### 1-1. logging synchronous
- コンソール操作中にログ出力で入力行が乱れるのを防止
- 入力作業の可読性・操作性向上


### 1-2. no ip domain-lookup
- コマンド誤入力時の DNS 名前解決を無効化
- 不要な待機時間を防止

### 1-1 ～ 1-2 の設定例

```
Router>enable
Router#configure terminal
Router(config)#line console 0
Router(config-line)#logging synchronous 
Router(config-line)#exit
Router(config)#no ip domain-lookup
```

---

### 2. #write memory
- running-config を startup-config に保存
- copy running-config startup-config の代替コマンド
