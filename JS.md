## 기술 부채 (2018. 6. 12.)


|  <center>KeyWords</center> |  <center>설명</center> |  <center></center> |
|:--------|:--------|:--------|
|**일급 객체** | 생성,연산,대입, 인자/반환값 역할 등을 제한 없이 할 수 있는 대상 |*4가지 필요 조건* |
|-| 무명 리터럴로 표현 가능, 변수/객체/배열에 저장 가능, 함수의 파라미터로 전달 가능, return value로 사용 가능 |JavaScript Function |
|**parameter** | 함수 내에서 변수 처럼 메모리 공간에 할당된다. 함수에 전달된 인수(argument)가 매개변수에 할당 되는 것이다.  |*argument -> parameter*   (매개변수는 인수로 초기화) |
|**argument** | 인수 |- |
|**함수 객체의 프로퍼티** | 함수도 객체이므로 프로퍼티를 소유 가능  |- |
|- | arguments, caller, length, name, prototype, [[prototype]] |*일반객체와는 달리 표준 프로퍼티를 갖음* |
|**arguments 프로퍼티** | arguments 객체를 값으로 가지며 함수 내부에서 지역 변수처럼 사용된다. (즉, 함수 외부에서는 사용 불가) |- |
|**arguments 객체** | 함수 호출 시 *전달된 인수(argument)의 정보를 담고 있는 순환 가능한 유사배열 객체* | 매개변수의 개수 > 인수의 개수, 또는 그 반대의 경우 매개변수가 undefined 되거나 남는 인수는 무시되기 때문에 runtime 시 호출된 함수의 인자 개수를 확인하고 이에 따라 동작을 달리 정의할 필요가 있을 수도 있다. 이 때 arguments 객체가 유용함  |
|**내부 함수** | <center>cell 1x2 </center> |*cell 1x3* |
|**클로져** | <center>cell 1x2 </center> |*cell 1x3* |
|**콜백 함수** | <center>cell 1x2 </center> |*cell 1x3* |
<!-- |  <center>Header1</center> |  <center>Header2</center> |  <center>Header3</center> |
|:--------|:--------:|--------:|
|**cell 1x1** | <center>cell 1x2 </center> |*cell 1x3* |
|**cell 2x1** | <center>cell 2x2 </center> |*cell 2x3* |
|**cell 3x1** | <center>cell 3x2 </center> |*cell 3x3* | -->

#### 현재 웹 애플리케이션 구현 
>SPA (Single Page Application) 방식
#### JS 사용의 목적
>DOM(HTML, CSS)를 JS로 제어 
#### 비동기 통신 방식 
```
예를 들어보자. 
클릭버튼!
클릭이 언제 발생할지 알 수 없다! 
클릭이 발생하면 수행할 행위를 정해놓는다.(이 경우에는 eventlistner가 동작하면서 클릭 발생을 모니터링)
```
##### ECMA Script 버전 ES3/5/6
##### REACT는	LIBRARY에 가까움
##### ANGULAR :	FRAMEWORK는 애플리케이션 전체를 아우름
	
#### 초기 JS의 용도 
```
ID/PW 입력 여부 확인과 같은 행위를 하기 위해서 비전문가들도 쉽게 JS를 활용 가능하도록 만들어졌다. 
일반 애플리케이션은 OS에서 동작하도록 만들었으나 (설치 과정이 수반) 웹 애플리케이션은 그런 과정을 생략할 수 있다. 
그러면 웹 애플리케이션은 어떻게 동작시킬 것인가? 웹 브라우저에서 애플리케이션을 실행/제어하자 → JS 필요
초창기에는 PLAIN JS로 코딩하기가 어려웠음 → JQUERY 등장 → 그런데 JQUERY가 SPA에는 적합하지 않았음 
(JQUERY는 HTML에 의존적이기 때문에 사용을 지양하게 되었음) → ANGULAR, REACT, Vue.js의 사용이 대두
그러나, JS는 애플리케이션용 언어가 아니기 때문에 태생적 한계가 있다!
```
#### JS는 프로토타입 기반 객체지향 언어	
>클래스 vs 프로토타입    
#### Object 프로그래밍 하는 대상들을 각각 object로 인식 
>객체는 데이터와 행위를 포함한다 - 표현식으로 객체를 바로 생성 가능

#### 프로토타입의 정의?
>To be explained
	
#### JS	HTML, CSS를 JS로 동적으로 제어

#### 웹 브라우저의 동작 원리 (brief)
```파서``` : 텍스트를 파싱해서(txt-> byte code) 메모리에 저장 (line by line)  
**스크립트의 위치**는 *head*안이 아니고 **body**를 닫기 전에 위치 한다.  
```DOM(HTML요소)```를 제어하기 위해서는 바디 태그 맨 마지막에 있어야 한다.

#### 모듈화 미 지원	
```파일을 분리할 수 없음```  
여러 JS 파일 있어도 한개 파일만 동작. ES6에서 파일을 쪼개는 기능을 지원하나 현재 브라우저에서는 미지원.  
따라서 ```webpack```을 사용하여 이를 보완하고자 한다.
#### 브라우저 동작 원리	
DOM/CSSOM/syntax Tree는 메모리에 저장된다. HTML 1.1에서는 파일을 각각 요청해서 받음 (html, css, script 각각)  
**2.0은 다중 요청**이 가능하다고 한다.
#### 값 = literal	
숫자, 문자열(한개 이상의 문자 모두), boolean, undefined, null,symbol // 이상은 ```기본 자료형```  
_(**변수에 할당될** 바이트 수가 정해져 있다)_  
메모리 확보하는 방법이 다른 한 가지 // ```객체형```_(변수에 할당될 바이트수가 유동적)_  

#### Statement의 예를 보자
>var foo = 10;  
```선언문이자 할당문```  
var foo;  
```선언만 하고 할당 하지 않았다.``` 이러한 경우 **undefined**를 기본으로 갖게 됨
symbol은 ES6에서 추가됨  
표현식 정의  
```x + y 와 같이 특정 값을 갖게 될 수 있는 형식```

#### 코드블록으로 구문 그룹화
```
중괄호로 지정한 범위 구문은 세미콜론으로 닫는다. (optional)  
필요한 구문을 그룹화하여 추후 재사용 하도록 하자.  
```
#### scope	
변수의 범위 (유효범위-코드블럭)
#### control flow	
```
JS코딩에 익숙해지면 if/for는 지양해야 한다. 이유는 코드를 읽기가 어렵기 때문. 
그래서 고차함수를 사용함 (JS는 함수형 언어)
현재는 코드의 가독성을 높이는 것에 초점을 맞춘다. 코드의 효율성보다도 중요 
그래서 변수/함수 생성시 이름 중요(역할/용도 등의 힌트를 줄 수 있어야 한다.)
```
#### Expression(표현식)	
궁극적으로 하나의 값을 만드는 것  
#### 동적 typing  
var foo 에는 모든 형태의 변수가 다 들어올 수 있다  그래서 type을 지정하기 위해서 typescript 사용  
Var foo : string; (정적 typing)
# 변수 	
위치를 기억하는 저장소  
숫자표현은 8바이트가 할당된다.
메모리 참조 : 변수가 어디에 저장되었는지 찾자   
call by value 방식  
**STACK** : 정해진 크기의 메모리 할당 (기본자료형 할당되는 공간)  
**HEAP** : 유동적 크기의 메모리 할당 (객체형 할당)

