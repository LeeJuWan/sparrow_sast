Sparrow_sast 진단도구 산출물
=========================

# 1. 대시보드 (DashBoard)
![image](https://user-images.githubusercontent.com/49786050/65334381-3f7ee380-dbfd-11e9-925f-477d8a23bba0.png)

위 사진의 대시보드는 현재 자신의 서비스(어플리케이션) 분석 현황을 한 눈에 볼 수 있도록 나타낸다.
대시보드에서는 원하는 분석 파일로 접근이 용이하다. 
또한, 좌측 상단의 액션 버튼을 통하여 프로젝트 추가를 할 수 있다.

# 2. 체커 그룹 추가

<div>
<img width="350" src="https://user-images.githubusercontent.com/49786050/65334691-e9f70680-dbfd-11e9-96e6-7c702adb7086.png">
<img width="350" src="https://user-images.githubusercontent.com/49786050/65334797-1dd22c00-dbfe-11e9-8237-ebdbff64d6d2.png">                                                                                               
</div>

프로젝트를 추가 하기전에 체커 그룹을 추가해준다. 

### 체커그룹이란?
소스코드 분석에 앞서 소스코드 위험도(매우위험, 위험, 높음, 보통, 낮음)를 체크할 수 있다.
더불어 레퍼런스 ( 행자부,금감원,CERT 등)를 추가하여 **취약점 가이드라인에 맞는 위험도를 매핑하여**
취약점을 분석 할 수 있도록 하는 기능이다.

### 체커그룹 추가 방법
1. 체커그룹명 입력 (추후 새 프로젝트 추가 시 사용될 이름)

2. 위험도 선택 (매우 위험, 위험, 높음은 빼놓지 않고 추가해주었다)

3. 레퍼런스 선택
(자신이 분석하고자 하는 서비스의 특징에 따라 추가해준다, 예를 들어 안드로이드 분석이면 행자부 안드로이드 취약점 선택
 웹 어플리케이션이면 행자부 취약점, 금감원 취약점 선택)

![image](https://user-images.githubusercontent.com/49786050/65335212-f6c82a00-dbfe-11e9-85fa-dd86f1099293.png)

위의 사진 처럼 체커 그룹 활성화 tab을 이동하여 수동으로 직접 취약점 체커를 활성화/비활성화 할 수 있다.

# 3. 새 프로젝트 추가

<div>
<img width="350" src="https://user-images.githubusercontent.com/49786050/65335429-61796580-dbff-11e9-84a7-ff4aa08c2c06.png"> 
<img width="350" src="https://user-images.githubusercontent.com/49786050/65335475-75bd6280-dbff-11e9-89ed-b37cb11a8513.png"> 
</div>

1. 대시보드에서 언급한 액션 버튼을 누르게되면, 위의 그림처럼 새 프로젝트 추가를 할 수 있다.
이어서 새 프로젝트 추가 창에 대한 내용은 위의 사진과 같다.

### 새 프로젝트 추가 방법
1. 프로젝트 키를 입력한다. (자신이 사용하고자하는 키를 직접 타이핑 하여 입력)

2. 프로젝트 명을 입력한다. (자신이 사용하고자하는 명을 직접 타이핑 하여 입력)

3. 상위 프로젝트 선택. (나는 ROOT로 두고 진행하였다)

4. 체커 그룹 선택. (위의 체커 그룹 추가 방법에서 입력한 체커 그룹명을 선택 한다)

5. 저장

다음과 같은 절차를 진행 하면 분석할 프로젝트가 추가 진행된다.

# 4. 분석 셋팅

<div>
<img width="350" src="https://user-images.githubusercontent.com/49786050/65336163-d4371080-dc00-11e9-92c3-6213f3dc915b.png"> 
<img width="350" src="https://user-images.githubusercontent.com/49786050/65336215-ea44d100-dc00-11e9-9c09-331b66b5a5bb.png"> 
</div>

다음은 소스코드 분석을 위한 소스코드 분석 셋팅 절차이다.

### 분석 셋팅 방법
1. 분석할 분석 파일을 zip형태로 묶어 드래그 앤 드롭

2. 분석에 사용할 언어를 선택한다.
(개발에 사용한 언어는 서비스마다 틀리기 때문에 선택은 개인마다 틀릴 수 있다.
나는 안드로이드 분석과 웹 분석을 할 때 사용한 언어가 JAVA,JSP,HTML,JAVAScript 이기 때문에 4개를 셋팅해주었고,
서버 연동도 하였기 때문에 SQL/XML을 해주었다. 또 XSL은 잘은 모르지만, XML과 관련있을것 같아 선택하였다)

3. 프로젝트를 추가한다. (위의 새 프로젝트 추가에서 셋팅 한 프로젝트를 선택한다)

# 5. 프로젝트 요약 (분석결과)
![image](https://user-images.githubusercontent.com/49786050/65336706-d0f05480-dc01-11e9-9c4f-847a613045e6.png)

위의 그림의 하단에 최근 분석을 통해 분석한 코드 결과를 볼 수있다.
진행률, 총이슈, 위험도를 확인 할 수 있으며 선택 시 바로 해당 프로젝트의 분석 결과 창으로 이동할 수 있다.

위의 절차대로 진행하면 아래와 같은 소스코드 분석 결과를 얻을 수 있으며 이제부턴 **오탐/정탐**을 판별하여
분석을 진행해야 한다.

![image](https://user-images.githubusercontent.com/49786050/65336954-3a706300-dc02-11e9-8e4d-99d08d4385d9.png)


소스코드 분석
=============

# 6. 로그인 인증 실패에 대한 횟수 제한 부재

![image](https://user-images.githubusercontent.com/49786050/65337059-6c81c500-dc02-11e9-8dfe-a68bf89056e7.png)
**19번째 라인**에서 로그인에 대한 입력값이 들어오며, 그 결과가 아래의 if문 루틴을 통해서 진행 된다.
그러나 로그인 인증에대한 제한을 두지 않아 공격자는 무작위 대입공격, 사전 대입 공격을 할 수 있는 취약점이다.

#### 대응방안은 횟수 제한을 걸어둔다.

# 7. 시스템 민감정보 외부 노출

![image](https://user-images.githubusercontent.com/49786050/65337311-df8b3b80-dc02-11e9-9b19-610589746c8a.png)
**152번째 라인**에서 e.printStackTrace(); 를 사용하였다.
 e.printStackTrace() 자체가 무조건 취약점이라고 할 수는 없다.
 
 일례로 미디어와 관련된 소스코드가 루틴을 돌고 있는 중 에러가 발생하여 외부에 에러정보가 노출이 되어도
 의미 없는 노출일 경우가 높기 때문이다.
 
 그러나 SQL과 관련된 루틴 진행중 에러정보가  e.printStackTrace()의해 노출 된다면 공격자는 데이터베이스 공격을 위한
 공격 정보를 얻을 수 있기 때문에 코드의 역할을 확인하여 취약점 유무를 확인한다.
 
#### 대응 방안은 Log , System.err.print로 예외처리를 한다.

# 8. 오류 상황 대응 부재

![image](https://user-images.githubusercontent.com/49786050/65337735-b7e8a300-dc03-11e9-92e3-64f4579686d6.png)
**179번째 라인**에서 오류가 발생 시 오류에 대한 대응 부재이다.

해당 취약점은 Catch문이 비어 있어 사용자는 Catch문에 접근 했을 시 어떤 상황이 발생하는지 전혀 알 수 없으며
공격자는 비어있는 오류 상황을 이용하여 자신의 의도대로 프로그램을 조작 할 수 있는 상황이 발생 할 수있다. 더불어
대응 부재 시 소스코드가 통으로 노출될 수도 있다.

##### 대응방안은 대응부재를 없애며 필요한 조치를 취해야 한다. 하다 못해 오류 추적코드라도 달면 좋을 것 같다.

# 9. 하드코드 된 비밀번호

![image](https://user-images.githubusercontent.com/49786050/65338076-6856a700-dc04-11e9-8cca-780773e41e6d.png)
**19번째 라인**은 하드코드된 비밀번호 취약점이다.
위 그림의 소스는 DB를 연결하는 소스코드인데 그림과 같이 DB Password가 통으로 하드 코딩되어 있다.
이럴 경우 소스코드가 유출된다면 공격자는 너무 쉽게 비밀번호를 가져가며 데이터베이스에 ROOT 권한으로 접근 할 수 있다.

#### 대응방안은 DB Password를 외부 파일에서 받아온다. 이때 DB password는 암호화 상태를 유지하며 커넥션 진행시 
#### 복호화 하여 사용한다. 암/복호화에 필요하는 키 관리는 다른 공간에서 관리 할 수 있도록 한다.


이외에도 ~~널포인터 취약점, 비밀번호 암호화(일방향 해시) 부재, 정수형 오버플로우 취약점~~ 등있다.

널포인터는 if문, 삼항 연산자( ? : )를 이용하여 null인지 판단

비밀번호 암호화는 일방향 해시 함수로 암호화 진행 , 나는 Bcrypt를 이용하여 암호화 하였다. Salt 관리가 필요 없다.
보통은 Salt 마저 DB에서 관리 해준다.

정수형 오버플로우는 널포인터와 같은 방법으로 정수값의 표현 범위가 넘어 가지 않도록 해준다.



#### 취약점 분석을 하며 부족한 부분은 행자부 47개 취약점 가이드라인을 참고한다.
<https://www.kisa.or.kr/public/laws/laws3_View.jsp?cPage=6&mode=view&p_No=259&b_No=259&d_No=88&ST=T&SV=>

#### 이외에도 C,JAVA,ANDROID-JAVA 다양하게 있다.
<https://www.kisa.or.kr/public/laws/laws3.jsp>

