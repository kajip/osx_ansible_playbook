# Mac開発環境構築用 Ansible Playbook

## 概要

Macに開発環境を構築するための Ansible Playbook

## ロール

1. homebrew
    - homebrew 及び homebrew cask を使って必要なパッケージをインストール

## 実行前の準備

1. [homebrew](https://brew.sh/index_ja.html) のインストール

    ```bash
    $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ```

2. ansible のインストール

    ```bash
    $ brew install ansible
    ```

3. cowsay のインストール（オプション）

    ```bash
    $ brew install cowsay
    ```

## 実行方法

ansible-playbook を実行する

    ```bash
    $ ansible-playbook -i hosts playbook.yml
    ```

## インストールするパッケージの設定

group_vars/all.yml ファイルで設定する

1. homebrew_packages

    - Homebrew でインストールするパッケージ。主にコマンドラインツール

2. homebrew_cask_packages

    - Homebrew Cask でインストールするパッケージ。主にGUIツール


## Tips

- Homebrew Cask でインストールされるのは、基本英語版になる
- InteliJ のパッケージを Homebrew Cask でインストールできるけど、Communication Edition っぽい
