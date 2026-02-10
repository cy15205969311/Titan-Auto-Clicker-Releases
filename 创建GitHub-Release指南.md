# 创建 GitHub Release 指南

## 方法一：通过 GitHub 网页创建（推荐）

### 步骤：

1. **访问 Releases 页面**
   - 打开：https://github.com/cy15205969311/Titan-Auto-Clicker-Releases/releases
   - 点击 "Create a new release" 按钮

2. **选择 Tag**
   - 在 "Choose a tag" 下拉框中选择 `v1.0`
   - 或者输入 `v1.0` 并选择现有的 tag

3. **填写 Release 信息**

   **Release title（发布标题）：**
   ```
   Titan 连点器 v1.0 - 修复闪退问题
   ```

   **Describe this release（发布说明）：**
   ```markdown
   # Titan 连点器 v1.0

   ## 🎉 主要更新

   ### 修复问题
   - ✅ 修复红米K60和雷电模拟器上的闪退问题
   - ✅ 修复应用退出后再次打开闪退的问题
   - ✅ 修复Gson序列化失败导致的崩溃

   ### 技术改进
   - 🔧 完善ProGuard混淆规则，保留所有关键类
   - 🔧 添加TitanApplication全局异常捕获
   - 🔧 保留Model、Service、Utils类不被混淆
   - 🔧 添加崩溃日志输出，便于调试
   - 🔧 保留行号信息，方便定位问题

   ### 界面优化
   - 🎨 更新应用图标为PNG格式
   - 🎨 优化图标显示效果

   ## 📦 下载

   - **APK文件：** Titan-AutoClicker-v1.0.apk
   - **文件大小：** 2.9 MB
   - **最低系统：** Android 7.0
   - **目标系统：** Android 14

   ## 🔧 安装说明

   1. 下载 `Titan-AutoClicker-v1.0.apk`
   2. 在手机上安装APK
   3. 首次打开时授予必要权限：
      - 无障碍服务权限
      - 悬浮窗权限
   4. 开始使用

   ## ⚠️ 重要提示

   - 如果之前安装过旧版本，建议先卸载再安装新版本
   - 新版本修复了闪退问题，可以正常退出后再次打开
   - 所有数据保存在本地，不会上传到服务器

   ## 📝 使用说明

   详细使用说明请查看：[README.md](https://github.com/cy15205969311/Titan-Auto-Clicker-Releases/blob/main/README.md)

   ## 🐛 问题反馈

   如果遇到问题，请在 [Issues](https://github.com/cy15205969311/Titan-Auto-Clicker-Releases/issues) 中反馈。

   ## 📸 应用截图

   查看更多截图：[screenshots](https://github.com/cy15205969311/Titan-Auto-Clicker-Releases/tree/main/screenshots)
   ```

4. **上传 APK 文件**
   - 在 "Attach binaries by dropping them here or selecting them" 区域
   - 点击或拖拽上传 `Titan-AutoClicker-v1.0.apk` 文件
   - 等待上传完成

5. **发布**
   - 确认信息无误
   - 点击 "Publish release" 按钮

---

## 方法二：使用 GitHub CLI（需要安装 gh）

### 前提条件
安装 GitHub CLI：https://cli.github.com/

### 命令：

```bash
# 进入仓库目录
cd Titan-Auto-Clicker-Releases

# 创建 Release 并上传 APK
gh release create v1.0 Titan-AutoClicker-v1.0.apk \
  --title "Titan 连点器 v1.0 - 修复闪退问题" \
  --notes "主要修复：
- 修复红米K60和雷电模拟器上的闪退问题
- 完善ProGuard混淆规则
- 添加全局异常捕获
- 更新应用图标

技术改进：
- 保留所有关键类不被混淆
- 修复Gson序列化失败问题
- 添加崩溃日志输出
- 应用现在可以正常退出后再次打开"
```

---

## 验证 Release

创建完成后：
1. 访问：https://github.com/cy15205969311/Titan-Auto-Clicker-Releases/releases
2. 确认 v1.0 Release 已显示
3. 确认 APK 文件可以下载
4. 测试下载链接是否正常

---

## 常见问题

### Q: 为什么 Releases 页面显示 "There aren't any releases here"？
A: 因为只推送了 tag，还没有创建 Release。需要按照上面的步骤手动创建。

### Q: 可以直接在 Tags 页面下载 APK 吗？
A: 不可以。Tags 只是代码的快照，不包含二进制文件。必须创建 Release 才能上传 APK。

### Q: 如何更新已发布的 Release？
A: 在 Release 页面点击 "Edit release"，可以修改说明或重新上传文件。

---

**推荐使用方法一（网页创建），更直观方便！**
