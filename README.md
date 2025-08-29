# LightPlane AI - 飞机大战游戏

一个基于Pygame的飞机大战游戏，集成了**三重AI系统**、**双重AI系统**、强化学习功能、AI图片生成和处理功能。

## 🚀 最新功能

### ✨ 三重AI系统集成 🆕
- **AI主控制器**: 统一管理所有AI子系统
- **AI学习优化器**: 动态优化AI策略和参数
- **AI场景生成器**: 智能生成游戏场景和关卡
- **AI策略生成器**: 自适应游戏策略调整
- **AI规则生成器**: 动态游戏规则优化

### ✨ 双重AI系统 🆕
- **战机AI控制器**: 专门控制战机移动和攻击
- **决策AI控制器**: 负责战略决策和战术规划
- **智能策略应用**: 攻击性、防御性、速度动态调整
- **实时性能监控**: 帧数、动作稳定性、移动状态监控

### ✨ AI图片生成与处理
- **AI图片生成**: 使用Stable Diffusion生成高质量飞机和背景图片
- **智能背景去除**: 支持RemBG、SAM、OpenCV等多种AI模型
- **边框去除与裁剪**: 自动检测主体边界，智能裁剪边框
- **批量图片处理**: 支持队列处理，实时进度显示

### 🎨 自定义配置系统
- **自定义配置页面**: 支持AI生成和上传自定义图片
- **智能图片优化**: 自动调整图片尺寸和格式
- **多图片类型支持**: 玩家飞机、敌机、背景图片
- **实时预览**: 即时查看处理结果

### 🎮 智能背景控制
- **AI生成背景**: 静态背景，不移动
- **上传背景**: 保持传统移动效果
- **默认背景**: 经典滚动效果

## 项目结构

```
LightPlane_AI/
├── README.md                      # 项目说明文档
├── launcher.py                    # 游戏启动器（主入口）
├── ai_master_controller.py        # AI主控制器 🆕
├── ai_learning_optimizer.py       # AI学习优化器 🆕
├── ai_scene_generator.py          # AI场景生成器 🆕
├── ai_strategy_generator.py       # AI策略生成器 🆕
├── ai_rule_generator.py           # AI规则生成器 🆕
├── custom_config_page.py          # 自定义配置页面
├── ai_game_page.py               # AI模式游戏页面
├── dual_game_page.py             # 双人模式游戏页面
├── traditional_game_page.py      # 传统模式游戏页面
├── custom_game_page.py           # 自定义模式游戏页面
├── easter_egg_page.py            # 彩蛋模式游戏页面
├── plane_sprites.py              # 游戏精灵类定义
├── game_function.py              # 游戏功能函数
├── Tools.py                      # 工具类
├── ai_image_processor.py         # AI图片处理器
├── background_remover.py         # AI背景去除器
├── local_image_generator.py      # 本地AI图片生成器
├── rl_game_ai.py                # 强化学习游戏AI 🆕
├── ml_game_ai.py                # 机器学习游戏AI 🆕
├── intelligent_decision_system.py # 智能决策系统 🆕
├── ai_controllers/               # AI控制器包
│   ├── __init__.py              # AI包初始化文件
│   ├── README.md                # AI包说明文档
│   ├── trained_ai_controller.py # 训练好的AI控制器
│   ├── integrated_ai_controller.py # 集成AI控制器 🆕
│   ├── realistic_ai_controller.py # 真实环境AI控制器 🆕
│   ├── advanced_ai_controller.py # 高级AI控制器 🆕
│   ├── ai_decision_controller.py # AI决策控制器 🆕
│   ├── game_strategy_controller.py # 游戏策略控制器 🆕
│   ├── plane_fighter_env.py     # Gymnasium环境定义
│   ├── integrated_plane_env.py  # 集成战机环境 🆕
│   ├── game_strategy_env.py     # 游戏策略环境 🆕
│   ├── ai_game_env.py           # AI游戏环境 🆕
│   ├── train_ai.py              # AI训练脚本
│   ├── train_integrated_plane.py # 集成战机训练 🆕
│   ├── train_game_strategy.py   # 游戏策略训练 🆕
│   ├── train_ai_decision.py     # AI决策训练 🆕
│   ├── check_training.py        # 训练状态检查脚本
│   ├── AI训练文档.md            # AI训练详细文档
│   ├── 训练命令速查表.md        # 训练命令快速参考
│   ├── AI决策系统训练指南.md    # AI决策训练指南 🆕
│   ├── AI决策系统集成完成报告.md # 集成完成报告 🆕
│   ├── 三重AI系统集成完成报告.md # 三重系统报告 🆕
│   └── 双重AI系统集成完成报告.md # 双重系统报告 🆕
├── models/                       # 训练好的AI模型
│   ├── best_model.zip           # 最佳模型
│   ├── integrated_plane_ppo/    # 集成战机PPO模型 🆕
│   ├── realistic_plane_ppo/     # 真实环境PPO模型 🆕
│   ├── game_strategy_ppo/       # 游戏策略PPO模型 🆕
│   ├── ai_decision_ppo/         # AI决策PPO模型 🆕
│   └── ppo_plane_fighter_*.zip  # 多个训练步数模型
├── logs/                         # 训练日志
├── images/                       # 游戏图片资源
├── music/                        # 游戏音乐资源
├── processed_images/             # AI处理后的图片
├── lora_output/                  # LoRA训练输出
└── airplane_dataset/             # 飞机图片数据集
```