*cf.* 문자열 1개는 2byte

	
```프로그래밍을 이해하기 위한``` _KEYWORDS  
>변수, 참조, 연산자, (데이터)흐름제어, 함수, 구문의 집합, 자료의 구조화

# 변수 (다시 한 번)
	변수는 주소를 식별할 수 있다.
	변수 할당 시 데이터의 크기 Var num(동적 타이핑) : 메모리의 일정 구역 확보 → undefined(변수선언 시 초기화 : 불필요한 더미값을 클리어 한다) → 값 할당 → 재할당할 경우 주소 변경되어 남게 된 기존 값은 불필요하기 때문에 garbage collection의 대상이 됨. (아무도 참조하지 않는 값) / garbage collection이 발생하는 시기는 알 수 없음
*cf.* 메모리의 이해  
#### 타입 추론
데이터형의 인지 : 값이 할당되는 과정에서 자동으로 변수의 자료형을 결정  
```기본자료형 vs 객체형```  
기본자료형 (primitive)은 변경불가능(immutable)한 값 (generally important in programming language)  
Pass by value
1. **boolean**	
2. **null** : 값이 없음을 명시하는 것 (참조 정보 제거 → garbage collection 대상이 됨) 굳이 null 변수 선언/할당할 필요는 없음
3. **undefined** : 변수 선언만 했을 때, 존재하지 않는 프로퍼티를 참조 시 undefined
4. **number** : JS에서는 숫자는 모두 실수 (*Infinity* : 2의 53승-1을 벗어나면 무한대 // *NaN* : 숫자를 문자로 나누는 등)
5. **string** : 여타 프로그래밍 언어에서는 string은 기본자료형이 아님
	
#### 객체형  
기본자료형과 반대되는 특징들이 많다. 크기가 정해지지 않는다!  
기본자료형은 stack에, 가변적인 객체형은 heap영역에서 관리됨   
`Mutable` 하다!  
	pass by reference :  
	**추상화** : 필요한 프로퍼티만 선언해서 객체를 표현한다. (프로퍼티와 행위로 객체를 구성)  
	**상속** : 다른 객체의 속성을 상속 받고 다른 속성도 사용할 수 있음  

**전역 변수** : 애플리케이션이 종료되지 않는 이상 계속 메모리 차지 (x=1처럼 var 키워드 생략 허용)  
**지역 변수** :	함수 내에게 선언된 변수  
**동적 타이핑** : 데이터 타입을 미리 선언하지 않는다. (값이 할당될 때 변수의 타입이 추론 될 것이다.)  
**정적 타이핑** : 미리 선언한다. (int n, char str 등등)
	
## var 키워드로 선언된 변수의 문제점	 
다른 언어는 모든 코드 블럭이 유효범위(스코프), *JS는 함수 범위만 유효*  
대부분의 문제는 전역 변수로 인해 발생한다.  함수범위 제외하고는 모두 GLOBAL SCOPE이다.  

연산자 사용 시, 숫자+문자할 때는 자료형을 명시적으로 바꿔서 작업  
'==’  *사용 금지*(true를 반환할 가능성 높음, 자료형에 대한 비교는 하지 않으므로..)  
html에서 사용자 입력과 같은 데이터를 받을 때는 모두 string으로 받음 (우리가 *숫자*를 입력하더라도..)  
**삼항연산자**	활용도 높음  (ex. Condition ? ‘true’ : ‘false’;)  
	
```var INPUT_ID_MIN_LEN = 5;```	상수!  
(재할당하면 안됨. 그러나 var는 강제할 방법 없음, 길고 자세한 대문자 변수명으로 의미/용도를 명시하는 것)  
id.length	기본자료형(string)이었는데 이렇게 선언되면서 id가 객체로 취급된다  
	
```10+'10' 10+10```	OR조건으로 문자가 있으면 문자열 연결 연산자, AND조건으로 숫자가 있어야 산술 연산자
논리연산자  
var n3 = !'Cat'; // false (문자열을 암묵적으로 형변환했다 -true)
	
```단축평가```	
>var foo = 'Cat' || 'Dog' (형변환 된 것이 넘어가는게 아니다!!!)  

Truthy / falsy  

방어 코드 (미입력으로 인한 오류발생 방지)	  
	function foo (str)  
	{   str = str || '';   
	// do somethig with str   
	console.log(str.length); }  
	foo();     // 0  
	foo('hi'); // 2  

빈 객체 또한 truthy  

자료형의 인식 	
자료형의 인식을 통해서 오류 최소화, 인식이 안되면 강제로 형 변환 해야 함.  
control flow	  
>for 문 중요하지만,  
>for문 대신 고차함수를 실무에서는 더 많이 사용함  

코드 블럭 (구문들의 집합체), 그룹화해서 재사용하려고 만든다  
	
SWITCH  
case ‘yellow’ : 일단 케이스 조건 일치하면 그 이후 조건은 일치하지 않아도 모두 출력, 그래서 break 명령 사용  
If → switch Conversion?  
위에 삼항연산자도 조건문  

# 05월 31일

## 알고리즘 10번
*이중 for* 문 사용해도 해결 가능
 
  for (var i = 0; i < 5; i++){  
    for (var j = 0; j <= i; j++){}  
  }  
 i : 0, j : 0  
 i : 1, j : 0~1  
 i : 2, j : 0~2  
  += '\n' 삽입할 수 있다  

**11번**도 이중 for문 사용해보자
  
>코드의 재사용성을 높이자 : ```효율성```, ```정확성```을 높이기 위함  
	
코드의 구조화를 위해서 프레임워크를 사용하자.  
JS에서는 변수가 함수 안에서만 지역변수다. for문 안에 선언되어도 전역변수이다.  
for문을 돌릴 수 있는 다른 방법(고차함수 사용)이 있다. (차주에 다룸)  
While은 무한 loop 필요 시 유용함 (게임 등)  
do while  
**continue** 짝수면 출력 안됨 (for 조건으로 다시 돌아감)  
**evaluating** 
평가의 결과물은 true/false  

if (x % 2)  : 짝수는 실행 안됨 값이 0이고 0은 false니까!!!  

**임의의 형변환**  
      '+' 문자열 / 문자열 * 1 : 숫자로 형 변환  
      생성자 함수 : 객체를 생성  
      Number(val) : number형 생성하는 함수  
      val + "" : 문자열로 형 변환  

**동등성 비교**  

```==``` 와 ```===``` 의 차이 : ```===```는 타입까지 본다. ```==```는 가급적 true를 반환하려고 함!(강제 형변환을 해서라도 true를 반환할 수도 있다)

**삼항연산자** : elem ? (true면 할일) : (false면 할일)  

```평가값을 갖는 객체는 그것이 false를 가졌더라도 해당 객체를 평가하게 되면 항상 true다!```  
식별은 Name, 데이터 접근/제어 key  


>object / function / type checking

prototype의 정의 (**hard**)

1. 객체(Object)
**객체** : 프로퍼티 + 메소드  (기본자료형(Primitives)을 제외한 나머지 값들(**함수, 배열, 정규표현식 등**)은 모두 객체)  
객체는 데이터를 한 곳에 모으고 구조화하는데 유용하다. 그래프나 트리와 같은 자료구조 표현 용이.  
- 왼쪽(프로퍼티)이 이름 : 오른쪽이 프로퍼티의 값  
person object의 name property의 값은 lee  
프로퍼티의 값으로 함수(1급 객체)가 올 수 있다. (함수도 값이다).  
```프로퍼티의 값이 함수일 경우``` (객체의 프로퍼티이면)에 일반 함수와 구분하기 위해 **메소드**라 부른다.  
	*cf.프로토타입 기반 객체지향 언어 vs 클래스 기반 객체지향 언어*  
	자바에서는 클래스를 사전에 정의하고 필요한 시점에 new 연산자를 사용하여 인스턴스를 생성하는 방식으로 객체를 생성한다.   
	하지만 자바스크립트는 클래스라는 개념이 없고 별도의 객체 생성 방법이 존재한다.  
	*cf.syntactic sugar (클래스 기반 처럼 동작하는 자바스크립트, 기타 무엇무엇 처럼 동작하게끔 할때)*  

- 방식 3가지 (**차이점**)
	1. 객체 리터럴(**literal**? 값과 유사함/값이 될 수 있는 값을 이르는 말)  
	함수 리터럴 : 함수 자체가 값이 될 수 있음을 내포하는 말  
	클래스의 목적은 인스턴스 생성  
	객체는 클래스가 필요가 없고 표현식만으로 객체를 생성할 수 있다.  
	{} 내에 아무것도 기술하지 않으면 빈 객체  

	2. object 생성자 함수 (**엔진이 사용하는 방식**)  
	*cf.* 객체는 기본자료형이 아닌 것을 이를 때, **instance** 는 메모리에 올라간 객체의 실체를 이를 때 사용하는 용어  
	new : instance 생성 명령  
	object 생성자로 인해 빈 객체 생성된다. 그 후에 프로퍼티 생성하자~  
	동적 프로퍼티 할당 : 프로퍼티는 추후에도 언제든, 얼마든지 추가 할당 가능하다! (*클래스 기반 언어에서는 불가능한 행위*)  
	*생성자 함수가 존재하는 이유?* 객체 리터럴 방식은 syntactic sugar다! 1번 방식을 사용하면 내부적으로는 2번으로 동작한다.

	3. 생성자 함수(대문자로 시작, 사용자간의 약속, **클래스 기반언어의 클래스와 생성자 함수**의 역할이 같다)  
	*동일한 형태의 객체를 다수 만들 때 사용하자*
	this에 연결(바인딩)되어 있는 프로퍼티와 메소드는 public(외부에서 참조 가능)하다.  
	성자 함수 내에서 선언된 일반 변수는 private(외부에서 참조 불가능)하다.  

	>```1번이 가장 많이 사용됨```

## **객체 프로퍼티 접근**

**프로퍼티 이름** : 빈문자열을 포함한 문자 또는 숫자, 결국에는 이름 전체는 문자열로 간주됨.  
한 문자열 타입의 값으로 수렴될 수 있는 표현식도 가능.  
프로퍼티에 따옴표를 생략할 수 있으나 **예외** first-name처럼 연산자 있을 때  
JS의 예약어 또한 이름으로 사용하지는 말자.  

	cf. 변수명 생성 시  
	first-name : kebap case (X)  
	first_name : snake case  
	firstName : camel case  
	FirstNmae : pascal case  

마침표 표기법 (일반적)  
대괄호 표기법 [first-name] 여기에는 ''생략하면 안 된다.  
person.1에서 1은 숫자로 인식됨.  

*cf.* delete는 안 쓰는게 좋음  
왜? 다른 사람이 사용할지도 모른다..  
객체 자체는 지울 수 없음 -> 메모리에서 우리가 직접 지울 수 없기 때문에  

## **pass-by-reference** 
>(객체의 중요한 특징 -> *주소*를 넘겨 준다)  

기본자료형은 stack에 값이 있다. (pass-by-value : 값으로 전달된다-> 이 말은 **값이 복사되어 전달된다**는 의미!)  
객체는 프로그램이 돌 때(runtime일 때) 그 크기를 알 수 있다.  
기본자료형은 runtime 이전에 JS엔진이 메모리 크기가 얼마나 필요한지 알 수 있지만 (선언을 통해서 무조건 stack에 변수당 8바이트가 할당 되기 때문에.)  
*객체*는 동적으로 메모리가 조절 가능한 영역(HEAP)에 존재함 -> 프로퍼티 추가/삭제가 가능하기 때문에!  
*객체의 주소를 스택에 써둔다.*(엔진에 따라서 다를 수 있음) -> 주소는 바이트 수가 고정적.  
객체 자체에는 주소값이 저장되어 있다. (var bar = foo; foo객체의 메모리 주소가 bar 변수에 저장됨) 그래서 메모리 상에 **같은 실체**를 공유하게 됨 **varbar**와 **foo**가 같은 것을 참조한다 -> 따라서 *값의 변경은 모두에게 영향을 미칠 수 있다.*  
>pass by reference를 통해 메모리의 효율적 사용이 가능해 진다! (원론적 이유)  
  
> ## ```pass by value vs pass by reference```  
> ## ```immutable vs mutable```

### *tip.*  
	객체의 프로퍼티 값을 기본자료형 변수에 할당하고 그 객체의 프로퍼티 값을 변경하면 변수의 값은 변경되지 않는다.  
	이는 변수에 프로퍼티 값을 할당했을 때 그 참조를 할당하는 것이 아니라 immutable한 값이 메모리에 새로 생성되고 변수는 이것을 참조하기 때문이다.  
	따라서 프로퍼티의 값이 변경된다 하더라도 변수가 참조하고 있는 값은 변함이 없다.  
	어떤 객체를 새로운 객체 변수에 할당(참조값을 전달한다!)하면, 프로퍼티 값 변경은 두 객체 모두에 영향을 미친다.  
    html도 객체로 관리되는데, 이 객체들을 관리하는 것이 DOM  


## **함수**
반복적으로 수행해야 한다면 구문의 집합을 정의 구문들의 집합을 **정의**하고 필요시에 **호출**하자.   (**코드의 *재사용*** 가능)

>일반적 기능(코드의 재사용) 이외에 객체 생성, 객체의 행위 지정(메소드), 정보의 구성 및 은닉, 클로저, 모듈화 등의 기능을 수행  
함수는 구문(statement)의 집합으로 모듈화의 근간이 된다.  
**일반적인 프로그래밍 기술**이란? "*요구사항*" -> "*자료구조 + 함수*"의 집합으로 변환  

함수 : 값으로 취급될 수 있다 (일급 객체이기 때문에.)	오브젝트 나라의 시민권자인 함수 ㅋㅋ  
즉 변수나 객체, 배열 등에 저장할 수 있고 다른 함수에 전달되는 인수로도 사용할 수 있으며 함수의 반환값이 될 수도 있다.  

## **함수의 생성 방식**
- 선언식
- 표현식
- function 생성자 함수 (by JS-engine)

```함수 선언식```  
	function(키워드) square(number) {  
		return number * number;  
	}  
number는 지역변수인데 별도 선언 필요 없음 (var 필요 없음)  

```익명 함수 표현식```  
var square = function(number) {  
  return number * number;  
};  

    함수가 값으로서 기능한다.  
    함수 객체의 주소를 square 변수에 저장  

**익명 함수표현식이 일반적**  
기명 함수표현식에서는 함수명 호출은 불가능

**선언식 vs 표현식**  
무엇을 써도 큰 상관 없음
선언식은, 함수표현식의 sytactic sugar.   
(여기서는 변수명이 square로 동작) 호이스팅 때문에 차이가 발생함  
(**함수 호이스팅이냐, 변수 호이스팅이냐**)  

## **함수 호이스팅** 

변수 / 함수 호이스팅(사전적 정의 : 끌어올림)  
정확한 의미, 모든 선언문은 스코프의 최상단으로 옮겨진 것처럼 동작한다.  

- **변수 호이스팅** : *모든 선언문은 호이스팅 된다.* 프로그램 실행전에 js엔진이 코드를 전체적으로 읽어서 선언+초기화 단계를 거치고(Variable Object에 저장, 할당은 따로 발생함) 이를 통해 메모리 크기를 추산한다. 그래서 아직 선언되지 않은 변수가 undefined 상태인 것이다! 이유는 '실행 컨텍스트'에서 다룬다.  
	

	>함수선언식은 함수 호이스팅 된다 : 선두에서 호출 **가능**  
	함수 선언의 위치와는 상관없이 코드 내 어느 곳에서든지 호출이 가능
	**????함수표현식은 undefined 이기 때문에????** 선두에서 호출 **불가능** (undefined를 호출하는 꼴)  
	>함수표현식의 경우 함수 호이스팅이 아니라 **변수 호이스팅**이 발생한다. 함수선언식과는 달리 스크립트 로딩 시점에 변수 객체(VO)에 함수를 할당하지 않고 runtime에 해석되고 실행


## **first-class object(일급 객체)**  

    정의 : 생성, 대입, 연산, 인자 또는 반환값으로서의 전달 등 프로그래밍 언어의 기본적 조작을 *제한없이 사용*할 수 있는 대상
    함수가 왜 값으로 취급되는가? : 변수에 함수를 담을 수 있기 때문에 함수형 프로그래밍이 가능한 것임 -> 이것이 함수형 프로그래밍이라고 JS가 불리는 이유다.  
    함수를 리턴할 수도 있음 	
    함수를 함수의 파라미터로 전달 할 수 있다


# 6월 4일

>함수객체의 프로퍼티  

	arguments 프로퍼티 : 유사 배열 객체
	arguments 객체는 배열의 형태로 인자값 정보를 담고 있지만 실제 배열이 아닌 유사배열객체(array-like object)이다.
	유사배열객체란 length 프로퍼티를 가진 객체
	배열 메소드를 사용하는 경우 에러가 발생하게 된다. 따라서 배열 메소드를 사용하려면 Function.prototype.call, Function.prototype.apply를 사용하여야 하는 번거로움이 있다.
    length 프로퍼티 : 매개변수의 갯수
    arguments.length와는 다를 수 있다.(호출 시 인자의 갯수)

>**매개변수 (Parameter, 인자)** : 매개변수는 함수 내에서 변수처럼 메모리 공간을 확보하며 함수에 전달한 인수는 매개변수에 할당

    모든 객체는  [[prototype]] 숨겨진 프로퍼티를 갖는다. [[prototype]]은 underscore proto underscore와 같다.
	[[prototype]]은 자신의 부모역할을 하는 객체(프로토타입 객체)를 가리킨다.
	함수의 프로토타입 객체는 Function.prototype (이것도 함수)
    함수 객체는 prototype 프로퍼티를 갖는다


>cf. javascripttutorial.net
```
Foo 함수는 인자를 받아들여서 네임 프로퍼티를 객체에 생성하고 인자값으로 네임 프로퍼티의 값을 설정한다. 내부적으로는, JS 엔진이 새로운 함수 Foo와 무명의 객체를 생성한다. 
Foo함수는 prototype이라는 프로퍼티를 갖게 된다. 이 prototype은 생성된 
무명의 객체를 가리키고 있다. 그리고 무명 객체의 constructor라는 프로퍼티가 
Foo 함수를 가리키게 한다. 추가적으로, Foo.prototype 객체는 [[prototype]]을 통해서 Object.prototype 객체에 연결되어 있다. [[prototype]]은 prototype linkage이다. 
Foo함수와 new를 이용해서 새로운 a라는 instance를 생성하자. 내부적으로 JS엔진은 
a객체를 생성하고 a를 [[prototype]]프로퍼티로 Foo.prototype에 연결한다.
```

>상속을 위해서 프로토타입(부모 객체)이 존재함  
>객체지향 언어가 되기 위해서 중요한 속성은 '상속' : 부모것(프로퍼티)을 자식이 언제든 사용할 수 있다.

- 모든 객체가 소유하고 있는 숨겨진 프로퍼티 __proto__ 부모역할을 하는 객체를 가리키고 있다.  
- 함수객체만 가지는 프로퍼티 = prototype  
- 생성된 객체의 입장에서는 '__proto__' 로 prototype 객체 참조  
- 생성자함수 입장에서는 .prototype으로 prototype 객체 참조  

## **IIFE**  
- 선언과 동시에 호출 
- 한번만 호출 가능, 종료 즉시 소멸
- 초기화 처리에 사용
- 호출 -> () 사용
```
자바스크립트에서 가장 큰 문제점 중의 하나는 파일이 분리되어 있다하여도 글로벌 스코프가 하나(전역이 1개다)이며 글로벌 스코프에 선언된 변수나 함수는 코드 내의 어디서든지 접근이 가능하다는 것이다. 모듈화 미지원(JS의 가장 큰 단점)
```

```전역 변수 사용을 지양하기 위해서 IIFE를 사용하는 것!```

```내부 함수 (클로저와 연관됨?)```
```지역변수는 함수 스코프 안에서만 유효함```

## 콜백 함수
특정 이벤트가 발생했을 때 시스템에 의해 호출되는 함수를 말한다.  
비동기 처리에 사용된다.  (사용빈도 매우 높음 99.9%)  

프로토타입 객체 : 모든 객체가 갖는 **부모 역할을 하는** 객체 (부모객체와 링크되어 있다 - 상속 개념과 유사)
*cf. 프로토타입 프로퍼티*

var student = {
  name: 'Lee',
  score: 90
};

// student에는 hasOwnProperty 메소드가 없지만 아래 구문은 동작한다.
console.log(student.hasOwnProperty('name')); // true
	hasOwnProperty 메소드 : 부모역할을 하는 프로토타입 객체가 갖고 있다.
console.dir(student);
	객체 내부를 보면 __proto__를 통해 프로토타입 객체의 메소드들을 볼 수 있다

student.__proto__ === Object.prototype (**실체**와 링크되어 있다) 	//true

일반함수도 프로토타입(이라는 프로퍼티)을 갖고 있지만 무의미하다. (왜 갖고 있나, 생성자함수(new와 함께 동작)도 일반함수에 포함되는 것, 생성자함수로 쓸 때 프로토타입이 의미를 갖는다, 생성자 함수는 대문자 사용으로 명시하자)

프로토타입 체인 : 프로토타입 객체만 따라 올라갈 수 있다.
object.prototype : 프로토타입 체인의 종점 (여기에도 없으면 reference error)


객체 리터럴에 메소드가 포함되어 있다 : 

var person = {  
  name: 'Lee',  
  gender: 'male',  
  sayHello: function(){  
    console.log('Hi! my name is ' + this.name);  
  }  
};  

person 객체는 object 생성자 함수에 의해  

생성자 함수 사용 시 : 생성자함수.prototype에 동일한 기능을 하는 메소드를 포함시키면 
효율적으로 메모리를 사용가능 (프로토타입 체인에 의해서 자식 객체들이 참조해서 사용할 수 있다)  **그림 참조**

constructor 프로퍼티 는 프로토타입 객체가 갖고 있음(생성자 함수를 가리킨다)
foo.constructor 로 생성자 함수를 찾아갈 수 있다 (프로토타입 체인이 사용 됨, foo에는 constructor 프로퍼티가 없기 때문에 Person.prototype에서 찾는다)
 
Person.prototype.sayHello = function(){  
  console.log('Hi! my name is ' + this.name);  
};  
>생성자함수.prototype에 함수를 추가하자  

wrapper 함수? : 

'.' 사용하면 기본자료을 객체화화
var str = 'test';
console.log(typeof str);                 // string
console.log(str.constructor === String-생성자함수); // true
console.dir(str);         

string객체의 프로토타입 객체에 메소드 추가는 가능하나 하면 안됨

Native object : 사용환경에 영향 받지 않는 코어 영역
Host object : ECMA script spec에 없음

예 : node.JS 같은 환경에서 사용할 수 있냐 없냐

네이티브 객체 

object가 인수를 무엇으로 받는지에 따라서 어떤 객체를 만들지 결정

JS에서 에러처리 방법
	JS에는 비동기 처리방식이 많은데, 이 때 에러처리가 안된다. 

'.'가 나오면 래퍼객체가 기본자료형을 객체로 바꿔준다.

호스트 객체 (현재까지는 native객체를 배우는 중이었음)
환경에 영향을 받는 객체, 표준에 포함되지 않음

전역 객체
애플리케이션 전역에서 참조 가능한 객체
예) 브라우저 시작 시 window라는 객체가 존재하기 시작, 사용자가 만드는 변수,객체(함수도 포함) 등이 window에 포함됨


