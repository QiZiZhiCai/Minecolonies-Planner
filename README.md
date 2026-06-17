[中文](./README.md#minecraft-模拟殖民地规划器) [English(ONLY for this doc! The tool itself has NOT been supported English yet!)](./README.md#minecraft-minecolonies-planner)
# Minecraft 模拟殖民地规划器
- 一款用于规划Minecraft游戏中模拟殖民地模组的殖民地建筑布局的工具

## 主要功能：
1. 蓝图库 - 支持Excel导入和自定义蓝图添加
2. 可视化画布 - 拖拽布局、缩放/移动、坐标显示
3. 蓝图操作 - 选择/旋转/复制/删除、详细信息展示
4. 数据管理 - 数据导入/导出、撤销/重做
5. 自定义设置 - 背景色调整、网格线颜色调整、字体缩放、蓝图透明度调整
---
## 更新日志：
- v2.1.1 - 2026年6月17日（贡献者：杞梓之才）
```
2.1版本贡献者杞梓之才注：我直到编辑此文档时才看见原来早就有了框选模式和蓝图移动模式，遂在界面里添加了提示文字
顺便把html文件里的开头注释删了，因为没必要
```

- v2.1 - 2026年6月16日（贡献者：杞梓之才）
1. UI左侧（蓝图界面）：
```
用户自己准备xlsx文件，读取后列出全部可选项
（不识别首行；第1列为分类，第2列为蓝图名，第3列为X轴方向上的长度，第4列为Z轴方向上的长度）
（建筑水平方向上的出入口朝向与哪轴垂直就在哪轴的长度数值后无空格添加“出入口”三字，出入口朝向默认与Z轴垂直）

改动前：硬编码检测分类：若有与硬编码一致的分类则支持涂色但不能自定义颜色，硬编码的分类之外的则不支持涂色
改动后：取消硬编码，支持自定义涂色
```
2. UI中部（规划界面）：
```
吸附到网格
改动前：吸附到半格
改动后：吸附到整格

缩放
改动前：0.2～8
改动后：0.01～10
```
3. UI右侧（设置界面）：
```
滑动条
改动前：下限均不为0
改动后：下限均为0，上限与步差不变（并不能通过将字体缩放调整为0以实现关闭蓝图名称显示）

底图移动
改动前：点一次移一格，仅此而已
改动后：点一次移一格，按住shift再点一次移一区块，按住ctrl和shift再点一次移16区块，在箭头按钮下方配有提示文字

数据管理
改动前：依托剪切板
改动后：依托json文件
```
此外为README.md校正了排版格式并添加了英文翻译

- v2.0 - 2025年9月10日
1. 增加导入底图功能，注意底图最好是一个像素对应mc中一个方块，up使用xaero地图，其他地图模组请自行测试
2. 增加导出图片功能
3. 优化已选建筑显示描边效果为内描边
```
额外说明：导入的地图不会自动识别区块位置，需要先在游戏中摆好一个区块，再到工具中移动地图对齐区块网格。
2.1版本贡献者杞梓之才注：实测Journeymap可用，注意此模组导出地图时会将已探索的区域全部导出，尺寸与中心会受孤立区块影响，会在用户调整底图位置时给用户带来不必要的麻烦，用户可能需要酌情裁剪底图
```

- v1.1 - 2025年9月9日
1. 增加了框选模式（B）
2. 增加了G键移动当前选择蓝图的功能
3. 增加了蓝图的描边
4. 增加了区块显示
```
2.1版本贡献者杞梓之才注：啊？？？？原来是有框选模式和蓝图移动模式的啊！！！！早知道我就不用那么费劲了！！！！都怪你不在界面里写提示！！！！呜呜呜:(
```
---
# Minecraft Minecolonies Planner
- A tool for planning building layouts of a colony in mod Minecolonies from game Minecraft

## Main functions:
1. Blueprint library - Supported Excel importing and custom blueprint adding
2. Visual canvas - Layout drag, zoom/move, coords display
3. Blueprint action - Select/rotate/copy/delete, detailed info display
4. Data management - Data import/export, redo/undo
5. Customization - Background colour, grid border colour, font zoom, blueprint transparency
---
## Changelog：
- v2.1 - 2026 June 16th (Contributor: 杞梓之才)
1. UI left (Blueprint interface):
```
The user prepares a xlsx file himself for reading to list all the options
（Not reading the header row; the 1st column is for classes, the 2nd column is for blueprint names, the 3rd column is for the length along the X axis, the 4rth column is for the length along the Z axis)
(Add 3 characters "出入口" without a space after the value of the length along the axis - defaultly Z - whose direction is perpendicular to the orientation of the horizontal entrance of the building)

Before the change：Hard coding detects the classes: If there is a class consistent with one of the hard-coded ones, colouring is supported but not customized while not supported for the rest classes
After the change：Cancelled the hard coding and supported custom colouring
```
2. UI middle (Planning interface):
```
Snap2grid
BtC: Snap to half grid
AtC: Snap to whole grid

Zoom
BtC: 0.2～8
AtC: 0.01～10
```
3. UI right (Setting interface):
```
Slidebar
BtC: All the lower limits are NOT 0
AtC: All the limits are 0 while the higher limits and the step sizes remain (unable to turn the blueprint names off by set the font zoom to 0)

Background image movement
BtC: 1 click 1 block and that's it
AtC：1 click 1 block, 1 chunk when holding shift, or 16 chunks when holding both ctrl and shift, tooltip under the arrow buttons

Data management
BtC: Via clipboard
AtC: Via a json file
```
Meanwhile corrected the typesetting of README.md and added English translation for it

- v2.0 - 2025 Sept 10th
1. Added background image importing function, note that it is best to have each pixel of the background image correspond to a single block in mc; the uploader (the owner) uses Xaero's Map, as for the rest map mod, users should test them of their own accord
2. Added image exporting function
3. Optimized the selected buildings to display a stroke effect with inner strokes
```
Additional note：the imported map would NOT auto recognize the position of the chunks, requiring a chunk marked in-game firstly, until then switch back to this tool and move the map to aligh with the chunk grid
Note from the contributor of v2.1 杞梓之才QiZiZhiCai: Verified that Journeymap is available，note that when exporting the map, this mod would export all the explored area, so the size and the centre are affected by isolated chunks, thus bringing unnecessary trouble to users, therefore users may have to flexibly crop the background image
```

- v1.1 - 2025 Sept 9th
1. Added box selection mode (B)
2. Added the function of moving the currently selected blueprint by pressing the key G
3. Added the outline for the blueprints
4. Added chunk display
```
Note from the contributor of v2.1 杞梓之才QiZiZhiCai: Huh???? So there IS a box seletction mode and a blueprint movement mode!!!! Had I known, I would not have to do so stressfully!!!! Blame you for having not annotated them in the interface!!! boohoo:(
```
