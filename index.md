
# 計算機実習のための環境整備

## 必要な環境

* 「[計算機実験ハンドブック](https://github.com/utphys-comp/handbook/releases)」に書いてあることが、自分のPC上で一通り試せるような環境を準備する
    * プログラミング (オフライン・リモート利用)
        * エディタ、コンパイラ(C, C++, Fortran, BLAS/LAPACK, MPI/OpenMP)
    * 計算結果のプロット (オフライン利用)
        * gnuplot (python/matplotlib, MATLAB でも可)
    * 文書(レポート、論文)の作成 (オフライン・クラウド利用)
        * LaTeX (TeX Live あるいは Overleaf)
    * ネットワークの利用 (ECCSなどの大学の計算機にリモートアクセスできる環境)
	  * ターミナル、SSH
    * インタプリタ環境 (オフライン・クラウド利用)
	  * MATLAB、Python
    * 他の講義や実験で必要な計算機環境の整備についても、できるだけサポート

## 推奨環境

自分で環境を用意できるのであれば、基本何を使ってもよい

しかし、個別の環境をサポートすることは不可能。問題が生じた時は、まず推奨環境で試した上で質問

サポートする側とされる側で同じ環境が揃っていることが重要

* ceenv (VirtualBox版) + Overleaf
    * Mac (Intel), Windowsで動作
    * 注: Apple Silicon (M1/M2)では現状動作しない
* ceenv (Docker版) + Overleaf
    * Mac (Intel/Apple Silicon)で動作
    * 原理的にはWindowsでも動作するはずだが、スクリプト未整理
* 上記のceenv以外にもWSL2 (Windowsの場合)やHomebrew (macOSの場合)などを使って、必要な環境を揃えることが可能である
    * Windows: [WSL2の導入](wsl2) [西村俊祐氏(物理学科2020年進学)による]
    * macOS: [Homebrewによる環境構築](homebrew)
* 上記に加えて、オンライン授業・実習を効果的に行うために、UTOL, Slackなどを活用する

## 準備

* UTokyo Account (東大限定)
    * これがないと UTAS にも UTOL にもアクセスできない
* ECCSクラウドメール (@g.ecc.u-tokyo.ac.jp) (東大限定)
* 「計算機実験」Slack (「計算機実験」限定)
    * 参加方法は UTOL で通知

* ceenv (Computer Experiment Environment) (VirtualBox版)
    * VirtualBox仮想環境。UNIX全般、C, C++, Fortran, Python, 並列化プログラミング環境がこれ一つで揃う
    * ダウンロードサイズは1.5GB程度
    * インストール方法 [https://github.com/cmsi/MateriAppsLive/wiki/ceenv](https://github.com/cmsi/MateriAppsLive/wiki/ceenv)
    * [MateriApps LIVE!](https://cmsi.github.io/MateriAppsLive/) (VirtualBox版)は ceenv に加えて、いろいろな物質科学シミュレーションも実行できる環境一式が揃っている (ただしサイズは少し大きい 〜2.6GB)
    * 注: Apple Silicon (M1/M2)では現状動作しない

* ceenv (Computer Experiment Environment) (Docker版)
    * Docker Image。UNIX全般、C, C++, Fortran, Python, 並列化プログラミング環境がこれ一つで揃う
    * インストール方法 [https://github.com/cmsi/MateriAppsLive/wiki/ceenv-docker](https://github.com/cmsi/MateriAppsLive/wiki/ceenv-docker)
    * Mac (Intel/Apple Silicon)で動作
    * 原理的にはWindowsでも動作するはずだが、スクリプト未整理

* (あるいはceenvの代わりに) WSL2 (Windowsの場合)やHomebrew (macOSの場合)などを利用
    * Windows: [WSL2の導入](wsl2) [西村俊祐氏(物理学科2020年進学)による]
    * macOS: [Homebrewによる環境構築](homebrew)
* LaTeX (計算機実験ハンドブック 第3章)
    * [LaTeX環境の整備](latex)

* Gnuplot (計算機実験ハンドブック 1.4節)
    * ceenv (gnuplotインストール済み)
    * Ubuntu (WSL2) (```sudo apt install gnuplot```でインストールできる)
    * Homebrew (macOS) (```brew install gnuplot```でインストールできる)
    * [単体でのインストール](gnuplot)

* SSHリモートアクセス (計算機実験ハンドブック 1.2節)
    * [ECCSへのリモートアクセス](ssh-to-eccs) (東大限定)
    * [知の物理学研究センターワークステーション(ai)へのSSHリモートアクセス](ssh-to-ai) (「計算機実験」限定)

* MATLAB あるいは Python など、インタープリタ言語の一つに慣れておくと便利
    * 電卓としての利用、図の描画、行列演算、数式処理、任意精度計算、など
    * [MATLABのインストールと利用方法](matlab)
    * Pythonは[ceenv](https://github.com/cmsi/MateriAppsLive/wiki/ceenv)、あるいは[Google Collaboratory](https://colab.research.google.com)を利用
