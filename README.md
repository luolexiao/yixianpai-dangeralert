# 危险牌预警（com.lejiu.dangeralert）

弈仙牌 MOD。按玩家累计「对手出过的牌」，命中危险牌表就在屏幕顶部预警（只报当前对战那个敌人）；
`F6` 开关大面板，面板里可以直接编辑危险牌表，支持命名预设、牌池筛选、牌名搜索。

## 安装

用 [弈仙牌 MOD 管理器](https://github.com/Airexplosion/yixianpai-mod-sdk) 的「浏览」页一键装，
或顶栏「安装」选 Release 里的 zip。

下载见 [Releases](https://github.com/luolexiao/yixianpai-dangeralert/releases)。

## 说明

- 数据源：`Proto.GameStatus.battlePlayerDatas[].lastRoundData.usedCards`，只读、不发包。
- 当前对手 = 自己那条记录的 `nextOpponent`（和游戏 `GameStatusExtension.GetNextOpponentPlayerData` 一致）。
- 默认危险牌表 10 张，可在面板里改，存在管理器数据目录。
- SDK：`>=1.0.0 <2.0.0`。