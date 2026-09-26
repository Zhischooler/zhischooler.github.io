

在音视频处理领域，**FFmpeg** 是当之无愧的王者。无论是格式转换、视频裁剪、提取音频，还是压缩体积、添加水印，它都能通过几行简单的命令行轻松搞定。

## 1. 安装 FFmpeg

- **Windows**：前往官网下载 Build 版本，解压后将 `bin` 目录添加到系统环境变量 PATH 中。
- **macOS**：使用 Homebrew 一键安装：`brew install ffmpeg`
- **Linux**：使用 apt 安装：`sudo apt install ffmpeg`

## 2. 核心语法逻辑

```bash
ffmpeg [全局参数] -i [输入文件] [处理参数] [输出文件]
```

## 3. 高频实战命令

###  格式转换
```bash
ffmpeg -i input.mp4 output.mkv
```

###  提取音频
```bash
ffmpeg -i video.mp4 -vn -acodec mp3 audio.mp3
```

###  裁剪视频
```bash
ffmpeg -i input.mp4 -ss 00:00:10 -t 5 -c copy output.mp4
```

###  压缩体积
```bash
ffmpeg -i input.mp4 -vf scale=1280:-1 -b:v 1000k output.mp4
```

### 调整速度
```bash
ffmpeg -i input.mp4 -vf "setpts=0.5*PTS" -af "atempo=2.0" output.mp4
```

### 合并视频
创建 `list.txt`：
```text
file 'part1.mp4'
file 'part2.mp4'
```
执行：
```bash
ffmpeg -f concat -safe 0 -i list.txt -c copy output.mp4
```

###  添加水印
```bash
ffmpeg -i input.mp4 -i watermark.png -filter_complex "overlay=W-w-10:H-h-10" output.mp4
```
<!-- ##{"timestamp":1789872832}## -->

