# 第三方源码与发行资料

QuietTune 的完整应用源码随每个 Release 的版本标签提供。Windows 安装器中的官方组件保持未修改，各自许可文件随安装器保存；Release 另附上游源码及许可资料压缩包。

| 组件 | 本版本使用的版本或提交 | 官方源码与构建资料 |
| --- | --- | --- |
| QuietTune | 1.1.3 | [v1.1.3 源码](https://github.com/JadeCake5/quiettune/tree/v1.1.3)，构建入口为 `package.json`、`desktop/prepare-runtime.ps1`，Python/npm 依赖均有锁文件。 |
| Essentia.js | 0.1.3，`f46c91c08bdf263d5f3d575ab8fb0f9b81695acf` | [官方源码](https://github.com/MTG/essentia.js/tree/f46c91c08bdf263d5f3d575ab8fb0f9b81695acf)，包含 `Dockerfile`、`Makefile.essentiajs`、`build-libs.sh` 和 C++/JavaScript 绑定。该提交与 npm 0.1.3 的 gitHead 一致。 |
| Essentia | Essentia.js 官方 WASM 内的算法 | [官方核心源码](https://github.com/MTG/essentia)，官方 0.1.3 的 Dockerfile 描述核心及 Eigen 的构建方式；其上游构建未将核心 Git 提交固定在脚本中，本项目没有自行重编该 WASM。 |
| FFmpeg/FFprobe | Gyan 9.0.1 full build，`bf1b838f2ab88b4f8fd83443325c782ea0e0f7fa` | [对应 FFmpeg 源码](https://github.com/FFmpeg/FFmpeg/tree/bf1b838f2ab88b4f8fd83443325c782ea0e0f7fa)。附带 Gyan 原始 README、完整组件版本列表、GPL 原文和实际 `-buildconf` 输出。静态链接的外部库分别保留各自许可与源码义务。 |
| Node.js | 22.18.0 | [官方源码](https://github.com/nodejs/node/tree/v22.18.0)，完整原始 LICENSE 随私有运行环境提供。 |
| Python | 3.11.6 | [官方源码发行](https://www.python.org/downloads/release/python-3116/)，嵌入式解释器保留 PSF 原始许可。 |
| Electron | 44.7.0 | [官方源码](https://github.com/electron/electron/tree/v44.7.0)，Electron 原始许可及 Chromium 第三方声明随应用分发。 |
| Python 与前端依赖 | 以仓库锁文件为准 | `backend/requirements-windows.lock`、各目录 `package-lock.json`；运行环境保留包的 dist-info 和原始许可文件，前端许可收集在 `runtime/licenses/frontend/`。 |
| 官方模型 | MSD MusiCNN、激烈与放松分类器 | 原始模型元数据保留作者、框架、类别和来源；模型共同许可见 [Essentia-models-LICENSE.txt](desktop/Essentia-models-LICENSE.txt) 与 [LICENSE-NOTICES.md](LICENSE-NOTICES.md)。 |

上游源码资料附件包含所列 Essentia.js、FFmpeg 的官方源代码归档、构建资料和许可文件，附件中的 SHA-256 索引用于校验下载完整性。静态第三方库及官方 WASM 的上游构建信息应与其原作者提供的资料一起查阅；该附件不宣称验证了上游二进制的可重现构建。

再次分发或修改安装器时，应完整保留版权、许可和所需对应源码及构建资料。第三方源码链接、许可声明和应用自身开源均不取消对应组件的原许可要求。
