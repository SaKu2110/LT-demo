# 未来大×企業エンジニア 春のLT大会で使うデモ
## 概要
Vagrantのプロビジョニング機能を使って簡単に  
Javaの実行環境を作ってみよう!
## 実行環境
- vagrant
- virtual box
## 実行手順
1. `Vagrantfile`があるディレクトリ内で`vagrant up`
2. `vagrant ssh`でログインする
3. `/home/vagrant/file`内に`Hello.java`が存在し、`java`と`javac`が使えることを確認する
4. `exit`でログアウトし、`vagrant halt`でシャットダウンまたは`vagrant destroy`でMVを破壊する

以上
