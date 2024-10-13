## KeywordGacha Server
- 与 [KeywordGacha](https://github.com/neavo/KeywordGacha) 配套的本地模型一键包

## 步骤
- 请确保你使用的是至少 8G 显存的 Nvidia 显卡，并且安装了最新版本的驱动程序
- 从 [发布页](https://github.com/neavo/KeywordGachaServer/releases) 下载最新的 `KeywordGachaServer` 并解压缩
- 下载模型 --> [glm-4-9b-chat-IQ4_XS.gguf](https://huggingface.co/bartowski/glm-4-9b-chat-GGUF/blob/main/glm-4-9b-chat-IQ4_XS.gguf) 并放入 `KeywordGachaServer` 文件夹
- 现在你的文件结构应该类似于：
  
  ```
  KeywordGachaServer\llama\...
                    \00_Core.bat
                    \01_2K_NP8.bat
                    \glm-4-9b-chat-IQ4_XS.gguf
                    \...
  ```

- 双击 01_2K_NP8.bat，会开启一个黑色的终端窗口
- 一阵文字滚动后，看到有类似 `all slots are idle` 的字样就说明成功启动了
- 关闭黑色的终端窗口即为关闭服务器

## 常见问题
- 什么是 `爆显存`，会导致什么问题？
  - 系统需求的显存超过了显卡实际的物理显存大小，称之为 `爆显存`
  - `爆显存` 时，翻译的速度和结果都会出现异常，基本丧失可用性，所以要避免这种情况
    
- 如何判断是否 `爆显存`
  - 如果爆的比较厉害，程序会直接报错或者退出
  - 爆了一点又没有完全爆比较难判断
  - 一个可参考的方式是通过第三方软件监测显卡功耗
  - 满载执行任务时，显卡实际功耗应为最大功耗的 `70%-80%` 或者更高
  - 如果显存接近用完，但是显卡实际功耗很低，则大概率是爆显存了

- 如何避免 `爆显存`
  - 在模型启动后，模型占用的显存大小是固定的，不会变化，但是系统中的其他应用也会占用显存
  - 本项目中的脚本都预留了一定的冗余空间，但如果开启过多应用，依然可能导致显存消耗完
  - 所以在使用时，应尽量减少开启其他消耗显存的应用
  - 比如 `浏览器`、`动态壁纸`、`视频播放器` 或 `QQNT`、`VSCODE` 等基于浏览器内核的应用