var ga = 'Global variable';  
console.log(ga);  
console.log(window.ga);  
 
전역변수는 윈도우 객체의 자식, 전역함수도 윈도우 객체의 자식  

eval() : 사용금지

메소드이름의 패턴이 있다

전역객체에 있는 메소드는 형변환 후에 결과 산출

number, matn객체는 형변환 하지 않는다. (isNaN 관련)

### parseInt()
문자열을 숫자 형으로 바꿀 때 사용	

encodeURI / decodeURI
### URI : 
fragment 내부 이동,페이지 전환 없는 요청

## BOM (스스로 학습하자)

# DOM (중요)
웹 문서를 컨트롤 한다.

메소드 학습 방법
	메소드명(keyword) 와 친숙해지자 : 어떤 메소드가 있는지 알고
	실제 적용시에 사용법을 익혀 나가자
	ex. string객체의 메소드를 이론 설명 -> 문제를 풀 떄 메소드 적용을 고민해라

6/4


# 6/5

review
>생성자 함수를 이용한 객체 생성 방식이 클래스 기반 객체지향 언어의 클래스와 같은 역할을 하는 것 (템플릿처럼 비슷한 객체 다수 만들 때)
	함수 생성
	선언식
	표현식
	function 생성자 함수 : 핵심 - 함수도 객체기 때문에 생성자 함수로 생성 가능하다. 일급객체 (값으로 활용할 수 있다.), 프로퍼티도 갖는다