## 游戏模式

### 1. 传统模式 (Traditional Mode)
- 单人游戏，只有玩家1
- 无僚机，玩家位置在左侧居中
- 使用默认游戏资源

### 2. 双人模式 (Dual Player Mode)
- 双人游戏，玩家1和玩家2
- 无僚机，玩家1在左上，玩家2在左下
- 支持键盘和鼠标控制

### 3. AI模式 (AI Mode) 🆕
- **双重AI系统**: 战机AI + 决策AI
- **三重AI系统**: 主控制器 + 学习优化器 + 场景生成器
- **预训练模型**: 使用数百万步训练的PPO模型
- **智能策略**: 攻击性、防御性、速度动态调整
- **实时监控**: 帧数、动作稳定性、移动状态监控

### 4. 自定义模式 (Custom Mode)
- 支持AI生成和上传自定义图片
- 智能背景去除和边框裁剪
- 自定义玩家飞机、敌机、背景
- 实时预览和配置管理

### 5. 彩蛋模式 (Easter Egg Mode)
- 特殊游戏模式和有趣玩法

## 🎯 快速开始

### 运行游戏
```bash
python3 launcher.py
```

### 使用AI模式
1. 启动游戏，选择"AI模式"
2. 系统自动加载预训练模型
3. 双重AI系统开始运行
4. 观察AI策略应用和性能监控

### 使用自定义配置
1. 启动游戏，选择"自定义模式"
2. 使用AI生成图片或上传自定义图片
3. 自动背景去除和边框裁剪
4. 开始游戏，享受个性化体验

### 训练AI模型
```bash
cd ai_controllers
python3 train_ai.py --mode train --timesteps 2000000
python3 train_integrated_plane.py --timesteps 1000000
python3 train_game_strategy.py --timesteps 500000
python3 train_ai_decision.py --timesteps 300000
```

### 检查训练状态
```bash
cd ai_controllers
python3 check_training.py
```

## 🎮 控制说明

### 玩家1控制
- **鼠标移动**: 控制飞机位置
- **空格键**: 发射子弹
- **ESC键**: 返回主菜单

### 玩家2控制（双人模式）
- **WASD键**: 控制飞机移动
- **空格键**: 发射子弹

### 游戏控制
- **开始按钮**: 开始/暂停游戏
- **暂停按钮**: 暂停/继续游戏

### 自定义配置页面
- **上传按钮**: 选择本地图片文件
- **AI生成按钮**: 使用AI生成图片
- **去边框按钮**: 去除图片边框
- **自动处理按钮**: 背景去除+边框裁剪

## 🤖 AI特性

### 三重AI系统 🆕
- **AI主控制器**: 统一管理所有AI子系统
- **AI学习优化器**: 动态优化AI策略和参数
- **AI场景生成器**: 智能生成游戏场景和关卡
- **AI策略生成器**: 自适应游戏策略调整
- **AI规则生成器**: 动态游戏规则优化

### 双重AI系统 🆕
- **战机AI控制器**: 专门控制战机移动和攻击
- **决策AI控制器**: 负责战略决策和战术规划
- **智能策略应用**: 攻击性、防御性、速度动态调整
- **实时性能监控**: 帧数、动作稳定性、移动状态监控

