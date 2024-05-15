# 소스 코드와 명령어

- 고급언어 : 개발자가 읽고 쓰기 쉬운 언어 (c, java 등)
- 저급언어 : 컴퓨터가 직접 이해 가능한 언어

## 저급언어의 종류 2가지

- 기계어 : 비트로만 이루어진 언어 (0, 1)
- 어셈블리어 : 기계어와 1:1 대응하는 언어 (add, sub 등)

## 고급언어에 대하여

- 컴파일 언어 : 컴파일러를 통해 고급언어의 소스코드를 -> 저급 언어의 목적 코드로 변환시켜 사용
- 인터프리터 언어 : 인터프리터를 통해 고급언어의 소스코드를 -> 저급 언어의 목적 코드로 변환시켜 사용 (한 줄씩 실행)

만약 컴파일 언어를 사용하는 개발자라면, 컴파일러에 대해 깊게 공부해보는 것도 좋다.

## 컴파일러와 인터프리터

- 컴파일러 : 컴파일러를 통해 고급언어의 소스코드를 -> 저급 언어의 목적 코드로 변환시켜 사용
- 인터프리터 : 인터프리터를 통해 고급언어의 소스코드를 -> 저급 언어의 목적 코드로 변환시켜 사용

# 명령어의 구조

> 명령어는 연산 코드와 오퍼랜드로 나누어집니다.

- 연산 코드 : 어떤 연산을 수행할 것인지를 나타내는 코드
- 오퍼랜드 : 연산에 필요한 자료를 나타내는 코드

## 연산코드의 유형 4가지

- 데이터 전송 : 데이터를 전송하는 명령어 (mov, push, pop 등)
- 산술/논리 연산 : 산술/논리 연산을 수행하는 명령어 (add, sub, mul, div 등)
- 제어 흐름 변경 : 프로그램의 실행 흐름을 제어하는 명령어 (jmp, jz, jnz 등)
- 입출력 제어 : 입출력 장치를 제어하는 명령어 (in, out 등)

## 주소 지정 방식

- 직접 주소 지정 방식 : 연산 코드와 오퍼랜드의 주소를 직접적으로 지정하는 방식
- 간접 주소 지정 방식 : 연산 코드와 오퍼랜드의 주소를 간접적으로 지정하는 방식