## Object
Object의 분류는 정설은 없다.
네이티브 객체(Native objects or Built-in objects or Global Objects)는 ECMAScript 명세에 정의된 객체
환경과 관계없이 언제나 

>Node.JS (서버사이드 JS엔진-자바스크립트 사용 환경)
>AJAX

**wrapper 객체**: 기본자료형을 객체처럼 동작하게 한다.
그 때 각 기본자료형의 생성자함수(constructor)가 사용된다.
null, undefined는 wrapper 객체 없다!

생성자함수에 인수를 준다? : 프로퍼티의 초기화 값

문자열(유사배열객체)은 순서를 보장하기 위해서 프로퍼티를 숫자로 보이는 문자를 갖고 있고, length 프로퍼티를 갖는다. [[숨겨진 프로퍼티-PrimitiveValue]]도 갖는다.

### 중요
var x = 'Lee';  
var y = new String('Lee');  

console.log(x == y);  // true  
console.log(x === y); // false  

console.log(typeof x); // string  
console.log(typeof y); // object  

var str = 'Hello';  
console.log(str.length);  
내부적으로 String생성자함수가 hello를 인수로 받아서 객체를 생성한다.  

String 객체의 모든 메소드는 언제나 새로운 문자열을 반환한다.  
변경불가능이기 때문에 .. 값의 재할당(중복선언)

