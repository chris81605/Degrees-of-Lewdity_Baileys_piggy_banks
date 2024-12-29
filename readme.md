# 公告  
## 2024/12/29 `貝利小金庫`即將與`貝利瘋狂Pc爆金幣`模組合併，目前倆模組代碼皆在重構中，最新消息請查看DC[`DOL汉化交流`](https://discord.gg/NBk4EtrS)/`DOL模组相关`板塊(測試版已發佈）

# Degrees-of-Lewdity
- <img decoding="async" src="https://gitgud.io/uploads/-/system/user/avatar/9096/avatar.png" width="24" alt=""> <b>遊戲作者</b> $\color{purple} {Vrelnir}$
  - [Vrelnir 的blog][blog]
  - [英文遊戲維基][wiki-en]
  - [中文英文遊戲維基][wiki-cn]
  - [官方 Discord][discord]
  - [遊戲源碼倉庫][gitgud]

# 需求  
* 需要搭配[MODLOADER][JML]使用  
* 需搭配[Degrees of Lewdity 中文本地化][DOLCN]使用  

# 貝利的小金庫簡介  
**為Degrees-of-Lewdity 新增要素：**  
* 在貝利辦公室、家中（未實裝）新增 “貝利的小金庫”，PC可於特定時段去嘗試撬開它爆貝利金幣。

# 更新日誌  
## 0.4.1  
1.嘗試使用其他方式獲取當啟用貝利瘋狂爆Pc金幣模組時的上一次租金（使本mod與該mod代碼低耦合，可能無法正常使用）   

## 0.4
1.貝利小金庫內的錢將隨著懷疑值超過500而開始減少  (最多降至1/100)
2.當懷疑值超過1500時，半夜造訪貝利的小金庫可能當場被貝利逮住（後續事件待完成）  
3.懷疑值計算增加上下限修正（0~2000） 

## 0.3.2  
1.文字敘述修正  
2.移除無法敲開的金庫  

## 0.3.1
1.優化貝利存款初始化方式，改為隨機產生天數後(30>90)，每天再隨機增加(£500>1000)  
2.優化貝利存款每日增減計算方式  
3.優化金庫內的錢數值範圍，改為隨機貝利存款的50分之1~全部   

## 0.3.0  
1.新增 貝利的懷疑值要素
* (1)現在依然只是個數字，無具體作用  
* (2)為未來劇情做準備

* (3)**升級至0.3.0需執行一次重置(使用言靈)**  
	* `<<link [[重置貝利的撲滿|$passage]]>>
<<unset $Baileys_money>>
<<unset $Baileys_money_init_date>>
<<unset $Baileys_PC_rent_money>>
<<unset $PC_rent_money_take_back>>
<<unset $visited_today>>
<<unset $lockpicking_tody>>
<<unset $lockpicking_tody_stage >>
<<unset $Baileys_money_refresh>>
<<unset $unlock>>
<<unset $Tack_Baileys_money_init>>
<<unset $taken_Baileys_money >>
<</link>>`  
	* 可透過
[過作弊拓展][CE]
開言靈或是使用其他類似MOD   

## 0.2.1  
1.修復問題  
* (1)修復已經清空貝利小金庫後離開場景再進入後 
"**拿走金庫里的錢**" 選項依然存在導致可能讓貝利存款及玩家存款數值異常的問題  
* (2)不幸觸發問題可透過 **回檔** 或：  
	* 言靈：<<link [[修復|$passage]]>><<unset $money>><<set $money to `任意不小於值100`>><<unset $Baileys_money>><<\/link>>修復  
	* 需使用新版解除言靈限制的言靈系統
 	* `任意不小於值100` 請填入任意 **大於** `100`的數值 

## 0.2.0  
1.優化代碼結構，將計算與判斷代碼獨立至
"**Widgets Bailey's piggy_banks**"，方便後續調用  
* (1)為未來劇情做準備，將可能重複利用的計算做成Widgets  

## 0.1.2  
1.修復開新檔第0天去撬貝利小金庫導致貝利存款初始化為0的問題  
* (1)修復問題
* (2)初始化計算方式變更  

2.修復貝利存款為0導致可能發生的潛在問題  
* (1)修復問題  
* (2)調整條件判斷代碼(至少能給貝利留下￡10 XD)  

3.調整部分文字顯示  
* (1)掃空貝利金庫收穫描述，增加新的級距  

## 0.1.1  
1.修復無限刷詭術問題  

## 0.1.0
1.基礎爆金幣功能完成  
* (1)各項數值待優化  

# todo  
✔️在貝利辦公室新增 “貝利的小金庫”  
  在貝利家新增貝利的金庫  
✔️pc於特定時間(半夜)可進入辦公室嘗試撬開保險箱  
✔️新增貝利的存款機制，小金庫內可獲取的金幣數量基於貝利的存款。  
  當貝利存款金額低於特定金額，當週貝利保護費加倍。  
✔️保險箱上鎖難度隨機(簡單->非常困難 or 密碼鎖小遊戲？)  
✔️可取得金幣數量隨機(與貝利存款掛勾)  
  新增事件，撬金庫被貝利發現  
  群友的點子：   
			新增貝利的電腦可黑客入侵轉走被利銀行帳戶的錢  
            白天也可以去撬小金庫，但被發現的機率大增，當貝利愛情足夠高時可以當貝利的面前撬，然後貝利笑著看你撬金庫後狠狠的撅你。  
            撬孤兒院的貝利小金庫可能被貝利發現，被發現後會被貝利撅(增加貝利的愛情程度)  
            撬貝利家的小金庫可能被貝利發現，發現後會被貝利賣掉，愛情足夠高則被留下來當RBQ。(可選擇)  
            變成貝利的RBQ後，貝利每晚會嘗試將在外遊蕩的PC抓回家撅。  
            變成貝利的RBQ後，可以請貝利帶你去鎮上的任何地方。  

[blog]: https://vrelnir.blogspot.com/
[wiki-en]: https://degreesoflewdity.miraheze.org/wiki
[wiki-cn]: https://degreesoflewditycn.miraheze.org/wiki
[gitgud]: https://gitgud.io/Vrelnir/degrees-of-lewdity/-/tree/master/
[discord]: https://discord.gg/VznUtEh
[JML]:https://github.com/Lyoko-Jeremie/sugarcube-2-ModLoader  
[DOLCN]:https://github.com/Eltirosto/Degrees-of-Lewdity-Chinese-Localization  
[CE]:https://github.com/chris81605/Degrees-of-Lewdity_Cheat_Extended/releases/download/v1.6.1/cheat.extended.zip 
