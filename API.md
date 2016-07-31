## 型別 Types

#### 牌 Card

一副 UNO 牌總共有 54 種牌 (0-9/skip/draw/reverse 有四種顏色，加上黑色 wild/draw)，所以使用兩個字元來代表：第一個字元代表的是顏色，可以是大寫的 `RGBYK` 之一，分別代表紅綠藍黃黑五種；第二個字元則是 `0123456789ABCDEF` 之一，依序代表 0-9 的數字牌、skip、draw two、reverse、wild、wild draw four。

#### 牌堆 Deck

牌堆是一組有上下順序的牌

#### 牌組 Cards

牌組是一組沒有上下順序的牌

#### 玩家資訊 Player

玩家資訊僅供後端記錄使用

- id: 系統給予的唯一代號，字串型別，僅供辨識用
- name: 玩家的名稱，字串型別
- cards: 玩家手上的牌組，Cards 型別

#### 賽局資訊 Game

賽局代表的是一局遊戲

- deck: 本局剩下還能抽的牌，Deck 型別，後端專屬
- discard: 出過的牌，Cards 型別，後端專屬
- last: 最後出的牌，Card 型別
- players: 依序記錄每個玩家的代號，字串陣列型別
- player_cards: 每個玩家的時牌，數值陣列型別，索引值是玩家的代號
- direction: 方向，必為 1 或 -1，順時針為 1
- current: 準備出牌的玩家的陣列索引，整數