String.prototype.charAt(pos: number): string
'At' : 위치를 찾는 뉘앙스 ex) at index 0
str[i] 를 사용하자

*cf.*
static method  
prototype method  

str.concat(name); // str = str + name;   
+문자 연결자가 있다!  

String.prototype.indexOf(searchString: string, fromIndex=0): number

```String.prototype.replace(**searchValue**: string | RegExp, **replaceValue**: string): string```

```String.prototype.split(separator: string | RegExp, limit?: number): string[]```

인수가 없는 경우, 대상 문자열 전체를 단일 요소로 하는 배열을 반환-> COPY  

__String.prototype.substring(start: number, end=this.length): string__

```String.prototype.trim(): string```

>모든 메소드는 원래 값을 변경하지 않기 때문에 메소드의 결과값(return)을 별도로 받아야 한다!

## 2.1 Number EPSILON (전부 대문자는 상수)

Number.isFinite()는 전역 함수 isFinite()와 차이가 있다.
전역 함수 isFinite()는 인수를 숫자로 변환하여 검사를 수행하지만 Number.isFinite()는 인수를 변환하지 않는다.
null 형변환하면 false라서 0이된다.

cf. Number.METHOD vs str.prototype.METHOD
static : 객체 생성 필요 없다 (Number 객체에 프로퍼티로써 존재함)
prototype : 객체를 생성한 후 객체에서 접근해야 함

