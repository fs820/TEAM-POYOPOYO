# 作品③
チーム制作のゲーム作品 (Windows,C++,DirectX9) ※起動可能  
2年生の後期にC++で書いたチームでのゲーム作品(テーマがベルトスクロールでした)

### チーム規模と開発期間
5人チーム（うちプログラマー3名）  
開発期間：2ヶ月

## ゲームプレイ動画URL
[https://youtu.be/lXaOvWuPhWw]

## 💻 私の担当ソースコード

主にnavi(誘導)システムのコア部分の設計と実装を担当しました。該当する主なソースコードは以下の通りです。

* **[navi.h](navi.h) / [navi.cpp](navi.cpp)**
  * ナビゲーション全体を管理するクラスです。マウス座標などをもとにマーカーを出し、ナビゲーションの配置と管理を行います
  * mapなどを使用し、安全に動作するように作成しました
* **[naviobject.h](naviobject.h) / [naviobject.cpp](naviobject.cpp)**
  * 配置するナビゲーションの親クラスです
  * Bulletを使ったTrigger判定がありPlayerが触れたら派生クラス固有の実行関数を呼びます
  * Playerへのメッセージを出すのが仕事で実際の動作はPlayerが行います
* **[arrow.h](arrow.h) / [arrow.cpp](arrow.cpp)**
  * naviobjectの派生です
  * 方向を持ち、プレイヤーにその向きを向かせる命令を出します
* **[climb.h](climb.h) / [climb.cpp](climb.cpp)**
  * naviobjectの派生です
  * プレイヤーに近くの上ることができるブロックを上る命令を出します
* **[jump.h](jump.h) / [jump.cpp](jump.cpp)**
  * naviobjectの派生です
  * プレイヤーにジャンプをする命令を出します
* **[naviMarker.h](naviMarker.h) / [naviMarker.cpp](naviMarker.cpp)**
  * マウスカーソルなどナビゲーションを置く場所に表示するオブジェクトです
* **[naviUi.h](naviUi.h) / [naviUi.cpp](naviUi.cpp)**
  * 現在選択しているナビゲーションの種類などを2D画面上に表示するクラスです
 
* **[player.h](player.h) / [player.cpp](player.cpp)**
  * 一部を担当
  * naviの処理をPlayerに適応するCheckNavigation,PreparationClimb,Turnなどを中心に担当
  * Playerとnaviの当たり判定のバグなどの対応なども行いました。

## ゲームプレイ画像
![ゲームのプレイ画面①](archive/picture/screenshot_000.png)
![ゲームのプレイ画面②](archive/picture/screenshot_001.png)
![ゲームのプレイ画面③](archive/picture/screenshot_002.png)
![ゲームのプレイ画面④](archive/picture/screenshot_003.png)
![ゲームのプレイ画面⑤](archive/picture/screenshot_004.png)
![ゲームのプレイ画面⑥](archive/picture/screenshot_005.png)
![ゲームのプレイ画面⑦](archive/picture/screenshot_006.png)

[要件定義書・システム設計書（PDF）はこちら](archive/sheet/HUMAN_SYNC_archive.pdf)
