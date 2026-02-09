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

### 2. #write memory
- running-config を startup-config に保存
- copy running-config startup-config の代替コマンド


### 3. Router(config-if)#no shutdown
- router設定時、interface活性化のためのコマンド
- ip address設定後忘れずコマンドする、しないと通信不可


### 4. Router設定後の結果が確認したい時

```
Rl#show ip interface brief
Interface              IP-Address      OK? Method Status  Protocol
FastEthernet0/0        192.168.1.1     YES manual up      up
FastEthernet0/1        192.168.1.33    YES manual up      up
```
