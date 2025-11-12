
# Minecraft 存档（saves）

本仓库保存了 Minecraft 世界的存档文件（saves 目录）。它可以用作备份、分享或协作恢复世界的手段。

## 包含内容
- 区域文件（region / *.mca）
- 玩家数据（playerdata）
- 维度数据（DIM-1、DIM1）
- 其他世界相关数据（poi、advancements、stats、datapacks 等）

> 注意：Minecraft 存档通常包含大量二进制文件，仓库大小可能迅速增加。

## 使用说明
1. 克隆仓库：
	```bash
	git clone https://github.com/zhengyinloong/Minecraft_saves.git
	```
2. 恢复到本地 Minecraft：将本仓库中的整个存档目录（本目录）复制到你的 Minecraft 安装目录下的 `saves` 文件夹中，路径示例：
	- Windows: `%appdata%\.minecraft\saves\<worldname>`
	- Fabric 多版本环境：将本目录复制到对应运行版本的 `saves` 中
3. 启动游戏并选择对应存档打开。

## 同步与提交建议
- 在提交前检查 `.gitignore`，不要把临时或自动生成的文件（例如崩溃日志、临时备份）加入版本控制。
- 对于大型且频繁变化的二进制文件（如大量 `.mca` 区域文件），建议使用 Git LFS：
  ```powershell
  git lfs install
  git lfs track "*.mca"
  git add .gitattributes
  git add <large-files>
  git commit -m "Track .mca with LFS"
  git push origin main
  ```

## 备份与安全
- 在覆盖本地世界前请先备份本地 `saves` 文件夹。
- 如果多人协作，建议使用分支或每天的增量备份，避免冲突导致存档损坏。

## 贡献与问题
- 如果你要上传大的变更或新的存档，请先在 Issues 中说明，并尽量告知变更大小。

## 免责声明
本仓库主要用于个人/小团体的存档备份与分享。上传或下载前请自行备份重要存档；对因操作导致的数据丢失概不负责。

