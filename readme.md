登录参考
https://supabase.com/docs/guides/auth/server-side/nextjs

## 优化安装时间

为了减少应用的安装时间，我们进行了以下优化：

### 快速构建脚本

使用以下命令进行优化构建：

```bash
#https://gitlab.winehq.org/wine/wine/-/wikis/Debian-Ubuntu
#https://www.electron.build/multi-platform-build#to-build-app-for-windows-on-linux
sudo apt-get update
sudo apt-get install --no-install-recommends -y winehq-stable

# 快速构建（使用缓存和优化配置）
pnpm build:quick

# 超快速构建（包含依赖优化）
pnpm build:super-fast

# 最大速度构建（全方位优化）
pnpm build:max-speed
```

### 优化内容

1. **构建优化**：
   - 减少压缩级别，加快构建和安装
   - 使用asar打包，提高安装效率
   - 使用缓存加速构建过程

2. **依赖优化**：
   - 减少不必要的依赖文件
   - 合并重复依赖
   - 排除开发相关文件

3. **安装优化**：
   - 优化NSIS安装脚本
   - 减少文件IO操作
   - 改善用户安装体验

使用优化方案后，应用安装时间预计可从10分钟减少到1-2分钟左右。
