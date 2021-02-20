### **소개**

파이프라인을 구현하는 프로젝트입니다. 단일 파이프라인으로 하나의 명령어씩만 수행 가능합니다.

각 명령어는 이진수로 표현됩니다. 이를 Register, Control, Memory, ALU를 거쳐 해석되며, 데이터가 저장됩니다.


### 사용 언어

- C++

### 구조

- Input의 처음 6 bit op 코드를 통해 lw, sw 또는 계산 명령어인지 구분합니다.
- 이후 Input에서 RS, RT, RD 데이터를 10진수로 바꿉니다.
- 각 명령어에 맞게 ALU나 Mem을 Control에 따라 호출합니다.
- 명령어에 대한 결과를 출력합니다.
![image](https://user-images.githubusercontent.com/63103070/108590534-623f9980-73a7-11eb-81f5-209ba26bf811.png)


### 명령어

- ALU에서는 add, sub, sll, srl, lw, sw, or, and, nor 명령어를 수행할 수 있습니다.
- 기존에 정해져 있는 값들은 그대로 사용했으며, 그 이외의 것들은 임의로 남은 이진수로 할당했습니다.

![image](https://user-images.githubusercontent.com/63103070/108590543-71264c00-73a7-11eb-9043-0792e6bf8818.png)


### Test Data Path

- 각 명령어에서 필요한 값들을 이진수로 표현하고, 필요하지 않은 값들은 자릿수에 맞춰 0으로 표시합니다.
- 총 20개의 테스트 케이스를 만들었습니다.
![image](https://user-images.githubusercontent.com/63103070/108590563-88fdd000-73a7-11eb-9ee3-601d12335773.png)

