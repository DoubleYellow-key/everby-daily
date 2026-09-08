# Daily 办公室工作

面向 Everby 内置角色 `daily` 的办公室西装场景动作包。所有动作统一使用炭黑色西装、哑光白色办公桌、深灰办公椅、银灰笔记本和深绿色文件盘。

## 动作

- `daily-office-idle-loop`：手持文件的低频待机循环。
- `daily-office-work-loop`：持续使用笔记本电脑。
- `daily-office-sign`：拿笔签字并确认文件。
- `daily-office-click-glance`：抬眼并轻推眼镜。
- `daily-office-tired-pause`：闭眼揉眉心短暂停顿。

## 构建与验证

```bash
pnpm motion:build -- artifacts/motions/daily-office-work/motion.json artifacts/motions/daily-office-work.soulmotion
pnpm motion:validate -- artifacts/motions/daily-office-work.soulmotion
```

导入后，可将办公待机设为状态待机动画、日常办公设为工作状态动作，并把抬眼回应绑定到点击事件。
