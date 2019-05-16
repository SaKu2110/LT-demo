# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "demoVM" do |o|
    o.vm.box = "centos/7" # VMイメージを設定
    o.vm.hostname = "hostname" #ホスト名の設定
    o.vm.network :private_network, ip: "192.168.100.10" # IPアドレスの設定
    o.vm.network :forwarded_port, id: "ssh", guest: 22, host: 2210 # ポートの設定

    # 拡張機能Guest Additionsが入っている場合に必要に応じてコメントアウトを外す
    # o.vbguest.auto_update = false
    # o.vbguest.no_remote = true

    # 手元にあるシェルスクリプトを実行する
    # o.vm.provision :shell, :path => "Path/to/file"

    # 手元のファイルを共有する
    o.vm.synced_folder "./file", "/home/vagrant/file"

    # 以下、インラインシェルを実行する
    # rootユーザーでコマンドを実行
    o.vm.provision "shell", inline: <<-SHELL
      yum update
      yum install -y java-1.8.0-openjdk-src-debug.x86_64
      yum install -y java-1.8.0-openjdk-devel
      yum install -y git
      yum install -y vim emasc
    SHELL

    # 以下ゲストユーザーでコマンドを実行
    # o.vm.provision "shell", privileged: false, inline: <<-SHELL
    # SHELL
  end
end
