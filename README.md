## KeywordGacha Server
- 与 [KeywordGacha](https://github.com/neavo/KeywordGacha) 配套的本地大模型服务器端一键包

## 步骤
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [Release下载页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的一键包，解压缩到本地；
- 下载模型 --> [GLM4-9B-Chat-GGUF](https://huggingface.co/second-state/glm-4-9b-chat-GGUF/blob/main/glm-4-9b-chat-Q4_K_S.gguf)，放到到上面的文件夹里
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

## 其他说明
- 每个人的系统环境不同，显存占用有波动是正常现象
- 如遇显存不足，建议在使用过程中关闭 `浏览器`、`VSCode` 及/或 `其他占用显存` 的软件
- 或者使用更低一个档次的启动脚本
