# PPT 逐页审阅

`ppt-page-review` 是一个 Codex 插件。它把汇报材料逐页做成可编辑的 PowerPoint，方便你在制作前确认内容和视觉效果。

1. **确认提纲**。核对页面结论、完整文字、阅读顺序和主画面。
2. **确认效果图**。用图像生成能力预览版式、配色和信息层级。
3. **交付可编辑 PPTX**。将文字、常规图形和表格尽量重建为 PowerPoint 原生对象。

修改事实、数据或措辞时，流程回到提纲确认。仅调整已确认内容的版式时，从对应的视觉阶段继续。

## 安装

在 Codex CLI 中添加此仓库的插件目录来源。

```sh
codex plugin marketplace add koliban/ppt-page-review
```

在支持本地插件的 ChatGPT 桌面应用中打开插件目录，切换到 **PPT 逐页审阅**，安装 `ppt-page-review`，然后在新聊天中调用它。也可以克隆仓库，在 Codex 中打开仓库根目录，并在重启桌面应用后从仓库的插件目录安装。安装方式见 [Codex 插件文档](https://developers.openai.com/plugins/build/plugins)。

插件需要支持本地执行的 Codex 环境和图像生成能力。可编辑 PPTX 路线的 Python 依赖见 [PPT Master requirements.txt](plugins/ppt-page-review/skills/ppt-master/requirements.txt)。

## 使用示例

> 用 ppt-page-review 把这份方案逐页做成汇报 PPT。先给我第一页提纲，我确认后再生成效果图。

开始新演示文稿时，你可以提供已有 PPTX 或版式参考，也可以说：

> 先根据我的品牌规范和参考页创建一套可复用模板，然后用它制作这套汇报 PPT。

创建的模板保存在当前项目或你指定的目录。仓库包含模板创建流程、规范和开发脚手架，可供你从自己的素材开始。

## 许可

插件自有工作流和发布配置采用 [MIT 许可证](LICENSE)。所附 [PPT Master](https://github.com/hugohe3/ppt-master) 使用 [原 MIT 许可证](plugins/ppt-page-review/skills/ppt-master/LICENSE)，所附 ImageGen 技能使用 [Apache 2.0 许可证](plugins/ppt-page-review/skills/imagegen/LICENSE.txt)。图标、音效等素材的许可见各自目录中的声明。

随附的 PPT Master 版本使用空的预设目录，并支持空图表库，便于从自有素材开始。
