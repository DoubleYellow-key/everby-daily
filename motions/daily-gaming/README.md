# Daily 游戏陪伴

面向 Everby 内置角色 `daily` 的桌面游戏场景动作包。Daily 保持侧身坐姿，双腿并拢，在黑色电竞桌前使用键盘和鼠标；服装与设备以克制的黄色细节统一视觉。

## 动作

- `daily-gaming-play-loop`：稳定坐姿下持续操作键盘和鼠标，适合工作或思考状态。
- `daily-gaming-win`：赢下对局后克制地握拳庆祝，适合庆祝、开心和鼓励语义。
- `daily-gaming-lose`：失利后皱眉并扶眼镜，适合困惑或疲惫语义。

## 构建与验证

```bash
pnpm motion:build -- artifacts/git/everby-daily/motions/daily-gaming/motion.json artifacts/git/everby-daily/dist/daily-gaming.soulmotion
pnpm motion:validate -- artifacts/git/everby-daily/dist/daily-gaming.soulmotion
```

导入后，可将“专注打游戏”配置为专注状态动作，并把胜利、失利动作映射到相应事件。`0.3.1` 已移除造成循环点头的前倾帧。
