# 커널 (Kernel)

커널은 운영 체제의 핵심 구성 요소로, 하드웨어와 소프트웨어 간의 상호 작용을 관리합니다. 커널의 주요 기능은 다음과 같습니다:

- 프로세스 관리: 프로세스의 생성, 스케줄링, 종료 등을 관리합니다.
- 메모리 관리: 메모리 할당, 해제 및 메모리 보호 기능을 제공합니다.
- 장치 관리: 하드웨어 장치와의 통신을 관리합니다.
- 파일 시스템 관리: 파일과 디렉토리를 관리하고 파일 시스템을 유지합니다.
- 보안 및 권한 관리: 사용자와 프로세스의 권한을 관리하여 시스템 보안을 유지합니다.

# 이중 모드 (Dual Mode)

이중 모드는 컴퓨터 시스템에서 두 가지 운영 모드를 제공하여 시스템 안정성과 보안을 보장합니다. 두 가지 모드는 다음과 같습니다:

- 사용자 모드 (User Mode): 애플리케이션 프로그램이 실행되는 모드로, 시스템 자원에 대한 제한된 접근 권한을 가집니다. 잘못된 명령이 실행되더라도 시스템 전체에 영향을 주지 않습니다.
- 커널 모드 (Kernel Mode): 운영 체제가 실행되는 모드로, 하드웨어와 시스템 자원에 대한 완전한 접근 권한을 가집니다. 커널 모드에서는 시스템 전체를 제어할 수 있기 때문에, 이 모드에서 오류가 발생하면 시스템 전체에 영향을 미칠 수 있습니다.
- 이중 모드는 CPU의 모드 비트(mode bit)를 통해 전환됩니다. 사용자 모드에서 커널 모드로 전환되는 주요 예는 시스템 호출(system call)입니다.

# 시스템 호출 (System Call)

시스템 호출은 사용자 프로그램이 운영 체제의 서비스를 요청하는 메커니즘입니다. 예를 들어, 파일을 읽거나 쓰기, 프로세스를 생성하거나 종료하기, 메모리를 할당하는 등의 작업이 시스템 호출을 통해 이루어집니다.

시스템 호출의 기본 과정은 다음과 같습니다:

- 트랩(Trap) 발생: 사용자 프로그램이 시스템 호출 명령을 실행하면, 트랩이 발생하여 사용자 모드에서 커널 모드로 전환됩니다.
- 커널 서비스 실행: 커널은 시스템 호출 번호를 참조하여 해당 서비스를 실행합니다.
- 결과 반환: 서비스가 완료되면 커널 모드에서 사용자 모드로 전환되고, 결과가 사용자 프로그램에 반환됩니다.
  시스템 호출은 프로그래머가 직접 사용하기 보다는 고수준의 라이브러리나 API를 통해 호출되는 경우가 많습니다.
