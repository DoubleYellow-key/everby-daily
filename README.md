# Daily for Everby

Daily 是 Everby 的桌面宠物角色。本仓库同时提供可导入的角色本体、基础日常动作扩展和居家陪伴动作扩展。

![Daily 角色动作总览](previews/daily-contact-sheet.png)

## 直接安装

发布文件位于 `dist/`：

- `daily.zip`：Daily 角色本体。在 Everby 的“角色与人设”页面选择“导入角色”。
- `daily-routines.soulmotion`：欢呼、专注和舒展动作。在“动作 → 扩展包”中导入。
- `daily-home-companion.soulmotion`：居家服装与坐垫场景动作，在“动作 → 扩展包”中导入。

请先导入 `daily.zip`，再导入 `.soulmotion` 文件。两个动作包的 `targetPetId` 都是 `daily`。

## 居家动作包

居家动作包包含 8 个动作、64 帧：

- 抱枕待机
- 抱枕敲代码
- 工作间隙伸展
- 坐着喝水
- 坐着吃饭
- 抱枕休息
- 抱枕睡眠
- 坐姿挥手

所有动作使用统一的米白猫耳家居服、圆形坐垫和棕色抱枕。一次性事件动作结束后，由 Everby 恢复当前状态动作。

![Daily 居家动作总览](previews/daily-home-companion.png)

## 仓库结构

```text
dist/                         可直接导入的发布文件
pet/daily/                    Daily 角色本体源码
motions/daily-routines/       基础日常动作包源码
motions/daily-home-companion/ 居家陪伴动作包源码
previews/                     角色与动作预览图
```

角色图集采用 `8 × 9` 网格，每格 `192 × 208`。动作扩展遵循 `.soulmotion` format v1，画布尺寸为 `192 × 208`。

## 验证

在 Everby 项目根目录中可以运行：

```bash
node skills/everby-pet-install/scripts/validate-pet.mjs artifacts/git/everby-daily/pet/daily
pnpm motion:validate -- artifacts/git/everby-daily/dist/daily-routines.soulmotion
pnpm motion:validate -- artifacts/git/everby-daily/dist/daily-home-companion.soulmotion
```

## License

代码与仓库内容按 [MIT License](LICENSE) 提供。涉及人物形象、第三方素材或再发布用途时，请自行确认对应授权范围。
