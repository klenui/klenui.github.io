## 개요
ESP 개발 환경인 IDF를 WSL([Windows Subsystem for Linux](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10))에 설치하고 
[ESP-WROVER-KIT](https://docs.espressif.com/projects/esp-idf/en/latest/hw-reference/get-started-wrover-kit.html) 
개발을 위해 사용하는 과정을 기술합니다.

[ESP-IDF Programming Guide](https://docs.espressif.com/projects/esp-idf/en/latest/)

# 설치

[설치 매뉴얼](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/linux-setup.html)

테스트 해본 결과, WSL 환경에서도 빌드/설치/Flash/Monitor 모두 매끄럽게 돌아갑니다.(어쩌면 당연)
대신 monitor의 baud rate를 115200으로 해야하고, flash/monitor를 위한 port가 다르게 보일수 있습니다.
(WSL의 flash 단계에서 flash가 끝나지 않고 계속 대기중인 경우 baud rate를 조정해야 함)
제 경우엔, ubuntu에서 /dev/ttyUSB1이었던 포트이름이 WSL에서는 /dev/ttyS7로 보이네요.


# idf.py





