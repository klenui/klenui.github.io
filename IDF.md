## 개요
ESP 개발 환경인 IDF를 WSL([Windows Subsystem for Linux](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10))에 설치하고 
ESP-WROVER-KIT 개발을 위해 사용하는 과정을 기술합니다.

[ESP-IDF Programming Guide](https://docs.espressif.com/projects/esp-idf/en/latest/)

# 설치

[설치 매뉴얼](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/linux-setup.html)

테스트 해본 결과, WSL 환경에서도 빌드/설치/Flash/Monitor 모두 매끄럽게 돌아갑니다.(어쩌면 당연)
대신 monitor의 baud rate를 115200으로 해야하고, ubuntu에서 /dev/ttyUSB1이었던 포트이름이 WSL에서는 /dev/ttyS7로 보인다 정도의 차이가 있습니다.



# idf.py



