[🇯🇵J] 将棋関係の software を Scoop で簡単に用意できます。

[🇬🇧E] Easy to install shogi software with Scoop.

# 作業手順の概要 / Summary

| 以下の条件に当てはまれば / If your PC ...                    | 以下の見出しへ / Jump to ... |
| ------------------------------------------------------------ | ---------------------------- |
| [🇯🇵J] ご利用の PC  で Scoop を初めて使うなら<br />[🇬🇧E] If your PC doesn't have Scoop, | Step #1                      |
| [🇯🇵J] Scoop に「t_shogi」を登録していなければ<br />[🇬🇧E] If you haven't added the bucket "t_shogi" to your Scoop, | Step #2                      |
| [🇯🇵J] 「t_shogi」が登録済みなら<br />[🇬🇧E] If you already have added the bucket "t_shogi" to your Scoop, | Step #3                      |

# Step #1 : Scoop を入れる / Install Scoop

## Step #1.1 : Scoop web page

[🇯🇵J] [本家の Scoop の説明](https://scoop.sh/)を読んでおくと理解が早いです。(読まずに #1.2 へ進んでも構いません。)
[🇬🇧E] See [Scoop site](https://scoop.sh/). (optional)

## Step #1.2 : PowerShell 起動

[🇯🇵J] 画面左下の「スタート」→「Windows PowerShell」→「Windows PowerShell」を起動します。

[🇬🇧E] "Start"(left-bottom) -> "Windows PowerShell" -> "Windows PowerShell"

## Step #1.3 : 設定の変更 / Execution Policy

[🇯🇵J] PowerShell 上で以下の1行を入力します。

[🇬🇧E] Input the following line on PowerShell.

```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```

## Step #1.4 : Scoop 導入 / install Scoop

[🇯🇵J] PowerShell 上で以下の1行を入力します。

[🇬🇧E] Input the following line on PowerShell.

```powershell
iwr -useb get.scoop.sh | iex
```

## Step #1.5 : 基本的な道具の導入 / install basic tools

[🇯🇵J] PowerShell 上で以下の2行を入力します。

[🇬🇧E] Input the following 2 lines on PowerShell.

```powershell
scoop install 7zip git
scoop bucket add extras
```

# Step #2 : 「t_shogi」を入れる / add "t_shogi" bucket

[🇯🇵J] PowerShell 上で以下の1行を入力します。

[🇬🇧E] Input the following line on PowerShell.

```powershell
scoop bucket add t_shogi https://github.com/topstone/scoop-bucket-t_shogi
```

# Step #3 : 将棋関係の software を入れる / install shogi software 

何を入れたいですか?

## Step #3.A 単独で動く software / independent software

| 名称 / name                                      | 説明 / description                                           | PowerShell                       |
| ------------------------------------------------ | ------------------------------------------------------------ | -------------------------------- |
| [Kifu for Windows](http://kakinoki.o.oo7.jp/)    | [🇯🇵J] 棋譜管理<br />[🇬🇧E] kifu management tool                   | `scoop install kifu_for_windows` |
| [K-shogi](https://www.studiok-i.net/kshogi.html) | [🇯🇵J] 機械と対局でき、棋譜解析もできる ([ぴよ将棋](https://www.studiok-i.net/piyo_shogi/)と互換)<br />[🇬🇧E] Playing shogi, analyzing kifu ([PIYO-shogi](https://www.studiok-i.net/piyo_shogi/) compatible) | `scoop install k-shogi`          |

## Step #3.B 組み合わせて動く software / Shogi UI and Engines

[🇯🇵J] 表示担当の software と試行部分の software を入れた後、表示担当の software 上で設定をする必要があります。

[🇬🇧E] You should register your shogi engines to your shogi GUI after the installation of GUI and engines.

| 表示担当 / GUI                            | 思考担当 / engine                                            | PowerShell                            |
| ----------------------------------------- | ------------------------------------------------------------ | ------------------------------------- |
| [将棋所](http://shogidokoro.starfree.jp/) | [Apery](https://github.com/HiraokaTakuya/apery_rust)         | `scoop install shogidokoro apery`     |
| [ShogiGUI](http://shogigui.siganus.com/)  | [Apery](https://github.com/HiraokaTakuya/apery_rust)         | `scoop install shogigui apery`        |
| [将棋所](http://shogidokoro.starfree.jp/) | [技巧 (Gikou)](https://github.com/gikou-official/Gikou)      | `scoop install shogidokoro gikou`     |
| [ShogiGUI](http://shogigui.siganus.com/)  | [技巧 (Gikou)](https://github.com/gikou-official/Gikou)      | `scoop install shogigui gikou`        |
| [将棋所](http://shogidokoro.starfree.jp/) | [稲庭将棋 (Inaniwa shogi)](https://github.com/inaniwa3/inaniwa-shogi) | `scoop install shogidokoro inaniwa`   |
| [ShogiGUI](http://shogigui.siganus.com/)  | [稲庭将棋 (Inaniwa shogi)](https://github.com/inaniwa3/inaniwa-shogi) | `scoop install shogigui inaniwa`      |
| [将棋所](http://shogidokoro.starfree.jp/) | [水匠 (Suisho)](https://twitter.com/tayayan_ts)              | `scoop install shogidokoro suisho`    |
| [ShogiGUI](http://shogigui.siganus.com/)  | [水匠 (Suisho)](https://twitter.com/tayayan_ts)              | `scoop install shogigui suisho`       |
| [将棋所](http://shogidokoro.starfree.jp/) | [やねうら王 (Yaneuraou)](https://yaneuraou.yaneu.com/)       | `scoop install shogidokoro yaneuraou` |
| [ShogiGUI](http://shogigui.siganus.com/)  | [やねうら王 (Yaneuraou)](https://yaneuraou.yaneu.com/)       | `scoop install shogigui yaneuraou`    |

### Step #3.B.将棋所

[🇯🇵J] 将棋所に思考担当 software を登録するには、画面左下の「スタート」→「Scoop Apps」→「将棋所」→「対局(G)」→「エンジン管理」→「追加」で「Windows (C:)」→「ユーザー」→あなたの名前→「scoop」→「apps」→お好きな思考担当 software→「current」の中の適切な □□□□□□□□.exe を選び、「開く(O)」を押します。

[🇬🇧E] To add your favorite engine to 将棋所(shogidokoro), click "Start"(left-bottom) -> "Scoop Apps" -> "将棋所"(Shogidokoro) -> "対局(G)"(game) -> "エンジン管理"(manage engines) -> "追加"(add) -> "Windows (C:)" -> "users" -> your name -> "scoop" -> "apps" -> your favorite engine -> "current", then select □□□□□□□□.exe which fit to your PC.

### Step #3.B.ShogiGUI

[🇯🇵J] ShogiGUI に思考担当 software を登録するには、画面左下の「スタート」→「Scoop Apps」→「ShogiGUI」→「ツール(T)」→「エンジン設定(E)」→「追加」で「Windows (C:)」→「ユーザー」→あなたの名前→「scoop」→「apps」→お好きな思考担当 software→「current」の中の適切な □□□□□□□□.exe を選び、「開く(O)」を押します。

[🇬🇧E] To add your favorite engine to ShogiGUI, click "Start"(left-bottom) -> "Scoop Apps" -> "ShogiGUI" -> "ツール(T)"(tools) -> "エンジン設定(E)"(engines) -> "追加"(add) -> "Windows (C:)" -> "users" -> your name -> "scoop" -> "apps" -> your favorite engine -> "current", then select □□□□□□□□.exe which fit to your PC.
