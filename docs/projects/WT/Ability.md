- Move： Crouch/Walk/Run/Sprint
- Jump
- Look
- Aim

- Attack
- Guard
- Dodge

```json
[
    {
        "id": "ability_attack",
        "name": "Attack",
        "cooldown": 2,
        "effect": {
            "damage": 10,
            "status_effects": ["stun"]
        },
        "animation_montage": "montage_attack",
        "user_input": "input_attack",
        "level_requirement": 1
    },
    {
        "id": "ability_defend",
        "name": "Defend",
        "cooldown": 1,
        "effect": {
            "reduce_damage": 50
        },
        "animation_montage": "montage_defend",
        "user_input": "input_defend",
        "level_requirement": 1
    }
]
```

