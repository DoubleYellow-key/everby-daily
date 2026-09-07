# Daily 雨天咖啡馆

面向 Everby 内置角色 `daily` 的精简场景动作包。所有动作统一使用咖啡馆桌边坐姿、黑色针织外套、黑灰格纹裙、黑色乐福鞋、胡桃木圆桌、绿色软椅、灰色咖啡杯和深灰笔记本电脑。

## 首版动作

- `daily-cafe-idle-loop`：桌边待机，可作为常规状态的待机动画。
- `daily-cafe-work-loop`：持续敲代码，可作为工作状态的背景动作。
- `daily-cafe-coffee-sip`：端杯喝咖啡，适合鼓励或等待语义。
- `daily-cafe-click-glance`：抬眼并轻推眼镜，适合左键点击事件。
- `daily-cafe-break-loop`：合上电脑捧杯休息，适合休息状态。

## 构建与验证

```bash
pnpm motion:build -- artifacts/motions/daily-rainy-cafe/motion.json artifacts/motions/daily-rainy-cafe.soulmotion
pnpm motion:validate -- artifacts/motions/daily-rainy-cafe.soulmotion
```

导入后，在“动作 → 状态模式”中将桌边待机设为待机动画、咖啡馆工作设为工作状态动作、雨天休息设为休息状态动作；在“事件规则”中将抬眼回应绑定到点击事件。
