# AppleMusicGUI版AAC下载器使用方法
**原地址**：[地址](https://github.com/Zhischooler/applemusic-aac-gui)
_使用截图_

<img width="1920" height="897" alt="Image" src="https://github.com/user-attachments/assets/9b7eedfd-31de-4b78-b976-e3b088b28b1e" />

## 📦 依赖

* Python 3.10+

* [gamdl](https://github.com/glomatico/gamdl) ≥ 2.7.0
 
* [FFmpeg](https://ffmpeg.org/)（用于转码，若不需要转 FLAC 可省略）
 
* PySide6（GUI 框架）

## 🚀 快速开始

### 1\. 克隆仓库

```bash
git clone https://github.com/Zhischooler/apple-music-aac-gui.git
cd apple-music-aac-gui
```

2. 安装依赖

```bash
pip install -r requirements.txt
```

3. 安装 FFmpeg（如需转 FLAC）

· Windows：下载 ffmpeg.org 并添加到 PATH。

·macOS：
```bash
brew install ffmpeg
```

· Linux：
```bash
sudo apt install ffmpeg
```
（或其他包管理器）

4. 获取 Cookies

使用浏览器扩展（如 Get cookies.txt LOCALLY）从 music.apple.com 导出 cookies.txt（Netscape 格式）。

5. 运行

```bash
python apple_music_gui.py
```

⚙️ 配置文件

程序首次运行会自动生成 config.txt，格式如下：

```
coversize:600x600      # 封面尺寸（宽x高）
downloadlyrics:true    # 是否下载歌词
m4atoflac:false        # 是否转 FLAC
```
true代表是，false代表否。

你可以直接修改文件或通过 GUI 实时调整，修改后会自动保存。

## 注意！
- 本工具仅供学习和个人使用，请勿用于商业目的或侵犯版权。
- 作者不对因使用本工具造成的任何后果负责。


