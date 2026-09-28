# LMC Team

> 以性能为唯一最高优先级的 Minecraft Java 版工具链团队

## 🚀 项目

### [LMC Launcher](https://github.com/LMC-Team/lmc-launcher)

高性能 **Android Minecraft Java 版启动器**。参考 PojavLauncher 与 Boat 的设计思路并吸取各自优点，不考虑向后兼容包袱：

- **JVM 直载** —— OpenJDK 21 aarch64（Termux 补丁版）通过 `dlopen` 直接加载，无 proot
- **渲染主路径** —— 自编译 Mesa Zink + Turnip（骁龙开源 Vulkan 驱动），直连 ANativeWindow
- **CPU 调度** —— big.LITTLE 拓扑识别，游戏主线程绑大核、GC/JIT 绑小核
- **输入直读** —— AInputQueue 在 native 层直接处理，零 Java 参与
- **音频** —— OpenAL-Soft + AAudio MMAP 低延迟模式

## 📮 联系

- 问题反馈：请在对应项目的 [Issues](https://github.com/LMC-Team/lmc-launcher/issues) 提交