JS가 표현가능한 범위내에 있는 정수가 안전한 정수

```Number.prototype.toFixed(digits=0): string```
**반올림**

# date

var d = new Date('2017/08/08/20:00:00');
console.log(d); // Tue Aug 08 2017 20:00:00 GMT+0900 (KST)

## setTimeout / setInterval
전역 함수

setTimeout(printNow(call back 함수), 1000(ms))  1초마다 call back 함수 호출하라.

재귀적 호출 

# 6/7 (point : Array)

>to do : my refence book

Math
round(반올림/내림) vs ceil(올림) 
ES6 : 2**8 (pow)

## 2.8, 2.9 (max, min)
	1. max  (math는 모두 static method(대상이 필요없는 method) / 비교 : prototype method) math(객체) 관련 메소드를 모아 놓기 위해서 math라는 객체를 생성한 것.
	전달된 인수의 리스트 중 가장 큰 애 반환  
		cf. JSON의 형태
		[
			{1,2,3}
			{4,5,6}
		]

	배열 요소, 배열은 프로퍼티가 없는 객체, 요소만 있다, 객체는 순서보장 x, 배열은 순서보장(index 순서,for문으로 순회할 수 있다)

RegExp (패턴 + 플래그)
	^(carrot) : 첫문자
	$ : 끝문자
	regexr (정규표현식 생성자 함수)
	  
	  
	  cf. RegExp.prototype.test()
		test method는 인자로 대상 문자열을 받는다. RegExp도 생성자 함수로써 정규표현식을 참조하는 객체를 생성한다.


# Array

*순차적*으로 여러 값을 저장.  
객체(유사배열 객체가 있긴 함, ES5, ES6에서는 iteration?)와 배열의 비교

배열 리터럴
배열 생성자 함수 : 요소만 (값은 없는) 있는 배열 만들 때

배열은 어레이 생성자 함수가 만듦
Array.prototype 에 관련 method가 있음

=> : ES6 문법
( 매개변수의 리스트) =>(준다) 
> 고차함수의 등장
function (item, i){
	console.log(i, item);
}
=== 수업자료

forEach 가 뒤에 함수를 호출한다. 뒤에 (인수)는 콜백함수(내부함수)다.
	Counter.prototype.add = function (array) {
  // entry는 array의 배열 요소의 값
  array.forEach(function (entry) {
    this.sum += entry; // 2번째 인자 this를 전달하지 않으면 this === window
    this.count++;
  }, this);
};

Array Method
대상 배열을 변경한다, 대상 배열을 변경해서 돌려준다 (차이를 함수마다 자물쇠와 연필로 표시)

## Array.prototype.concat (빈도 높음)

## Array.prototype.pop() (연필)  
마지막 요소 pop/push   
맨 앞 요소 shift/unshift   

slice (복사본 생성)  
slice() : 배열 전체 복사  

## Array.prototype.slice === [].slice로 호출 가능  
## call(arguments) : arguments(유사배열객체)를 배열로 바꾸는 역할
## splice
>뽑아오면서 값을 없애거나 다른 것을 추가할 수 있다.

함수로 인자를 받는 메소드 (고차함수)

sort (숫자정렬)

오름차순
points.sort(function (a, b) { return a - b; });
함수선언문을 인자에 넣음 (함수자체를 매개변수에 넣어서 sort가 그것을 실행 시킨다. a-b로 오름차순임을 명시)
console.log(points); // [ 1, 2, 5, 10, 25, 40, 100 ]

fruits.reverse (오름차순으로 하고 reverse사용 해야 함)

*JSON 포맷*
>예시  
var todos = [
  { id: 4, content: 'JavaScript' },
  { id: 1, content: 'HTML' },
  { id: 2, content: 'CSS' }
];

다중 삼항연산자
 (a.id > b.id) ? 1: (a.id < b.id) ? -1 : 0;
 a의 id가 크면 1, 아니고 b가 크면 -1, 그것도 아니면 0

forEach 
외견상 함수호출문이다. Array.prototype에 갖고 있음
var total = 0;
var testArray = [1, 3, 5, 7, 9];

testArray.forEach(function (item, index, array) {
  console.log('[' + index + '] = ' + item);
  total += item;
});
대상 배열을 순회하면서 각각의 요소에 대하여 콜백함수를 실행한다.
5번 콜백함수 호출
인자 3개 : 요소값, 인덱스, 배열전체 (옵셔널)

forEach의 리턴은 없음
앞으로의 method는 순회를 포함하고 있다.


# 6/8

Scope : Function level scope (JS)
ES6에서 바뀜................


var x = 0;			//; 전역변수
{
  var x = 1;		//; 중복선언,전역변수
  console.log(x); // 1
}
console.log(x);   // 1; 전역변수니까 

let y = 0;				// ES6; let 선언 변수는 block level scope 가능
{
  let y = 1;
  console.log(y); // 1		// 지역변수 y
}
console.log(y);   // 0		// 전역에서는 지역변수 볼 수 없음

cf. 호이스팅은 자신의 scope 최상위로 간다.


var x = 'global';

function foo() {
  var x = 'local';				// 이름은 같지만 다른 공간에 할당된 x, // 문제의 원인은 전역 변수의 사용												
  console.log(x);

  function bar() {  // 내부함수	(또 다른 local, foo의 아래 레벨, 자기 지역에서 선언이 없으면 상위 레벨로 이동해서 찾는다.전역까지 탐색)
    console.log(x); // ?
  }

  bar();
}
foo();
console.log(x); // ?

var x = 10;