### 游戏AI
- **混合AI控制器**: 结合训练模型和规则AI
- **智能行为**: 自动躲避、追击、巡逻
- **平滑移动**: 优化的移动算法，减少抖动
- **自适应射击**: 根据敌人位置自动射击
- **预训练模型**: 使用数百万步训练的PPO模型

### 图片AI
- **Stable Diffusion**: 高质量AI图片生成
- **智能背景去除**: 多种AI模型支持
- **轮廓检测**: OpenCV智能边界识别
- **自适应裁剪**: 智能padding和尺寸调整

## 🛠️ 技术栈

- **游戏引擎**: Pygame
- **AI框架**: Stable Baselines3
- **强化学习**: Gymnasium
- **深度学习**: PyTorch
- **图片处理**: OpenCV, PIL, RemBG
- **AI生成**: Stable Diffusion
- **编程语言**: Python 3.7+

## 📋 系统要求

- Python 3.7+
- 操作系统: Windows/macOS/Linux
- 内存: 8GB+ (推荐16GB用于AI图片生成)
- 存储: 5GB+ (包含AI模型和图片资源)
- GPU: 推荐NVIDIA GPU用于AI图片生成

## 🔧 安装依赖

### 基础依赖
```bash
pip install pygame numpy pillow
```

### AI图片处理依赖
```bash
pip install opencv-python rembg torch torchvision
pip install diffusers transformers accelerate
```

### 强化学习依赖
```bash
pip install stable-baselines3 gymnasium
```

## 📚 使用指南

### AI模式使用
1. 选择"AI模式"进入游戏
2. 系统自动加载预训练模型
3. 观察双重AI系统的运行状态
4. 查看AI策略应用和性能监控

### AI图片生成
1. 在自定义配置页面输入描述
2. 选择图片类型（玩家飞机/敌机/背景）
3. 点击"AI生成"按钮
4. 等待生成完成，自动背景去除

### 自定义图片上传
1. 准备PNG/JPG格式图片
2. 在自定义配置页面上传
3. 自动调整尺寸和格式
4. 可选择背景去除和边框裁剪

### 智能背景控制
- **AI生成背景**: 自动设置为静态，不移动
- **上传背景**: 保持传统滚动效果
- **默认背景**: 经典移动效果

## 🐛 故障排除

### 常见问题
1. **AI图片生成失败**: 检查GPU内存和模型文件
2. **背景去除效果差**: 尝试不同的AI模型
3. **游戏卡顿**: 降低图片分辨率或使用默认资源
4. **AI模型加载失败**: 检查模型文件路径和依赖

### 性能优化
1. 使用较小的图片尺寸
2. 启用GPU加速（如果可用）
3. 关闭不必要的AI功能
4. 使用预训练模型减少计算开销

## 🔄 更新日志

### v3.0.0 (当前版本) 🆕
- ✨ 新增三重AI系统集成
- ✨ 新增双重AI系统
- ✨ 新增AI主控制器
- ✨ 新增AI学习优化器
- ✨ 新增AI场景生成器
- ✨ 新增AI策略生成器
- ✨ 新增AI规则生成器
- ✨ 新增多个预训练模型
- ✨ 新增实时性能监控
- ✨ 优化AI策略应用

### v2.0.0
- ✨ 新增AI图片生成功能
- ✨ 新增智能背景去除
- ✨ 新增边框去除和裁剪
- ✨ 新增自定义配置页面
- ✨ 新增智能背景移动控制
- ✨ 优化AI控制器性能
- ✨ 支持批量图片处理

### v1.0.0
- 🎮 基础飞机大战游戏
- 🤖 强化学习AI控制器
- 🎯 多种游戏模式

## 👥 开发团队

- **项目名称**: LightPlane AI
- **版本**: 3.0.0
- **最后更新**: 2024年12月
- **主要功能**: 飞机大战 + 三重AI系统 + 双重AI系统 + AI图片生成 + 智能处理

## 📄 许可证

本项目仅供学习和研究使用。

## 🤝 贡献

欢迎提交Issue和Pull Request来改进项目！

---

**享受AI驱动的个性化飞机大战游戏！** 🚀✈️🤖
