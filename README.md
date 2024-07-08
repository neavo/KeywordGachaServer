## KeywordGacha Server
- 与 [KeywordGacha](https://github.com/neavo/KeywordGacha) 配套的本地大模型服务器端一键包
- 也可以作为 [SakuraLLM](https://github.com/SakuraLLM/SakuraLLM) 轻小说翻译模型的服务器端来使用

## 注意
- `翻译` 与 `提取关键词` 使用不同的模型和启动配置，不能混用
- `提取关键词` 应使用 [GLM4-9B-Chat-GGUF](https://huggingface.co/second-state/glm-4-9b-chat-GGUF) 模型
- `翻译` 应使用 [SakuraLLM](https://github.com/SakuraLLM/SakuraLLM) 模型
- 请仔细阅读本页的各项步骤

## 作为 KeywordGacha 服务器使用
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [Release下载页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的一键包，解压缩到本地；
- 下载模型 --> [GLM4-9B-Chat-GGUF](https://huggingface.co/second-state/glm-4-9b-chat-GGUF) ，放到到上面的文件夹里
- 现在你的文件结构应该类似于：
  
  ```
  KeywordGachaServer\llama\...
                    \common.bat
                    \00_RUN_NP2_3K.bat
                    \glm-4-9b-chat-Q4_K_S.gguf
                    \...
  ```

- 双击 00_3K_NP4.bat，会开启一个黑色的终端窗口
- 一阵文字滚动后，看到有类似 `all slots are idle | tid="xxx" timestamp=xxx` 的字样就说明成功启动了
- 关闭黑色的终端窗口即为关闭服务器

## 作为 SakuraLLM 服务器使用
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [Release下载页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的一键包，解压缩到本地；
- 根据你的显存大小下载对应的 SakuraLLM 模型并放入上面的文件夹
- 显存小于 11G --> [GalTransl-7B-v1.5](https://huggingface.co/SakuraLLM/GalTransl-7B-v1.5/blob/main/GalTransl-7B-v1.5-IQ4_XS.gguf)
- 显存大于等于 11G --> [Sakura-14B-Qwen2beta-v0.9.2-GGUF](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2beta-v0.9.2-GGUF/blob/main/sakura-14b-qwen2beta-v0.9.2-iq4xs.gguf)
- 双击 `显存大小对应的启动脚本`，选择对应的模型使用即可
- 一键包内启动脚本应参考这个教程 [SakuraLLM 性能优化指南](https://github.com/NEKOparapa/AiNiee/blob/main/SakuraLLMScript/OptimizationGuide.md) 与 [AiNiee](https://github.com/NEKOparapa/AiNiee) 翻译器搭配使用
- 不保证与其他应用翻译应用的兼容性

## 其他提醒　
- 每个人的系统环境不同，显存占用有波动是正常现象
- 如遇显存不足，建议在使用过程中关闭 `浏览器`、`VSCode` 及/或 `其他占用显存` 的软件
- 或者使用更低一个档次的启动脚本