function foo() {
  x = 100;			// 전역변수, 참조해서 할당한다(**선언이 없다!**)는 의미, 자기 내부에서 찾고 없으니 전역에서 참조.
  console.log(x);
}
foo();
console.log(x); // ?

-----------------------------------------------------------------
var x = 10;

function foo(){
  var x = 100;								//함수 안에서 변수를 **선언했다!**
  console.log(x);							

  function bar(){   // 내부함수
    x = 1000;
    console.log(x); // ?
  }

  bar();
}
foo();
console.log(x); // ?
---------------------------------------------
var foo = function ( ) {
  var a = 3, b = 5;						//지역변수
  var bar = function ( ) {		//내부함수
    var b = 7, c = 11;				//**선언문이다!**
																											// 이 시점에서 a는 3, b는 7, c는 11
    a += b + c;
																											// 이 시점에서 a는 21, b는 7, c는 11
  };
																											// 이 시점에서 a는 3, b는 5, c는 not defined
  bar( );
																											// 이 시점에서 a는 21, b는 5
};
-------------------------------------------------------
scope를 어떻게 참조하는가? -> 실행 컨텍스트와 관련 있음
변수가 지역/전역, 함수가 지역/전역인지를 JS엔진이 알아야함 (컨텍스트를 알아야 함->이것을 관리하는 객체가 실행 컨텍스트)
------------------------------------------------------------------
## 암묵적
function foo() {
  x = 1;   // 이 지역에서 변수 x를 찾는다, 선언이 없으므로 전역에서 찾는다, 없으므로 선언해버린다. (의도치 않은 전역 변수의 선언이 발생, 전역변수의 사용 가능이 원인)
  var y = 2;
}

foo();

console.log(x); // 1
console.log(y); // ReferenceError: y is not defined
-------------------------------------------------------------------

var i = 5;

function foo() {
  var i = 10;
  bar();
}

function bar() { // 선언된 시점에서의 scope를 갖는다! 
  console.log(i);
}

foo(); // ?

변수명의 중복 : HTML에서 이 2개의 자바스크립트 파일을 로드하여 사용하면 변수 i는 중복된다.
네임 스페이스가 1개 (전역이 1개, 파일 분리가 무의미하다.)
ES6 모듈화 개념은 있으나 브라우저가 지원 안됨...............

전역변수의 무분별한 사용은 무척 위험하다. 전역변수를 반드시 사용하여야 할 이유를 찾지 못한다면 지역변수를 사용하여야 한다. 변수의 범위인 스코프는 좁을수록 좋다.

모든 소스를 IIFE로 묶으면, 전역변수를 하나도 쓰지 않게 된다.
(그러나 old, 클래스(ES6)로 대신한다.)

this의 공식 (함수 호출 패턴에 따라 this에 binding되는 객체가 달라짐)
- this는 전역객체(Window)를 가리킨다.(binding한다)
- 예외
	1. 생성자 함수 내에서의 this는 생성하는 객체를 가리킨다.
	2. method내에서 this는 method를 호출(소유)한 객체를 가리킨다.

arguments 사용
함수 내에서 지역변수처럼 사용
this가 함수안에 자동으로 생성된다.
함수 내부에서 this 참조 가능

  function square(number) {  
  console.log(arguments);  
  console.log(this); //**일반함수로써 this가 호출되어 짐 (기본적으로 this는 전역객체 - window에 binding됨)**  
  return number * number;  
  }  
  var result = square();  

전역 변수는 global scope를 갖고, 전역 객체(window)의 property이다.  
global scope에 생성된 함수는 전역객체의 property로 접근할 수 있는 method가 된다.  

기본적으로 this는 window에 binding된다. 전역함수는 물론이고 내부함수도 this는 **외부함수가 아닌**
window에 binding된다.  

apply 호출 패턴 : this에 binding된 객체를 바꾸고 싶을 때 사용하자  

cf. Window는 host 객체   
파일 분리가 의미 없다 ~   
브라우저 탭 : 탭 하나에 window객체 하나 존재, 그 window 아래에 여러 JS 파일...window가 전역이다.  

var value = 1;
var obj = {
  value: 100,
  foo: function() {
    console.log("foo's this: ",  this);  // obj
    console.log("foo's this.value: ",  this.value); // 100
    function bar() {
      console.log("bar's this: ",  this); 
      // **bar는 메소드가 아니고 내부함수**라서 window를 가리킴(문제의 발단),  
      this가 obj를 가리키길 원한다면 상위의 this로 갈아낀다. 
      console.log("bar's this.value: ", this.value); // 1
    }
    bar();
  }
};

obj.foo();

=======callback 함수의 경우도 this는 window에 binding된다.   

      var value = 1;
      var obj = {  
        value: 100,  
        foo: function() {  
          setTimeout(function() {     // 콜백함수(일반함수) 부분  
            console.log("callback's this: ",  this);        // 콜백함수 부분, *this는 window를 가리킴*  
            console.log("callback's this.value: ",  this.value);	  // 1  //콜백함수 부분  
          }, 100);
        }
      };
      obj.foo();  

-------------method 안에 있는 내부함수의 사용 시------------------------  
method 안에서 별도의 지역 변수(that)를 선언하여 객체의 this를 가리키게 한 후  
(아래 경우는 obj) method의 내부함수에서는 그 지역변수를 필요에 따라 사용한다.    
(obj와 binding되어 있는 this를 참조 대피 시킨 that)  

    var value = 1;
    var obj = {
      value: 100,
      foo: function() {
        var that = this;  // Workaround : this === obj	//참조 대피(할당)  
        console.log("foo's this: ",  this);  // obj
        console.log("foo's this.value: ",  this.value); // 100
          function bar() {
            console.log("bar's this: ",  this); // window 
            console.log("bar's this.value: ", this.value); // 1

            console.log("bar's that: ",  that); // obj    --->  that변수가 bar에는 없으니 상위로 올라가서 참조
            console.log("bar's that.value: ", that.value); // 100
            }
          bar();
      }
    };

    obj.foo();
---
method 호출 패턴, 함수 호출 패턴 모두 내부함수의 this는 window에 binding 된다.  
이를 해결하기 위해서 call, apply 존재 (this binding을 명시적으로 할 수 있기 때문.)
---

    var obj1 = {          
      name: 'Lee',	     
      sayName: function() {
        console.log(this.name);     //자신을 소유한, 호출한 객체에 binding  
      }
    }
    var obj2 = {
      name: 'Kim'
    }

    obj2.sayName = obj1.sayName;		//객체 obj2에 obj1의 method를 할당한다. 그래서 둘이 같다면, this는 누구를 가리키나?
    obj1.sayName();   //sayName 안에 있는 this는 자신을 호출/소유한 객체에 binding 되어 있으므로 obj1.name
    obj2.sayName();   //sayName 안에 있는 this는 자신을 호출/소유한 객체에 binding 되어 있으므로 obj2.name

