### KeywordGachaServer
- 与 [KeywordGacha](https://github.com/neavo/KeywordGacha) 配套的本地大模型一键包

### 使用
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [Release下载页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的一键包，解压缩到本地；
- 从 Qwen2 官方的下载页下载 Qwen2-7B 模型文件，然后解压缩到上面的文件夹里 --> [国内地址](https://modelscope.cn/models/qwen/Qwen2-7B-Instruct-GGUF/file/view/master?fileName=qwen2-7b-instruct-q4_k_m.gguf&status=2)  --> [海外地址](https://huggingface.co/Qwen/Qwen2-7B-Instruct-GGUF/blob/main/qwen2-7b-instruct-q4_k_m.gguf)
- 现在你的文件结构应该是：
```
KeywordGachaServer\llama\...
                  \common.bat
                  \00_RUN_NP2_3K.bat
                  \qwen2-7b-instruct-q4_k_m.gguf
```
- 双击 00_RUN_NP2_3K.bat，会开启一个黑色的终端窗口。
- 一阵文字滚动后，看到会有类似 `all slots are idle | tid="6188" timestamp=1719838812` 的字样就说明成功启动了。
- 你可以开始使用 [KeywordGacha](https://github.com/neavo/KeywordGacha) 了。
