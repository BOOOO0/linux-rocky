# WHP

- VMWare Wokrstation을 설치할 때 WHP의 설치에 대한 질문이 나타납니다. 여기서 WHP가 무엇이고 윈도우의 Hyper-V와 가상머신에서의 Hyper-V가 어떻게 다른지 살펴보겠습니다.

- 우선 하이퍼바이저는 호스트 컴퓨터에서 다수의 운영 체제를 동시에 실행할 수 있는 논리적 플랫폼을 의미합니다.

- Windows에서 제공하는 Hyper-V는 level 1 하이퍼바이저(Native)이고 VMware는 level 2 하이퍼바이저(hosted) 입니다. level2 하이퍼바이저는 OS에서 어플리케이션으로 실행되지만 level 1 하이퍼바이저는 OS 자체로 하이퍼바이저가 실행됩니다.

- Hyper-V가 활성화되는 경우 현재 내 컴퓨터의 Host OS인 Windows 자체가 Hyper-V의 가상머신이 되므로 이 가상머신 위에서 다른 하이퍼바이저 플랫폼을 사용하면 그 하이퍼바이저는 자신의 게스트 OS에 가상 자원을 할당할 수 없기 때문에 오류가 발생하는 것입니다.

- 두가지의 차이점을 설명하자면 지금 저의 컴퓨터에는 WSL을 통해 우분투를 사용중입니다. 우분투를 설치하고 사용하기 위해 BIOS에서 Hyper-V를 활성화시킨 상태이고 Hyper-V라는 플랫폼 위에 기존에 설치된 Windows와 Ubuntu가 게스트 OS인 것입니다.

- VMware를 사용하는 경우엔 Windows와 Ubuntu가 호스트 OS가 되고 하이퍼바이저로 VMWare Workstation을 두고 가상머신을 실행해 게스트 OS로 필요한 운영체제를 사용하는 것입니다.

- Windows Hypervisor Platform(WHP)은 다른 level 2 하이퍼바이저 플랫폼에 Hyper-V의 호스트 컴퓨팅 시스템 API를 제공합니다. 그로 인해 level 2 하이퍼바이저 플랫폼인 VMware에서도 자신이 생성하는 가상머신에 가상 자원을 할당할 수 있게 됩니다.
