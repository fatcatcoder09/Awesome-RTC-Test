# Awesome-RTC-Test

[English Version](README_EN.md)

## 音频质量测试框架

### AATT (Automated Audio Test Tool)
Google开源的WebRTC音频测试工具  
GitHub: [https://github.com/webrtc/AATT](https://github.com/webrtc/AATT)  
特点: 
- 可以进行音频质量、延迟、噪声等自动化测试
- 支持多种音频编解码器
- 提供详细的测试报告和分析

### WebRTC-APM-Test
WebRTC音频处理模块的测试框架  
GitHub: [https://github.com/wiseman/py-webrtcvad](https://github.com/wiseman/py-webrtcvad)  
提供了完整的音频前处理测试方案:
- 包含噪声抑制、回声消除、增益控制等处理模块
- 支持多种音频输入输出格式
- 可以模拟不同的音频环境进行测试

## 音频分析工具

### Asterisk Test Suite
Asterisk项目的测试套件  
GitHub: [https://github.com/asterisk/test-suite](https://github.com/asterisk/test-suite)  
包含了大量VoIP音频测试用例:
- 支持SIP、PJSIP等协议的测试
- 提供音频质量、延迟、抖动等测试功能
- 可以与Asterisk服务器集成进行端到端测试

### Audio Quality Test Tools
Mozilla开源的音频质量测试工具集  
GitHub: [https://github.com/mozilla/audio-test-tools](https://github.com/mozilla/audio-test-tools)  
支持音频编解码器性能测试:
- 包含音频编码、解码、转码等功能
- 提供音频质量评估工具，如PESQ、POLQA等
- 支持批量测试和自动化测试

## 网络模拟工具

### Network Link Conditioner
Apple开源的网络条件模拟工具  
可以模拟各种网络环境下的音频传输:
- 支持带宽限制、延迟、丢包等网络条件
- 可以模拟Wi-Fi、4G、3G等不同网络类型
- 提供简单易用的图形界面

### netem
Linux内核的网络模拟模块  
常用于WebRTC测试:
- 支持延迟、抖动、丢包、带宽限制等网络条件
- 可以与其他网络工具结合使用，如tc、iptables等
- 提供灵活的命令行接口

## 音频指标测量

### PESQ-Python
PESQ算法的Python实现  
GitHub: [https://github.com/vBaiCai/python-pesq](https://github.com/vBaiCai/python-pesq)  
用于测量音频感知质量:
- 支持PESQ (Perceptual Evaluation of Speech Quality) 算法
- 可以评估不同编码器、网络条件下的音频质量
- 提供详细的质量评分和分析报告

### PyDSP
数字信号处理工具库  
GitHub: [https://github.com/pydsp/pydsp](https://github.com/pydsp/pydsp)  
提供音频分析功能:
- 包含滤波、频谱分析、信号变换等功能
- 支持多种音频格式和采样率
- 提供简单易用的Python接口

## 构建自己的测试框架建议

如果您想构建自己的测试框架, 我建议可以:
- 参考 AATT 的整体架构设计
- 使用 WebRTC-APM-Test 的音频处理测试方案
- 集成 PESQ-Python 进行质量评估
- 采用 netem 进行网络模拟

## 如何使用这些工具对视频会议软件进行测试

### 使用 AATT 进行音频质量测试
1. 克隆 AATT 仓库并安装依赖:
    ```bash
    git clone https://github.com/webrtc/AATT.git
    cd AATT
    npm install
    ```
2. 配置测试参数，例如音频文件路径、测试类型等。
3. 运行测试并生成报告:
    ```bash
    npm run test
    ```

### 使用 WebRTC-APM-Test 进行音频处理测试
1. 克隆 WebRTC-APM-Test 仓库并安装依赖:
    ```bash
    git clone https://github.com/wiseman/py-webrtcvad.git
    cd py-webrtcvad
    pip install -r requirements.txt
    ```
2. 配置测试参数，例如输入音频文件、处理模块等。
3. 运行测试并分析结果:
    ```bash
    python run_tests.py
    ```

### 使用 Asterisk Test Suite 进行VoIP音频测试
1. 克隆 Asterisk Test Suite 仓库并安装依赖:
    ```bash
    git clone https://github.com/asterisk/test-suite.git
    cd test-suite
    ./install_prerequisites.sh
    ```
2. 配置Asterisk服务器和测试用例。
3. 运行测试并生成报告:
    ```bash
    ./run_tests.sh
    ```

### 使用 Audio Quality Test Tools 进行音频编解码器性能测试
1. 克隆 Audio Quality Test Tools 仓库并安装依赖:
    ```bash
    git clone https://github.com/mozilla/audio-test-tools.git
    cd audio-test-tools
    pip install -r requirements.txt
    ```
2. 配置测试参数，例如编码器、解码器、音频文件等。
3. 运行测试并生成报告:
    ```bash
    python run_tests.py
    ```

### 使用 Network Link Conditioner 模拟网络条件
1. 下载并安装 Network Link Conditioner。
2. 配置网络条件，例如带宽限制、延迟、丢包等。
3. 启动 Network Link Conditioner 并运行 Zoom 进行测试。

### 使用 netem 模拟网络条件
1. 在Linux系统上安装 netem:
    ```bash
    sudo apt-get install iproute2
    ```
2. 配置网络条件，例如延迟、抖动、丢包等:
    ```bash
    sudo tc qdisc add dev eth0 root netem delay 100ms
    ```
3. 运行 Zoom 进行测试。

### 使用 PESQ-Python 测量音频感知质量
1. 克隆 PESQ-Python 仓库并安装依赖:
    ```bash
    git clone https://github.com/vBaiCai/python-pesq.git
    cd python-pesq
    pip install -r requirements.txt
    ```
2. 配置测试参数，例如参考音频文件、测试音频文件等。
3. 运行测试并生成质量评分:
    ```bash
    python pesq_test.py
    ```

### 使用 PyDSP 进行音频分析
1. 克隆 PyDSP 仓库并安装依赖:
    ```bash
    git clone https://github.com/pydsp/pydsp.git
    cd pydsp
    pip install -r requirements.txt
    ```
2. 配置分析参数，例如音频文件、分析类型等。
3. 运行分析并生成报告:
    ```bash
    python analyze.py
    ```

## 桌面端视频会议客户端测试工具

### TestRTC
TestRTC 是一个专门用于测试 WebRTC 应用的工具，支持桌面端视频会议客户端的测试。
- 特点:
  - 支持端到端的 WebRTC 测试
  - 提供实时监控和报告功能
  - 支持模拟不同的网络条件
- 使用方法:
  1. 注册并登录 TestRTC 平台。
  2. 创建一个新的测试用例，配置测试参数，例如测试 URL、网络条件等。
  3. 运行测试并查看实时监控和报告。

### Pion WebRTC
Pion WebRTC 是一个开源的 WebRTC 实现，支持桌面端视频会议客户端的测试。
- 特点:
  - 提供灵活的 API 接口
  - 支持多种编程语言
  - 可以与其他测试工具结合使用
- 使用方法:
  1. 克隆 Pion WebRTC 仓库并安装依赖:
      ```bash
      git clone https://github.com/pion/webrtc.git
      cd webrtc
      go get ./...
      ```
  2. 编写测试脚本，配置测试参数，例如视频流、音频流等。
  3. 运行测试脚本并分析结果。

### Selenium
Selenium 是一个广泛使用的自动化测试工具，可以用于测试桌面端视频会议客户端的 Web 界面。
- 特点:
  - 支持多种浏览器和操作系统
  - 提供丰富的 API 接口
  - 支持自动化测试脚本的编写
- 使用方法:
  1. 安装 Selenium 和浏览器驱动:
      ```bash
      pip install selenium
      ```
  2. 编写测试脚本，配置测试参数，例如测试 URL、用户操作等。
  3. 运行测试脚本并生成报告。

通过以上步骤，您可以使用这些工具对视频会议软件（例如Zoom）进行全面的音频质量、处理、网络条件模拟和指标测量测试。