>프로토타입 객체에도 메소드 생성이 가능하다. 그래서 프로토타입 객체의 메소드 안에서도 this는 동일하게 메소드를 소유/호출한 객체에 binding된다.  (프로토타입 객체에 binding된다.)

---------------------------------
    function Person(name) {
      this.name = name;    // 생성하게 될 객체를 가리킴. name이 그 객체의 프로퍼티가 된다.
    }

    Person.prototype.getName = function() {
      return this.name;
    }

    var me = new Person('Lee');
    console.log(me.getName());

    Person.prototype.names = 'Kim';
    console.log(Person.prototype.getName());   // Person.prototype의 메소드니까 this.names에서 this는 Person.prototype에 binding됨

---  
생성자 호출 패턴(Constructor Invocation Pattern)
---
**new 연산자와 함께 생성자 함수를 호출하지 않으면** 생성자 함수로 동작하지 않는다.  

    var you = Person('Kim');    // 일반함수로 동작하였다.
    console.log(you); // undefined

    function Person (name){
    /* 1. 빈 객체 me 생성한다. 
    Person의 this가 me와 binding된다.*/
    this.NAME = name; 
    /*  생성된 빈 객체에 this를 사용하여
    프로퍼티/메소드를 동적으로 할당 가능*/
    }

new 연산자 : 후에 오는 함수에 특수한 행위를 한다. (**그러고보니 그동안의 생성자 함수에는 return이 없었다?!**)  
첫 라인에서 빈 객체 생성 후 this가 빈 객체를 가리키도록 바인딩 한다.  
메소드/프로퍼티 등이 객체에 추가  
new가 맨 마지막에 this를 return 한다.  
반환문이 없는 경우, this에 바인딩된 새로운 객체를 return,  
반환문이 this가 아닌 다른 객체를 반환하는 경우, *그 생성자 함수는 생성자 함수로서의 역할을 수행하지 못한다.*  
그래서 생성자 함수에는 **명시적인 return**을 사용하지 않는 것.  

객체 리터럴 방식과 생성자 함수 방식의 차이  
(누가 만드느냐에 따른 차이 - 프로토타입 객체[[prototype]]에 그 차이가 있다.)
---

**객체 리터럴 방식**으로 객체를 생성하면, 생성된 객체의 프로토타입 객체는 **Object.prototype**이고,  
**생성자 함수**로 객체를 생성하면, **생성자함수.prototype**이다.  

    생성자 함수 호출 시 new 연산자를 사용하지 않으면? 생성자 함수로 동작하지 않는다고 언급했음.  
    이유는? 생성자 함수가 아닌 일반함수로 인식되기 때문에 그 함수 내의 this는 전역객체(window)에 binding 된다.  
    그러면 window에 프로퍼티를 추가하는 형태가 된다. 또한 (암묵적으로) 객체를 생성 후 반환하지 않게 된다.  
    new 연산자 없이 생성자 함수가 호출될 수 있기 때문에, Scope-Safe Constructor라는 패턴을 사용하자.
    (대부분의 라이브러리에서 사용되는 방식)

    function  A(arg)  {
    if  (!(this instanceof arguments.callee)){
     return new arguments.callee(arg);
    }
      //new arguments.callee(arg);
      this.value = arg ? arg : 0;
    }

    var a = A(10);
    console.log(a);

    > new 연산자 없이 호출해도 A 생성자 함수가 this 바인딩된 a에 value 프로퍼티를 추가 하였음.


자신의 함수명을 참조하고 싶을 때 callee (arguments 객체의 프로퍼티로서 함수 내부에서 현재 실행 중인 함수를 참조할 때 사용)
instanceof Person (Person으로 만들어진 객체냐?)

    -LAME EXAMPLE-
    function  A(num){

      var callee = arguments.callee;
      console.log(callee);
    }

    A(10);    // [Function: A] 해당 함수를 누가 호출했는가

  
APPLY 호출 패턴
--

THIS는 함수 호출 패턴에 따라 어디에 BINDING 될 지 결정된다.  (JS엔진에 의한 암묵적 binding)
그런데 APPLY를 이용해서 어디에 binding할지 명시적으로 정할 수 있다.
> APPLY method를 호출하는 것은 **함수**이고 APPLY method는 this를 특정 객체에 바인딩만 할 뿐이지 본질적인 기능은 함수 호출이다!

cf. **Apply는 ES6에서 안 쓰인다.**

    var Person = function (name){
      this.name = name;
    }

    var foo = {};
    Person.apply(foo, ['lee']);     //Person을 호출하는데 this(생성될 객체)를 foo로 대신해서 써라.(갈아낀다)  
    console.log(foo);

APPLY method의 두번째 인자는 매개변수를 **배열**로 합쳐 놓은 것  
foo에 name 프로퍼티를 추가하고 매개변수에 전달할 배열로 값을 채운다. (배열이 풀어져서 들어간다)  
cf. 처음 것만 받고 나머지는 무시 (apply method의 argument 배열이 함수의 argument 갯수보다 많을 경우)  

APPLY method는 유사배열 객체에(arguments 객체와 같은) 배열 객체의 method를 사용하기 위함. 유사배열 객체에서는 배열 객체의 method를 사용할 수 없는데, apply method를 이용하면 가능하다.  
유사배열 -> 배열 (변환이유 : 배열처럼 많은 메소드를 가진 객체가 없으므로 메소드를 사용하기 위해서 바꾼다)

    function convertArgsToArray() {
      console.log(arguments);		// 인수들의 리스트를 담고 있는 argu.(유사배열)			

            // arguments 객체를 배열로 변환	
            // slice: 배열의 특정 부분에 대한 복사본을 생성한다.(인수 없을 때)
      var arr = Array.prototype.slice.apply(arguments);   
            //Array.prototype.slice를 호출하라 그런데 this는 arguments 객체로 binding 하라. (원래 이 method는 자신을 소유/호출한 객체에 binding 된다)
            // arguments.slice	(argu.를 배열로 바꿔서 리턴하라, 유사배열객체만 가능함)		
            // [].slice ; 메소드 내부에서 this는 자신을 호출한 객체를 가리킨다. 따라서 [] -> this
            // var arr = [].slice.apply(arguments);
            // 결국은 arguments(배열이 아니다)를 배열처럼 넘겨서 slice 배열 메소드를 사용하기 위함이다. 
               유사배열객체로 slice 메소드를 사용할 수 없음

      console.log(arr);  
      return arr;  
    }  

    convertArgsToArray(1, 2, 3);  


## call / apply와의 차이점

    Person.apply(foo, [1, 2, 3]);   //apply method에서는 배열로 넘긴 것을, 
    Person.call(foo, 1, 2, 3);      //각각의 인자로 넘긴다.

cf. *인수의 리스트*의 의미 
예)foo(1,2,3);  // *1,2,3* 이 인수의 리스트

forEach


