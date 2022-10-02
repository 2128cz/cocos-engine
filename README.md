<p align="center">
    <a href="https://www.cocos.com/">
        <img src="https://user-images.githubusercontent.com/1503156/112012067-d5cdf580-8b63-11eb-819a-1c32cf253b25.png"
             alt="Cocos Creator Logo">
    </a>
</p>
<p align="center">
    <a href="https://github.com/cocos/cocos-engine/stargazers">
        <img src="https://img.shields.io/github/stars/cocos/cocos-engine.svg?style=flat-square&colorB=4183c4"
             alt="stars">
    </a>
    <a href="https://github.com/cocos-creator/engine/network">
        <img src="https://img.shields.io/github/forks/cocos/cocos-engine.svg?style=flat-square&colorB=4183c4"
             alt="forks">
    </a>
    <a href="https://github.com/cocos-creator/engine/releases">
        <img src="https://img.shields.io/github/tag/cocos/cocos-engine.svg?label=version&style=flat-square&colorB=4183c4"
             alt="version">
    </a>
    <a href="./licenses/LICENSE">
        <img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square&colorB=4183c4"
             alt="license">
    </a>
    <a href="https://twitter.com/CocosEngine">
        <img src="https://img.shields.io/twitter/follow/CocosEngine.svg?logo=twitter&label=follow&style=flat-square&colorB=4183c4"
             alt="twitter">
    </a>
</p>

# Engine for Cocos Creator

**Cocos Creator是Cocos家族中的新一代游戏开发工具，它带来了一套完整的3D和2D功能，同时为游戏开发者提供了一个直观、低成本和协作友好的工作流程。** Cocos Engine是Cocos Creator编辑器的运行时框架。

![image](https://www.cocos.com/wp-content/uploads/2022/08/13f41f1c975e8255fdc06f59597b9546-7.png)

Cocos Creator继承了以前版本的许多优秀品质和很酷的功能，例如高性能的低级别c++实现，直观的编辑器，跨平台支持。它支持本地平台，网页平台和快速扩展的即时游戏平台，包括Windows, Mac, iOS, Android, HarmonyOS, web, Facebook即时游戏，微信迷你游戏和TikTok迷你游戏。

此外，Cocos Creator将引擎技术推到了一个全新的水平，实现了在各种平台上的高性能可扩展性、完全可扩展性和易于开发。

1. **现代图形**:GFX实现是设计来适应现代图形api，它使用Vulkan在Windows和Android，金属在Mac OS和iOS, WebGL在Web平台。
2. **高性能**:运行时引擎用一半c++一半TypeScript构建，底层基础设施、本机平台适配、渲染器和场景管理都用c++编写，以确保高运行时性能。我们继续尽可能多地将繁重的起重工作转移到本地。
3.**可定制的渲染管道**:渲染管道被设计成完全可定制的，它支持跨所有平台的内置前向和延迟渲染管道。开发人员可以按照相同的方法定制自己的渲染管道。
4. **可扩展表面着色**:材质系统是建立在Cocos效果格式使用GLSL 300，着色程序将自动转换为合适的运行时格式。表面着色器允许完全定制表面材料，同时确保通用照明模型。
5. **基于物理的渲染(physical Based Rendering, PBR)**:标准效果采用基于物理的渲染，配合基于物理的相机和基于物理指标的照明，开发人员可以轻松实现跨不同环境的逼真和无缝渲染结果。
6. **简单的TypeScript API**: TypeScript中提供了用户级API集，以及强大的VSCode编辑器，使用Cocos Creator进行开发是非常高效的。
除了所有这些亮点，Cocos Creator还提供内置动画系统，物理系统，粒子系统，地形编辑支持，复杂的UI系统，即时预览等。

![image](https://user-images.githubusercontent.com/1503156/111037166-f27c7600-845d-11eb-988f-4c2c8b5c7321.png)

这个开源存储库是Cocos Creator的运行时引擎，这个引擎自然集成在Cocos Creator中，被设计成只作为基本的运行时库，而不能独立使用。

## Development and Contribution Notice

Cocos Creator引擎是开源的，欢迎社区参与，对于使用Cocos Creator编辑器进行开源引擎开发，您应该在编辑器中分叉这个存储库并设置
[定制引擎](https://docs.cocos.com/creator/manual/en/advanced-topics/engine-customization.html)。

### Prerequisite

- Install [node.js v9.11.2 +](https://nodejs.org/)
- Install [gulp-cli v2.3.0 +](https://github.com/gulpjs/gulp/tree/master/docs/getting-started)

### Clone

将此存储库克隆到您的本地环境中。

### Install

在克隆的引擎文件夹中，运行如下命令建立开发环境:

```bash
# download & build engine dependencies
npm install
```

这就是设置引擎开发环境所需要做的一切。

### Build

- 如果运行在Cocos Creator内，引擎将在编辑器窗口打开后自动编译和构建。关于在Cocos Creator中修改引擎的更多说明，请参考[引擎定制工作流](https://docs.cocos.com/creator/manual/en/advanced-topics/engine-customization.html)。
- 在编辑器外，需要运行以下命令进行编译:

```bash
npm run build
```

如果您想开发本机应用程序，请参考[native readme](native/ readme .md)。

### Contribution

您可以通过多种方式为Cocos Creator开源引擎做出贡献，非常感谢:

1. 通过[创建问题](https://github.com/cocos/cocos-engine/issues/new/choose)报告bug或特性请求。
2. 参与[议题]的讨论(https://github.com/cocos/cocos-engine/issues/)。
3.如果你修复或改进了任何东西，实现了任何功能，就创建一个pull request。
4. 通过对[使用文档存储库](https://github.com/cocos/cocos-docs)的拉请求来改进文档。
5. 在我们的[论坛](https://discuss.cocos2d-x.org/c/creator)中帮助其他开发者。

### Contribution notice

如果你试图发出一个pull request，有一些要求必须满足，这样你的pull request才能被接受:

1. 遵循我们的[Cpp编码风格指南](./docs/CPP_CODING_STYLE.md)和[TypeScript编码风格参考](./docs/TS_CODING_STYLE.md)。

2. 尝试在你的编码环境中集成ESLint和[CPP自动修复工具](./docs/CPP_LINTER_AUTOFIX_GUIDE.md)。

3.在你的拉请求中链接相关的问题或讨论，并清楚地说明你的拉请求的目的。

4. 通过所有自动持续集成测试。

5. 请求文件所有者或引擎开发人员检查您的pull请求。

## Example Project

- [小心你的步伐3D](https://github.com/cocos/cocos-tutorial-mind-your-step):初学者一步一步的教程项目回购。
- [测试用例](https://github.com/cocos/cocos-test-projects):每个引擎模块的单元测试场景。
- [示例案例](https://github.com/cocos/cocos-example-projects):简单而富有表现力的演示场景，用于基线测试和特定主题的案例研究。
- [Awesome Cocos](https://github.com/cocos/awesome-cocos):你可以在这里找到其他有用的工具和展示案例。

## Links

- (官方网站)(https://www.cocos.com/)
- [下载](https://www.cocos.com/en/creator/download)
- (文档)(https://docs.cocos.com/creator/manual/en/)
- (API参考)(https://docs.cocos.com/creator/api/en/)
- [项目和路线图](https://github.com/orgs/cocos/projects?query=is%3Aopen&type=new)
- (论坛)(https://discuss.cocos2d-x.org/c/creator)
- Discord社区:在Discord的发现面板中搜索Cocos。
