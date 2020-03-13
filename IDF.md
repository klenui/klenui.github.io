## 개요
ESP 개발 환경인 IDF를 WSL([Windows Subsystem for Linux](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10))에 설치하고 
[ESP-WROVER-KIT](https://docs.espressif.com/projects/esp-idf/en/latest/hw-reference/get-started-wrover-kit.html) 
개발을 위해 사용하는 과정을 기술합니다.

[ESP-IDF Programming Guide](https://docs.espressif.com/projects/esp-idf/en/latest/)

# 설치

[ESPRESSIF DOC](https://docs.espressif.com/projects/esp-idf/en/latest/get-started/linux-setup.html)

테스트 해본 결과, WSL 환경에서도 빌드/설치/Flash/Monitor 모두 매끄럽게 돌아갑니다.(어쩌면 당연)
대신 monitor의 baud rate를 115200으로 해야하고, flash/monitor를 위한 port가 다르게 보일수 있습니다.
(WSL의 flash 단계에서 flash가 끝나지 않고 계속 대기중인 경우 baud rate를 조정해야 함)

[esptool baud rate 460800 & Openocd both fail on WSL (IDFGH-1796)](https://github.com/espressif/esp-idf/issues/4008)
[Amazon FreeRTOS](https://docs.aws.amazon.com/ko_kr/freertos/latest/userguide/getting_started_espressif.html)

# IDF 빌드 시스템

[ESPRESSIF DOC](https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html#)

IDF project는 app 혹은 bootloader를 빌드할수 있습니다.
각 프로젝트는 component들로 구성되는데, 기본으로 main component와 componenets 디렉토리 아래의 component들을 포함합니다.
main이 아닌 다른 폴더를 추가하고 싶을 때는 EXTRA_COMPONENT_DIRS 변수에 추가해 줍니다.

[Renaming main component](https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html#rename-main)

# IDF Component

Component는 각 폴더에 idf_component_register를 포함하는 CMakeLists.txt를 포함하고 있어야 합니다.

# CMake 사용

[ESPRESSIF DOC](https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html#using-esp-idf-in-custom-cmake-projects)

idf project.make를 사용하지 않고, 일반 cmake에서 IDF build를 가져다 사용하는 방법입니다.






