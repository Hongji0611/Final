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

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3088656-db5d-42ea-8442-954f1c1bab08/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3088656-db5d-42ea-8442-954f1c1bab08/Untitled.png)

### 명령어

- ALU에서는 add, sub, sll, srl, lw, sw, or, and, nor 명령어를 수행할 수 있습니다.
- 기존에 정해져 있는 값들은 그대로 사용했으며, 그 이외의 것들은 임의로 남은 이진수로 할당했습니다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/579e7bd1-b940-43c9-aeff-33be758d73f2/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/579e7bd1-b940-43c9-aeff-33be758d73f2/Untitled.png)

### Test Data Path

- 각 명령어에서 필요한 값들을 이진수로 표현하고, 필요하지 않은 값들은 자릿수에 맞춰 0으로 표시합니다.
- 총 20개의 테스트 케이스를 만들었습니다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c2f52c2-e6ff-445d-b1b9-6d77730c94c6/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c2f52c2-e6ff-445d-b1b9-6d77730c94c6/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c8c6a4b1-58cb-423c-b389-78143845fbec/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c8c6a4b1-58cb-423c-b389-78143845fbec/Untitled.png)
