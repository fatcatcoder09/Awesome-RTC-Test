# Awesome-RTC-Test

[中文版](README_CH.md)

## Audio Quality Test Framework

### AATT (Automated Audio Test Tool)
Google's open-source WebRTC audio test tool  
GitHub: [https://github.com/webrtc/AATT](https://github.com/webrtc/AATT)  
Features: 
- Automated testing for audio quality, latency, noise, etc.
- Supports various audio codecs
- Provides detailed test reports and analysis

### WebRTC-APM-Test
Test framework for WebRTC audio processing module  
GitHub: [https://github.com/wiseman/py-webrtcvad](https://github.com/wiseman/py-webrtcvad)  
Provides a complete audio pre-processing test solution:
- Includes noise suppression, echo cancellation, gain control, etc.
- Supports various audio input and output formats
- Can simulate different audio environments for testing

## Audio Analysis Tools

### Asterisk Test Suite
Test suite for the Asterisk project  
GitHub: [https://github.com/asterisk/test-suite](https://github.com/asterisk/test-suite)  
Contains numerous VoIP audio test cases:
- Supports SIP, PJSIP, and other protocols
- Provides audio quality, latency, jitter testing functions
- Can integrate with Asterisk server for end-to-end testing

### Audio Quality Test Tools
Mozilla's open-source audio quality test toolset  
GitHub: [https://github.com/mozilla/audio-test-tools](https://github.com/mozilla/audio-test-tools)  
Supports audio codec performance testing:
- Includes audio encoding, decoding, transcoding functions
- Provides audio quality evaluation tools like PESQ, POLQA
- Supports batch testing and automation

## Network Simulation Tools

### Network Link Conditioner
Apple's open-source network condition simulation tool  
Can simulate audio transmission under various network conditions:
- Supports bandwidth limitation, latency, packet loss, etc.
- Can simulate different network types like Wi-Fi, 4G, 3G
- Provides an easy-to-use graphical interface

### netem
Linux kernel network emulation module  
Commonly used for WebRTC testing:
- Supports delay, jitter, packet loss, bandwidth limitation, etc.
- Can be combined with other network tools like tc, iptables
- Provides a flexible command-line interface

## Audio Metrics Measurement

### PESQ-Python
Python implementation of the PESQ algorithm  
GitHub: [https://github.com/vBaiCai/python-pesq](https://github.com/vBaiCai/python-pesq)  
Used for measuring perceptual audio quality:
- Supports PESQ (Perceptual Evaluation of Speech Quality) algorithm
- Can evaluate audio quality under different codecs and network conditions
- Provides detailed quality scores and analysis reports

### PyDSP
Digital signal processing toolkit  
GitHub: [https://github.com/pydsp/pydsp](https://github.com/pydsp/pydsp)  
Provides audio analysis functions:
- Includes filtering, spectrum analysis, signal transformation, etc.
- Supports various audio formats and sampling rates
- Provides an easy-to-use Python interface

## Suggestions for Building Your Own Test Framework

If you want to build your own test framework, I suggest:
- Refer to the overall architecture design of AATT
- Use the audio processing test solution of WebRTC-APM-Test
- Integrate PESQ-Python for quality evaluation
- Use netem for network simulation

## How to Use These Tools to Test Video Conferencing Software

### Using AATT for Audio Quality Testing
1. Clone the AATT repository and install dependencies:
    ```bash
    git clone https://github.com/webrtc/AATT.git
    cd AATT
    npm install
    ```
2. Configure test parameters, such as audio file paths, test types, etc.
3. Run the test and generate a report:
    ```bash
    npm run test
    ```

### Using WebRTC-APM-Test for Audio Processing Testing
1. Clone the WebRTC-APM-Test repository and install dependencies:
    ```bash
    git clone https://github.com/wiseman/py-webrtcvad.git
    cd py-webrtcvad
    pip install -r requirements.txt
    ```
2. Configure test parameters, such as input audio files, processing modules, etc.
3. Run the test and analyze the results:
    ```bash
    python run_tests.py
    ```

### Using Asterisk Test Suite for VoIP Audio Testing
1. Clone the Asterisk Test Suite repository and install dependencies:
    ```bash
    git clone https://github.com/asterisk/test-suite.git
    cd test-suite
    ./install_prerequisites.sh
    ```
2. Configure the Asterisk server and test cases.
3. Run the test and generate a report:
    ```bash
    ./run_tests.sh
    ```

### Using Audio Quality Test Tools for Audio Codec Performance Testing
1. Clone the Audio Quality Test Tools repository and install dependencies:
    ```bash
    git clone https://github.com/mozilla/audio-test-tools.git
    cd audio-test-tools
    pip install -r requirements.txt
    ```
2. Configure test parameters, such as encoders, decoders, audio files, etc.
3. Run the test and generate a report:
    ```bash
    python run_tests.py
    ```

### Using Network Link Conditioner to Simulate Network Conditions
1. Download and install Network Link Conditioner.
2. Configure network conditions, such as bandwidth limitation, latency, packet loss, etc.
3. Start Network Link Conditioner and run Zoom for testing.

### Using netem to Simulate Network Conditions
1. Install netem on a Linux system:
    ```bash
    sudo apt-get install iproute2
    ```
2. Configure network conditions, such as delay, jitter, packet loss, etc.:
    ```bash
    sudo tc qdisc add dev eth0 root netem delay 100ms
    ```
3. Run Zoom for testing.

### Using PESQ-Python to Measure Perceptual Audio Quality
1. Clone the PESQ-Python repository and install dependencies:
    ```bash
    git clone https://github.com/vBaiCai/python-pesq.git
    cd python-pesq
    pip install -r requirements.txt
    ```
2. Configure test parameters, such as reference audio files, test audio files, etc.
3. Run the test and generate quality scores:
    ```bash
    python pesq_test.py
    ```

### Using PyDSP for Audio Analysis
1. Clone the PyDSP repository and install dependencies:
    ```bash
    git clone https://github.com/pydsp/pydsp.git
    cd pydsp
    pip install -r requirements.txt
    ```
2. Configure analysis parameters, such as audio files, analysis types, etc.
3. Run the analysis and generate a report:
    ```bash
    python analyze.py
    ```

## Desktop Video Conferencing Client Test Tools

### TestRTC
TestRTC is a tool specifically designed for testing WebRTC applications, supporting desktop video conferencing client testing.
- Features:
  - Supports end-to-end WebRTC testing
  - Provides real-time monitoring and reporting
  - Supports simulating different network conditions
- Usage:
  1. Register and log in to the TestRTC platform.
  2. Create a new test case, configure test parameters, such as test URL, network conditions, etc.
  3. Run the test and view real-time monitoring and reports.

### Pion WebRTC
Pion WebRTC is an open-source WebRTC implementation that supports desktop video conferencing client testing.
- Features:
  - Provides flexible API interfaces
  - Supports multiple programming languages
  - Can be used with other test tools
- Usage:
  1. Clone the Pion WebRTC repository and install dependencies:
      ```bash
      git clone https://github.com/pion/webrtc.git
      cd webrtc
      go get ./...
      ```
  2. Write test scripts, configure test parameters, such as video streams, audio streams, etc.
  3. Run the test scripts and analyze the results.

### Selenium
Selenium is a widely used automation testing tool that can be used to test the web interface of desktop video conferencing clients.
- Features:
  - Supports multiple browsers and operating systems
  - Provides rich API interfaces
  - Supports writing automated test scripts
- Usage:
  1. Install Selenium and browser drivers:
      ```bash
      pip install selenium
      ```
  2. Write test scripts, configure test parameters, such as test URL, user actions, etc.
  3. Run the test scripts and generate reports.

By following the above steps, you can use these tools to comprehensively test video conferencing software (e.g., Zoom) for audio quality, processing, network condition simulation, and metrics measurement.
