# course-helper-windows-build

Windows x64 构建流程，基于 [AneryCoft/course_helper](https://github.com/AneryCoft/course_helper) 1.2.4，源码提交固定为 `9df279e8558975777c9c686f5b07bc174ef6054f`。

## 获取程序

打开 [Actions 构建记录](https://github.com/KimAerielle/course-helper-windows-build/actions)，选择最近一次成功的 **Build Course Helper for Windows**，下载 **CourseHelper-Windows-x64** 产物。

产物包含 Windows 程序压缩包、对应源码压缩包和 SHA-256 校验文件。解压程序压缩包后，运行 `course_helper.exe`，并保留同目录的 DLL 文件和 `data` 文件夹。

## Windows 兼容处理

- 生成 Flutter Windows 启动工程。
- 补充 Windows 通知初始化配置。
- Windows 启动时跳过手机端环信 IM SDK，因此手机端 IM 实时通知在本构建中不可用。
- 摄像头扫码等移动平台功能受 Windows 插件支持范围限制。

## 验证与源码

构建流程包含原生 Windows 启动和账号页切换测试，通过后才编译 Release。测试不登录学习通或雨课堂，在线课程功能需由使用者自行验证。

源码包包含本次构建使用的 Windows 工程和兼容调整，原项目许可证一并附在程序中。
