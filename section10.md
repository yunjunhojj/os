# 프로세스 개요

프로세스는 실행 중인 프로그램의 인스턴스로, 운영 체제에 의해 관리되고 실행되는 기본 단위입니다. 프로세스는 코드, 데이터, 스택 등의 메모리 공간과 CPU 상태 등을 포함합니다.

## 프로세스

프로세스는 다음과 같은 구성 요소로 이루어집니다:

- 프로그램 코드: 실행될 명령어들이 저장된 메모리 공간입니다.
- 프로그램 카운터(PC): 다음에 실행될 명령어의 주소를 가리킵니다.
- 프로세스 스택: 함수 호출과 지역 변수 등을 저장합니다.
- 프로세스 힙: 동적 메모리 할당을 위한 공간입니다.
- 데이터 섹션: 전역 변수들이 저장된 공간입니다.
- 프로세스는 생성, 준비, 실행, 대기, 종료의 상태를 가지며, 운영 체제는 이러한 상태 전이를 관리합니다.

- 프로세스 제어 블록 (Process Control Block, PCB)
- 프로세스 제어 블록은 운영 체제가 각 프로세스를 관리하기 위해 사용하는 데이터 구조체입니다. PCB에는 다음과 같은 정보가 포함됩니다:

- 프로세스 상태: 현재 프로세스의 상태 (예: 준비, 실행, 대기 등).
- 프로그램 카운터: 프로세스가 실행 중인 명령어의 주소.
- CPU 레지스터: 프로세스 실행 시의 CPU 레지스터 값.
- 메모리 관리 정보: 프로세스의 메모리 할당 정보.
- 계정 정보: 프로세스의 소유자, CPU 사용 시간, 우선순위 등.
- 입출력 상태 정보: 프로세스가 사용하는 입출력 장치 목록.

## 문맥 교환 (Context Switching)

문맥 교환은 CPU가 한 프로세스에서 다른 프로세스로 전환되는 과정입니다. 이 과정에서 현재 실행 중인 프로세스의 상태를 저장하고, 다음에 실행할 프로세스의 상태를 로드합니다. 문맥 교환의 단계는 다음과 같습니다:

- 현재 프로세스의 상태 저장: 현재 프로세스의 PCB에 CPU 레지스터, 프로그램 카운터, 메모리 관리 정보 등을 저장합니다.
- 새 프로세스의 상태 로드: 실행할 프로세스의 PCB에서 CPU 레지스터, 프로그램 카운터 등을 로드합니다.
- CPU 제어권 전환: 새 프로세스의 프로그램 카운터에 지정된 명령어를 실행합니다.
- 문맥 교환은 오버헤드가 발생하지만, 다중 프로세스 환경에서 CPU 자원을 효율적으로 사용하기 위해 필수적입니다.

## 프로세스 사용자 영역 (User Space)

프로세스 사용자 영역은 사용자 애플리케이션이 실행되는 메모리 공간입니다. 사용자 영역은 시스템 호출을 통해 커널 영역과 상호작용할 수 있습니다. 사용자 영역의 주요 구성 요소는 다음과 같습니다:

- 코드 섹션: 실행될 명령어들이 저장된 공간.
- 데이터 섹션: 전역 변수들이 저장된 공간.
- 힙: 동적 메모리 할당을 위한 공간.
- 스택: 함수 호출, 지역 변수 등이 저장된 공간.
- 사용자 영역에서 실행되는 프로그램은 직접 하드웨어 자원에 접근할 수 없으며, 시스템 호출을 통해 커널의 서비스를 요청해야 합니다.

# 스레드 (Thread)

스레드는 프로세스 내에서 실행되는 가장 작은 실행 단위입니다. 스레드는 프로세스의 리소스를 공유하면서 동시에 실행될 수 있는 경량 프로세스로 간주됩니다. 스레드는 독립적으로 실행되는 작업 흐름을 제공하며, 멀티스레딩을 통해 하나의 프로세스 내에서 여러 작업을 병렬로 수행할 수 있습니다.

## 스레드의 특징

- 공유 메모리: 같은 프로세스 내의 스레드는 메모리 공간(코드, 데이터 섹션, 힙)을 공유합니다.

- 독립된 실행 흐름: 각 스레드는 독립적인 실행 흐름을 가지며, 각자의 프로그램 카운터, 레지스터, 스택을 가집니다.

- 경량 프로세스: 스레드는 프로세스보다 적은 자원을 사용하며, 생성과 전환이 빠릅니다.

- 병렬 처리: 여러 스레드가 동시에 실행됨으로써 작업을 병렬로 처리할 수 있습니다.

## 스레드의 장점

- 자원 효율성: 스레드는 동일한 프로세스 내에서 자원을 공유하기 때문에 메모리와 시스템 자원의 사용이 효율적입니다.

- 빠른 컨텍스트 전환: 스레드 간의 문맥 교환은 프로세스 간의 문맥 교환보다 빠릅니다.

- 향상된 응답성: GUI 애플리케이션에서 백그라운드 작업을 스레드로 처리하여 응답성을 향상시킬 수 있습니다.

- 병렬 처리: 멀티코어 시스템에서 스레드를 이용하여 병렬 처리를 구현할 수 있습니다.

## 스레드의 단점

- 동기화 문제: 스레드가 메모리를 공유하기 때문에, 동기화 문제(예: 경쟁 상태, 데드락)가 발생할 수 있습니다.

- 디버깅 어려움: 스레드 간의 상호작용으로 인해 디버깅이 어려울 수 있습니다.

- 복잡성 증가: 멀티스레드 프로그램은 단일 스레드 프로그램보다 설계와 구현이 복잡합니다.

## 스레드의 종류

- 커널 수준 스레드 (Kernel-Level Threads): 운영 체제 커널에 의해 관리되며, 커널이 스레드 스케줄링과 관리를 담당합니다. 예: POSIX 스레드(pthread) 라이브러리.

- 사용자 수준 스레드 (User-Level Threads): 사용자 라이브러리에서 관리되며, 커널이 아닌 사용자 공간에서 스레드 스케줄링을 수행합니다. 예: Java의 그린 스레드(Green Threads).

## 스레드 생성 및 관리

스레드는 다양한 프로그래밍 언어와 라이브러리에서 지원됩니다. 예를 들어, C에서는 POSIX 스레드 라이브러리를 사용하여 스레드를 생성하고 관리할 수 있습니다. Java에서는 Thread 클래스와 Runnable 인터페이스를 사용하여 스레드를 생성하고 관리합니다.

예제: POSIX 스레드를 이용한 스레드 생성 (C)
c

```java
#include <pthread.h>
#include <stdio.h>

void* thread_function(void* arg) {
printf("Hello from thread!\n");
return NULL;
}

int main() {
pthread_t thread;
pthread_create(&thread, NULL, thread_function, NULL);
pthread_join(thread, NULL);
return 0;
}
```

예제: Java에서 스레드 생성
java

```java
public class MyThread extends Thread {
public void run() {
System.out.println("Hello from thread!");
}

    public static void main(String[] args) {
        MyThread thread = new MyThread();
        thread.start();
    }

}
```

## 스레드 동기화

스레드 간의 동기화를 위해 뮤텍스, 세마포어, 모니터 등의 동기화 도구를 사용합니다. 동기화는 데이터 일관성을 유지하고 경쟁 상태를 방지하기 위해 필요합니다.

예제: Java에서 동기화 블록 사용
java

코드 복사

```java
public class Counter {
private int count = 0;

    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }

    public static void main(String[] args) {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        try {
            t1.join();
            t2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        System.out.println("Final count: " + counter.getCount());
    }

}
```
