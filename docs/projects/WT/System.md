## 动画系统

- 模型、动画、皮肤、装备等 
- movement
	- 移动
	- 翻滚
	- 攻击、连击
	- 防御
	- Iaido（拔刀攻击）
	- Roll
- 碰撞时添加声音和粒子特效
- 命中反馈
- 攻击方向使用蒙太奇播放不同部分
- 目标锁定功能
## 战斗系统

#### 职业定义

| 职业            | 特点                                                         | 主要职责                                                                       | 典型触发器                             |
| --------------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------ | -------------------------------------- |
| **Attacker**    | 近战攻击为主<br>高攻击力和高机动性<br>强大的近战武器和技能   | 冲锋陷阵，直接攻击敌人<br>通过近战技能快速解决战斗<br>承担高风险任务，击败敌人 | Kogetsu<br>Raygust<br>Scorpion         |
| **Gunner**      | 中距离和远距离攻击<br>高火力输出<br>多种攻击模式和弹药类型   | 提供持续火力压制<br>适应多种战斗环境<br>通过多样化的弹药类型进行攻击           | Asteroid<br>Hound<br>Viper             |
| **Sniper**      | 远距离精准射击<br>高单发伤害<br>远离战场核心进行攻击         | 远距离狙击敌人<br>提供侦察和情报支持<br>利用高精准度和高伤害的武器进行致命打击 | Egret<br>Ibis<br>Lightning             |
| **Shooter**     | 快速灵活的远程攻击<br>多样化的攻击手段<br>多种远程武器       | 提供远程火力支援<br>使用多种类型的弹药和武器<br>通过远程攻击压制敌人           | Asteroid<br>Hound<br>Meteor            |
| **All-Rounder** | 多种技能和武器<br>适应多种战斗情况<br>兼具近战和远程攻击能力 | 灵活切换角色职责<br>兼顾攻击、防御和支援<br>在不同战斗环境中发挥作用           | Kogetsu<br>Asteroid<br>Egret<br>Shield |

#### 属性系统

| 属性名称       | 说明                             |
| -------------- | -------------------------------- |
| HP             | 生命值，初始值为40。             |
| Attack         | 攻击力，在10以内随机生成。       |
| Trion          | Trion能量，在10以内随机生成。    |
| Defense        | 防御力，在10以内随机生成。       |
| Mobility       | 机动性，在10以内随机生成。       |
| Skill          | 技能水平，在10以内随机生成。     |
| Range          | 攻击范围，在10以内随机生成。     |
| Command        | 指挥能力，在10以内随机生成。     |
| SpecialTactics | 特殊战术能力，在10以内随机生成。 |

#### 技能系统

- 包括8个可配置触发槽（4主槽，4副槽）
- 角色内置特性：Bailout、雷达、Trion Body

触发机制设计：Trigger管理资源和实现技能效果，角色类调用抽象技能接口

## 背包系统

角色系统

	职业定义  
	
	 
	背包系统（Inventory）  
	物品获取、管理、使用等  
	装备（Equipment）  
	武器、防具、道具等  
	
	玩家属性和状态（Player）  
	状态、属性、数据等  



完善角色系统：
- 动画系统：继续完善和优化角色的动画，确保流畅和自然的过渡。可以考虑增加更多的动画细节，比如跑步、跳跃、翻滚等。
- 属性系统：细化角色属性，确保每个属性在游戏中都有明确的作用和反馈。Trigger机制：继续优化和扩展Trigger机制，确保每个Trigger都有独特的效果和玩法。
- 战斗系统：伤害反馈：进一步优化伤害反馈机制，增加受击动画和音效，提升战斗的打击感。
- 战斗逻辑：完善战斗逻辑，确保攻击、防御、闪避等行为的合理性和平衡性。
- 技能系统：开发更多的技能和特殊攻击，丰富战斗体验。
- 用户界面（UI）：HUD：开始设计和实现基本的HUD，包括血条、能量条、技能冷却时间等。
- 菜单系统：创建角色选择界面、技能升级界面等基本UI元素。

辅助系统（Development + Hotfix + Tests + Replays + Performance + Physics + Settings）

	开发工具（Development）  
	脚本、调试工具等  
	热修复（Hotfix）  
	快速修复和更新游戏内容  
	测试（Tests）  
	单元测试、集成测试  
	回放系统（Replays）  
	记录和重现玩家游戏过程  
	性能优化（Performance）  
	性能相关资源和配置  
	物理系统（Physics）  
	物理属性和行为  
	游戏设置（Settings）  
	图像、音频、控制等设置选项


竞技系统（GameModes + GameFeatures + System + Teams + Feedback）

	排位规则（System + Teams）  
	匹配系统  
	资格系统  
	战斗系统（GameFeatures）  
	战斗逻辑  
	伤害计算  
	反馈机制（Feedback）  
	震动、屏幕闪烁、UI提示等  

任务系统（GameFeatures + System）

	训练任务（GameFeatures）  
	训练任务设计  
	训练任务管理  
	平行世界探险（GameFeatures）  
	探险任务设计  
	探险任务管理  
	排名管理（System + GameModes + Feedback）

排名组件（System）  

	积分、奖惩机制等  
	排名系统（System + GameModes）  
	管理和更新玩家排名  


利用[mixamo](https://www.mixamo.com/#/)
使用 Blender 处理FBX
使用 ocenaudio 处理音频



```cpp

// https://dev.epicgames.com/documentation/zh-cn/unreal-engine/gameplay-ability-system-for-unreal-engine
// PublicDependencyModuleNames.AddRange(new string[] { "GameplayAbilities", "GameplayTags", "GameplayTasks", "Core", "CoreUObject", "Engine", "InputCore", "HeadMountedDisplay" });
```

- UGameStatics::ApplyDamage 
- AActor::TakeDamage 
- 判断伤害类型 
- 计算实际伤害并判断是否有效 
- 触发相应的广播信号 
- 自己定义的处理函数


PlayerState：适合存储玩家的持久数据，例如等级、经验和排名等。
Character：适合存储角色在当前游戏会话中的状态和行为。
