
```json
[
    {
        "id": "trigger_kogetsu",
        "name": "Kogetsu",
        "type": "melee",
        "damage": 15,
        "abilities": ["ability_kogetsu"],
        "level_requirement": 1,
        "durability": 100
    },
    {
        "id": "trigger_shield",
        "name": "Shield",
        "type": "defensive",
        "damage_reduction": 100,
        "abilities": ["ability_shield"],
        "level_requirement": 1,
        "durability": 100
    },
    {
        "id": "trigger_armor_basic",
        "name": "Basic Armor",
        "type": "armor",
        "defense": 10,
        "attributes": {
            "endurance": 2
        },
        "level_requirement": 1,
        "durability": 100
    }
]

```

[What Makes a Good Combat System?](https://www.youtube.com/watch?v=8X4fx-YncqA)
- Anticipation 可打断
- Contact 不可打断
- Recovery 可打断

我打算把montage播放，分为几个阶段，Tag
- Status_Attack_Anticipation
- Status_Attack_Contact
- Status_Attack_Recovery

1. 动画开始播放，进入Status_Attack_Anticipation
2. 动画通知阶段，进入Status_Attack_Contact
3. 通知结束阶段，进入Status_Attack_Recovery
4. 动画结束播放，清除Status


這些句子是描述武術或格鬥技巧的各種動作與策略，充滿動作的節奏感和技擊的精髓：

1. 抽帶雲抹提：可能是描述武器或手臂的快速運動，像是抽取、揮舞、提起等動作，類似柔和而連續的攻防轉換。
2. 點崩撩刺擊：點、崩、撩、刺都是快速而直接的攻擊動作，點指輕點、崩為強力反擊，撩為上撩，刺為直線突刺。
3. 絞截斬格劈：絞截是封鎖對手攻擊的動作，斬和劈則是切割和劈砍動作，格則是防守或阻擋。
4. 挑撥掛錯洗：這一系列動作可能強調的是擾亂對手的節奏，挑撥用來誘使對手露出破綻，掛錯與洗可能指防禦與攻擊之間的轉換。

這些動作名詞可應用於武術或遊戲設計中的連招系統，特別適合在格鬥或戰鬥系統中展示多樣化的攻防手段。你打算如何將這些動作融入你的遊戲系統中呢？
