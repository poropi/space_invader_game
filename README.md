# スペースインベーダーゲーム

## 概要
このゲームは、JavaScript と HTML5 Canvas を用いて実装したクラシックなスペースインベーダーゲームです。  
プレイヤーは左右に移動し、画面上部から侵攻してくる敵を撃墜して各 Wave をクリアします。  
通常の敵を全滅させると、ボスUFOが出現し、ボスの HP（10）をプレイヤーのミサイルで削り切ると次の Wave へ進みます。

以下で遊べます。  
https://poropi.github.io/space_invader_game/

## 特徴
- **クラシックなゲーム体験**  
  昔懐かしいスペースインベーダーの世界観を再現しています。

- **ウェーブシステム**  
  各 Wave ごとに通常敵の移動速度や攻撃頻度が上昇し、難易度が増していきます。

- **ボス戦**  
  通常敵全滅後にボスUFOが出現。  
  ボスは画面上部近くをランダムかつトリッキーに動き、プレイヤーが直下にいるとミサイル攻撃を行います。  
  ボスにミサイルが当たった際は、ヒット時に金属音（効果音）を、ボス破壊時には爆発音を鳴らし、スコアに 200 点加算されます。

- **効果音**  
  ・ミサイル発射、敵破壊、ボスへのヒット／破壊時に効果音が再生されます。

- **背景演出**  
  背景には下方向にスクロールする星空を表示し、Wave が進むごとにスクロール速度が上がります。

- **操作制限**  
  ・スペースキーを押しっぱなしでは攻撃せず、単一のキー押下でのみミサイル発射。  
  ・画面上にミサイルが最大 3 発まで存在する場合、新規ミサイルは発射されません。

## ゲームの仕様
- **プレイヤー操作**  
  - 左右の矢印キー：プレイヤーの移動  
  - スペースキー：ミサイル発射（最大 3 発まで画面上に存在）

- **通常の敵**  
  - 画面上部に縦 5 行 × 横 11 列、計 55 体配置  
    - 各行ごとに色分け：1 行目：赤、2～3 行目：黄色、4～5 行目：水色  
  - 敵は左右に移動し、画面端に到達すると下方向へ滑らかにドロップします。

- **ボス戦**  
  - 通常敵全滅後にボスUFOが出現  
  - ボスの HP は 10。プレイヤーのミサイルで 10 回ヒットすれば破壊され、Wave クリアとなる  
  - ボスは画面上部近くをランダムでトリッキーに移動し、プレイヤーがボスの直下にいるとミサイル攻撃を行う  
  - ボスにミサイルがヒットした場合、残り HP があると金属音（効果音）を鳴らし、破壊された場合は通常の爆発音を鳴らし、スコアに 200 点加算される

- **スコア**  
  - 通常敵：1 行目 50 点、2～3 行目 30 点、4～5 行目 10 点  
  - ボス破壊時：追加で 200 点

- **背景**  
  - 星空が下方向にスクロール。Wave が進むごとにスクロール速度が上昇

## 操作方法
- **タイトル画面**  
  - 起動時はタイトル画面が表示され、「インベーダーゲーム」と大きな文字が中央に表示されます。  
  - 「スペースキーを押してスタート」の案内があり、スペースキーを押すとゲームが開始されます。

- **ゲーム中**  
  - 左右の矢印キーでプレイヤーを移動  
  - スペースキーを押すとミサイルが発射されます（押しっぱなしは無効、画面上に最大 3 発まで発射可能）

- **ボス戦**  
  - 通常敵を全滅させるとボスが出現  
  - ボスの HP をプレイヤーのミサイルで 10 回攻撃して破壊すると、次の Wave に進みます。

- **ゲームオーバー**  
  - プレイヤーが敵ミサイルに当たるとゲームオーバーとなり、スコアと Wave 数が表示されます。  
  - スペースキーを押すとタイトル画面に戻ります。

## インストールと実行方法
1. GitHub からリポジトリをクローンします：
   ```bash
   git clone https://github.com/yourusername/space-invaders-game.git
   ```
2.	クローンしたディレクトリ内の index.html をブラウザで開くか、ライブサーバーで実行してください。
3.	ゲーム開始はブラウザ上でスペースキーを押してください。

## 開発環境
  - 使用言語: JavaScript, HTML, CSS
  - ライブラリ: なし（純粋な JavaScript と HTML5 Canvas を使用）
  - 対象ブラウザ: モダンブラウザ（Chrome, Firefox, Edge 等）

## 既知の問題
  - 効果音はブラウザの自動再生ポリシーにより、ユーザー操作後に再生される場合があります。
  - 高速な Wave でのゲームバランスは今後調整予定です。
  - キーの自動リピートにより、ミサイル発射に制限を設けていますが、環境によって挙動が異なる可能性があります。

## ライセンス

このプロジェクトは MIT ライセンスの下で公開されています。
