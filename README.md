## KeywordGacha Server
- 与 [KeywordGacha](https://github.com/neavo/KeywordGacha) 配套的本地大模型一键包
- 也可以作为 [SakuraLLM](https://github.com/SakuraLLM/SakuraLLM) 轻小说翻译模型的服务器来使用

## 作为 KeywordGacha 服务器使用
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [Release下载页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的一键包，解压缩到本地；
- 从 Qwen2 的官方下载页下载 Qwen2-7B 模型文件，放到到上面的文件夹里
- --> [Qwen2 国内下载地址](https://modelscope.cn/models/qwen/Qwen2-7B-Instruct-GGUF/file/view/master?fileName=qwen2-7b-instruct-q4_k_m.gguf&status=2)    --> [Qwen2 海外下载地址](https://huggingface.co/Qwen/Qwen2-7B-Instruct-GGUF/blob/main/qwen2-7b-instruct-q4_k_m.gguf)
- 现在你的文件结构应该类似于：
  
  ```
  KeywordGachaServer\llama\...
                    \common.bat
                    \00_RUN_NP2_3K.bat
                    \qwen2-7b-instruct-q4_k_m.gguf
                    \...
  ```

- 双击 00_RUN_NP2_3K.bat，会开启一个黑色的终端窗口
- 一阵文字滚动后，看到有类似 `all slots are idle | tid="xxx" timestamp=xxx` 的字样就说明成功启动了
- 关闭终端窗口即为关闭服务器

## 作为 SakuraLLM 服务器使用
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [Release下载页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的一键包，解压缩到本地；
- 根据你的显存大小下载对应的 SakuraLLM 模型并放入上面的文件夹
- 显存 < 11G --> [GalTransl-7B-v1.5](https://huggingface.co/SakuraLLM/GalTransl-7B-v1.5/blob/main/GalTransl-7B-v1.5-IQ4_XS.gguf)
- 显存 >= 11G --> [Sakura-14B-Qwen2beta-v0.9.2-GGUF](https://huggingface.co/SakuraLLM/Sakura-14B-Qwen2beta-v0.9.2-GGUF/blob/main/sakura-14b-qwen2beta-v0.9.2-iq4xs.gguf)
- 双击 `显存大小对应的脚本`，选择对应的模型使用即可
- 与 [AiNiee](https://github.com/NEKOparapa/AiNiee) 翻译器搭配使用的话，可以参考这里的教程 [SakuraLLM 性能优化指南](https://github.com/NEKOparapa/AiNiee/blob/main/SakuraLLMScript/OptimizationGuide.md)

　　　　
> [!CAUTION]
> 
> 每个人的系统环境不同，显存占用有波动是正常现象
> 
> 如遇显存不足，建议在使用过程中关闭浏览器的硬件加速及其他占用显存的软件
