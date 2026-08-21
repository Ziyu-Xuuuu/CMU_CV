# CMU LeCAR Lab 成员、研究方向与 MSR 套磁分析

> 调研快照：2026-07-15  
> 目标读者：新入学 CMU MSR、希望联系 Guanya Shi（石冠亚）并寻找具体合作切入点的学生

## 1. PI：Guanya Shi

### Guanya Shi（石冠亚）— Assistant Professor, CMU RI/SCS

[个人主页](https://www.gshi.me/)｜[Google Scholar](https://scholar.google.com/citations?hl=en&oi=ao&user=joR1Z4UAAAAJ)｜[LeCAR Lab](https://lecar-lab.github.io/)

Guanya 对自己的研究定义非常清楚：研究位于 **AI、robotics 和 control 的交叉点**，从算法基础一直延伸到 humanoid 等真实通用机器人系统，目标是 reliable、adaptive、efficient 的 learning and control。

他的研究轨迹大致经历了三个阶段：

- **Learning-augmented control 与理论保证**：Neural Lander、Neural-Swarm、Neural-Fly、meta-adaptive nonlinear control、MPC regret analysis；
- **Agile mobility 与 sim-to-real**：高动态无人机、四足和车辆的在线适应、安全运动与 learned dynamics；
- **Generalist humanoid / manipulation**：OmniH2O、ASAP、BFM-Zero、SPIDER、PLD、ENPIRE、CaP-X，以及更系统化的真实机器人数据与 post-training 基础设施。

因此，联系 Guanya 时不应把他描述成“只做人形机器人”或“只做强化学习”。更准确的概括是：

> 用学习扩大控制系统的适应性和通用性，同时保留物理结构、闭环性能与真实部署能力。

对你的直接启示是：第一封邮件应同时出现 **具体机器人平台、闭环问题、学习方法和验证方式**，而不是只说想做 embodied AI 或 foundation model。

## 2. 当前 PhD 成员
### 2.1 Eliot Xing 
[个人主页](https://etaoxing.com/)｜[Google Scholar](https://scholar.google.com/citations?sortby=pubdate&user=wzmAVGsAAAAJ&view_op=list_works)
- 方向： 仿真/真实接口一致性、可微物理、real-time robot I/O、跨平台 policy evaluation。
- 匹配度：0.5
### 2.2 Chaoyi Pan
[个人主页](https://panchaoyi.com/)｜[Google Scholar](https://scholar.google.com/citations?hl=en&oi=ao&user=lJNKzEMAAAAJ)
- 方向：**Physics-based robot data generation** 与 **generative models in control**，MPC
- 匹配度：0.7
### 2.3 Zeji Yi
[个人主页](https://iscoyizj.github.io/)｜[Google Scholar](https://scholar.google.com/citations?hl=en&user=l8xh-QQAAAAJ)
- 方向：研究 learning-based control、optimization
- 匹配度：0.5
### 2.4 Jin Cheng
[个人主页](https://jin-cheng.me/)｜[DBLP/论文记录](https://dblp.org/pid/230/9055-2)
- 方向：RL, whole-body control、inverse-dynamics MPC、motion retargeting、safe/adaptive torque policies、unsupervised skill discovery；
- 匹配度：0.6
### 2.7 Wenli Xiao 
[个人主页](https://wenlixiao.com/)｜[Google Scholar](https://scholar.google.com/citations?hl=en&user=WGbVYzsAAAAJ)
- 方向：dexterous manipulation 与 humanoid robots， **foundation model post-training + physical autoresearch + real-robot feedback loop**。
- 匹配度：1
### 2.8 Cunxi (Jimmy) Dai
[个人主页](https://cunxid.github.io/)｜[Google Scholar](https://scholar.google.com/citations?hl=en&oi=ao&user=nJkhpJ0AAAAJ)
- 方向：contact-implicit MPC、foundation model（不主要）
- 匹配度：0.7

## 3. 当前硕士生
### 3.1 Chaitanya Chawla 
- 方向：从人类数据学习 dexterous manipulation
### 3.2 Tonghe Zhang
- 方向：scalable robot learning、flow-VLA post-training 与 agentic self-improvement
### 3.3 Lingxiao Guo 
- 方向：real-world RL、self-supervised learning 与 robot foundation-model data flywheel
### 3.4 Angchn Xie 
- 方向：uncertainty、knowledge transfer 与 few-shot adaptation
### 3.5 Yutong Wang
- 方向：aerial robot planning、control 与 aerial manipulation
### 3.6 Jia Xie 
- 方向：真实机器人硬件与 physical autoresearch 
## 5. 按研究簇理解“谁和谁在做什么”

| 研究簇 | 核心成员/高度相关成员 | 代表问题 |
|---|---|---|
| Humanoid foundation model / whole-body control | Guanya、Wenli、Tonghe、Cunxi、Jin | 一个 policy 如何覆盖多种目标、技能、奖励和全身动作？ |
| VLA post-training / physical self-improvement | Wenli、Tonghe、Jia、Lingxiao、Huanyu | 如何利用真实 rollout、failure 和 residual RL 持续提高 policy？ |
| Human data → robot skills | Chaoyi、Chaitanya、Wenli、Huanyu | 如何进行 retargeting、physics grounding，并把人类视频/交互转成可执行技能？ |
| Sampling MPC / optimization / theory | Zeji、Chaoyi、Jin、Anoushka | 生成式优化、sampling MPC 和 learned dynamics 的性能来源与保证是什么？ |
| Sim-to-real / adaptation / uncertainty | Angchen、Cunxi、Ishayu、Wenli、Jin | 动力学、terrain、payload、actuator 或 embodiment 变化时如何少样本适应？ |
| Differentiable physics / infrastructure | Eliot、Jia、Angchen、Giri | 如何让 simulation、I/O、data 和训练/评测系统支持跨平台扩展？ |
| Aerial / field autonomy | Yutong、Anoushka，以及 Guanya 的历史工作 | 如何把 learning-and-control 用于高速、接触或复杂环境中的飞行/车辆？ |