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
|**내부 함수** | 함수 내부의 함수 |내부함수에서의 this는 window에 binding된다. |
|**클로져** |||
|**콜백 함수** |||
|**IIFE** |스크립트 파일 간에 같은 이름의 변수, 함수가 있을 경우 문제 발생 가능 |```전역 변수 사용을 지양하기 위해서 IIFE를 사용하는 것!``` |
|**call method** |||
|**caller & callee** |||
|**apply method** |||


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

## **IIFE**  (즉시호출함수표현식 - Immediately Invoke Function Expression)
- 선언과 동시에 호출 : 선언 -> 호출 -> (()) 
- 한번만 호출 가능, 종료 즉시 소멸
- 초기화 처리에 사용
```
자바스크립트에서 가장 큰 문제점 중의 하나는 파일이 분리되어 있다하여도 글로벌 스코프가 하나(전역이 1개다)이며 글로벌 스코프에 선언된 변수나 함수는 코드 내의 어디서든지 접근이 가능하다는 것이다. 모듈화 미지원(JS의 가장 큰 단점)
```
- 스크립트 파일 간에 같은 이름의 변수, 함수가 있을 경우 문제 발생 가능 -> 
 ```전역 변수 사용을 지양하기 위해서 IIFE를 사용하는 것!```

## 내부 함수 

함수 내부에 정의된 함수.  
내부함수는 부모함수의 변수에 접근 가능, but ```NOT vice versa```  
```또한 부모함수의 외부에서는 내부함수 호출 불가능```

*cf.* ```지역변수는 함수 스코프 안에서만 유효함```

## 콜백 함수 (클로저)
특정 이벤트가 발생했을 때 시스템에 의해 호출되는 함수를 말한다.  
```명시적인 호출을 통해서 사용하는 것이 아님!```  
비동기 처리에 사용된다.  (사용빈도 매우 높음 99.9%)  

JS의 함수는 일급객체이므로 변수처럼 사용 가능하다. **콜백 함수는 매개변수를 통해 전달되고** 이는 함수 내부에서 특정 시점에 실행된다.
  
- 비동기식 처리 모델 : 처리가 종료하면 호출될 함수(콜백함수)를 미리 매개변수에 전달하고 처리가 종료하면 호출하는 것
```
  cf. from MDN

콜백함수는 비동기식 작업이 끝난 후에 코드 실행을 계속하기 위해서 자주 사용된다. 이를 비동기식 콜백함수라고 한다.
예를 들어, 지도 예제를 보면 현재 위치 표시를 위해서 Google Maps API and Geolocation API 가 사용된다.
GPS 기능을 통한 장치의 좌표를 알아내는 것은 비동기식이기 때문에 (좌표가 언제 return될지 정확히 알 수 없다), Geolocation.getCurrentPosition() method가 인자값으로 익명의 콜백 함수를 전달 받는다. 이 콜백 함수는 인자값으로 리턴된 좌표 정보를 전달 받으며 좌표 정보를 return 받을 때에만 동작한다.
 
```
> 콜백 함수는 콜백 큐에서 이벤트가 발생하면 호출된다. 콜백 함수는 클로저 이므로 콜백 큐에 단독으로 존재하다가 호출되어도 콜백함수를 전달 받은 함수의 변수에 접근 가능하다.

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

## 네이티브 객체 
```
ECMAscript spec에 정의된 객체, 애플리케이션 전역의 공통 기능을 제공.
따라서 애플리케이션 사용환경에 비 의존적.
Object, String, Number, Function, Array, RegExp, Date와 같은 객체 생성에 관계 있는 함수객체와 메소드로 구성
객체가 인수를 무엇으로 받는지에 따라서 어떤 객체를 만들지 결정
```
1. Object  
Object 생성자함수는 객체를 생성.
인수값이 null, undefined이면 빈 객체를 생성, 그 외에 String, Number, Boolean 형 인수값을 받으면 강제 형변환하여 객체를 생성함. 따라서 prototype객체는 Object.prototype이 아니고 객체 생성자 함수.prototype 객체이다.
>그래서 객체리터럴 방식을 사용하는 것이 일반적
2. Function  
자바스크립트의 모든 함수는 Function 객체이다.  
3. Boolean
Boolean 객체는 기본자료형 boolean을 위한 wrapper객체이다. Boolean 생성자 함수로 Boolean 객체를 생성할 수 있다.

JS에서 에러처리 방법
	JS에는 비동기 처리방식이 많은데, 이 때 에러처리가 안된다. 

4. 기본자료형과 Wrapper Object  
각 네이티브 객체는 각자의 프로퍼티와 메소드를 가진다. 정적 프로퍼티, 메소드는 해당 인스턴스를 생성하지 않아도 사용할 수 있고 prototype의 메소드는 해당 prototype을 상속받은 인스턴스가 있어야만 사용할 수 있다.
그런데 기본자료형 값에 대해서도 네이티브 객체의 메소드를 사용할 수 있다. 
메소드 호출 시 기본자료형 값이 연관된 wrapper 객체로 일시 변환되기 때문. 메소드 호출 종료 시 원래 기본자료형으로 바뀜.  
('.'가 나오면 래퍼객체가 기본자료형을 객체로 바꿔준다.)
**Prototype: 6.기본자료형의 확장 참조**

5. 전역 객체(Global Object)  
모든 객체의 유일한 최상위 객체.  
예) 브라우저 시작 시 window라는 객체가 존재하기 시작, 사용자가 만드는 변수,객체(함수도 포함) 등이 window에 포함됨  
전역변수는 윈도우 객체의 자식(프로퍼티), 전역함수도 윈도우 객체의 자식(메소드)  
전역객체에 있는 메소드는 형변환 후에 결과 산출  
number, matn객체는 형변환 하지 않는다. (isNaN 관련)
6. 호스트 객체  
환경에 영향을 받는 객체, 표준에 포함되지 않음
  

### eval() : 사용금지 (보안상 취약함)
메소드이름의 패턴이 있다

### parseInt()
문자열을 숫자 형으로 바꿀 때 사용	

encodeURI / decodeURI
### URI : 
fragment 내부 이동,페이지 전환 없는 요청

## BOM 
브라우저 객체 모델은 브라우저 탭 또는 브라우저 창의 모델을 생성한다. window객체가 현재브라우저 또는 창을 표현하는 최상위 객체이다.  
이 최상위 객체의 자식 객체들이 다른 기능을 표현하고 이 객체들은 Standard Built in Objects가 구성된 후에 구성된다.  

Window 밑에 document, history, location, navigator, screen 등이 있다.  
*cf.* MDN Web APIs : Window 참조

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

JS의 기본 Scope는 Function level이다. 그 외에는 모두 전역 scope를 갖는다. 이로 인한 문제를 해결하기 위해 ES6에서는 let/const 변수를 사용하여 block level scope를 갖게 할 수 있다.  
함수 레벨 스코프 외에는 모두 전역 변수/함수로 선언되어야 하기 때문에 이름 충돌, 중복 할당 등의 문제가 발생할 수 있다.  

var x = 0;  
{  
  var x = 1;  
  // 중복선언, 함수에서 선언된 것이 아니니까 여전히 전역변수  
  console.log(x); // 1  
}  
console.log(x);   // 1, 전역변수니까  

let y = 0;				// ES6; let 선언 변수는 block level scope 가능  
{  
  let y = 1;  
  console.log(y); // 1		// 지역변수 y  
}  
console.log(y);   // 0		// 전역에서는 지역변수를 참조할 수 없음.  

*cf. 호이스팅은 자신의 scope 최상위로 코드가 옮겨간 것처럼 동작하는 것(변수/함수 호이스팅)*  


var x = 'global';

function foo() {  
  var x = 'local';  
  // 이름은 같지만 다른 공간(함수 내부에서는 지역 변수)에 할당된 x  
  // 문제의 원인은 전역 변수의 사용  
  console.log(x);  

  function bar() {  
    // 내부함수	(또 다른 local, foo의 아래 scope, 자신의 scope에서 변수 x의 선언이 없으면 상위 레벨로 이동해서 찾는다. 이런 식으로 전역까지 탐색)  
    console.log(x);  
    // 그래서 local이 출력  
  }  

bar();  
}  
foo();  
console.log(x); //  global  

---------------------------
var x = 10;

function foo() {
  x = 100;  
  // 재할당 : 전역변수를 참조해서 할당한다(**선언이 없으므로!**). 자기 내부에서 찾고 없으니 전역에서 참조.  
  console.log(x);  
  // 100
  }  
foo();  
console.log(x);  

-----------------------------------------------------------------
var x = 10;

function foo(){
  var x = 100;  
  //함수 안에서 변수를 **선언했다!**  
  console.log(x);  
  // 100

  function bar(){  
    // 내부함수  
    x = 1000;  
    console.log(x);  
    // X = 1000  
  }  
  
  bar();  
}
foo();  
console.log(x);  
// 여기서 참조하는 x는 전역 변수

---------------------------------------------
var foo = function ( ) {  
  var a = 3, b = 5;						//지역변수  
  var bar = function ( ) {		//내부함수  
    var b = 7, c = 11;				//**선언문 - 새로운 지역변수 b 선언/할당**  
    																								// 이 시점에서 a는 3, b는 7,c는 11  
   a += b + c;  
		
    																									// 이 시점에서 a는 21, b는 7, c는 11  
  };  
		
    																									// 이 시점에서 a는 3, b는 5, c는 not defined  
  bar( );  

                                          						// 이 시점에서 a는 21, b는 5  
};  

-------------------------------------------------------
scope를 어떻게 참조하는가? -> Scope Chain에 의해서 참조 가능. 이것은 [[scope]]프로퍼티로 참조 가능.  
변수가 지역/전역, 함수가 지역/전역인지를 JS엔진이 알아야함 (컨텍스트를 알아야 함 -> 이것을 관리하는 객체가 실행 컨텍스트)

------------------------------------------------------------------
## 암묵적

function foo() {  
  x = 1;  
  // 이 지역에서 변수 x를 찾는다, 선언이 없으므로 전역에서 찾는다, 없으므로 선언해버린다. (의도치 않은 전역 변수의 선언이 발생, 전역변수의 사용 가능이 문제의 원인이다.)  
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

function bar() {        // 선언된 시점에서의 scope를 갖는다!  
  console.log(i);  
}  

foo();  

**<i></i>**
**<i>변수명의 중복</i>** : HTML에서 이 2개의 자바스크립트 파일을 로드하여 사용하면 변수 i는 중복된다.
네임 스페이스가 1개 (파일 분리가 무의미하다. 분리해도 모두 window 객체에 바인딩 되기 때문이다.)  
ES6 모듈화 개념은 있으나 브라우저가 지원 안 함, 그래서 **<i>webpack</i>** 사용.  

전역변수의 무분별한 사용은 무척 위험하다. 전역변수를 반드시 사용하여야 할 이유를 찾지 못한다면 지역변수를 사용하여야 한다. 변수의 범위인 스코프는 좁을수록 좋다.  

**<i>모든 코드를 IIFE로 묶으면, 전역변수를 하나도 쓰지 않게 된다.</i>**  
(그러나 old한 방법이라 한다. **<i>클래스(ES6에서 도입)</i>** 로 대신한다.)  

## **<i>this의 공식</i>**  

 함수 호출 패턴에 따라 this에 binding되는 객체가 달라짐
- this는 기본적으로 전역객체(window)를 가리킨다.(에 binding 된다)
- 예외
	1. **생성자 함수** 내에서의 this는 생성하는 객체를 가리킨다.
	2. **method**내에서 this는 method를 호출(소유)한 객체를 가리킨다.

>arguments 사용  
함수 내에서 지역변수처럼 사용  
this가 함수안에 자동으로 생성된다.  
함수 내부에서 this 참조 가능  

  function square(number) {  
  console.log(arguments);  
  console.log(this);  
  //**일반함수에서 this가 호출되어 짐 (기본적으로 this는 전역객체 - window에 binding됨)**  
  return number * number;  
  }  
  var result = square();  

전역 변수는 global scope를 갖고, 전역 객체(window)의 property이다.  
global scope에 생성된 함수는 전역객체의 property로 접근할 수 있는 method가 된다.  

기본적으로 this는 window에 binding된다. 전역함수는 물론이고 내부함수도 this는 **외부함수가 아닌
window**에 binding된다.  

***apply 호출 패턴*** : *this에 binding된 객체를 바꾸고 싶을 때 사용하자!*  

cf. Window는 host 객체 (Node.JS에서는 global)  
파일 분리가 의미 없다, 브라우저 탭 하나에 window 객체가 개별적으로 존재, 그 window 아래에 여러 JS 파일이 바인딩 된다.  
```
var value = 1;  
var obj = {  
  value : 100,  
  foo: function() {  
    console.log("foo's this: ",  this);    // obj  
    console.log("foo's this.value: ",  this.value);   // 100  
    function bar() {  
      console.log("bar's this: ",  this);  
      // bar는 메소드가 아니고 내부함수라서 window를 가리킴(문제의 발단),  
        this가 obj를 가리키길 원한다면 상위의 this로 갈아낀다.??
      console.log("bar's this.value: ", this.value); // 1  
    }  
    bar();  
  }  
};  

obj.foo();  
```
-----------
***callback 함수의 경우도 this는 window에 binding된다.***  

      var value = 1;
      var obj = {  
        value: 100,  
        foo: function() {  
          setTimeout(function() {  

            console.log("callback's this: ",  this);  
                // 콜백함수 부분, *this는 window를 가리킴*  

            console.log("callback's this.value: ",  this.value);	  // 1 콜백함수 부분  
          }, 100);
        }
      };
      obj.foo();  

***method 안에 있는 내부함수(는 window에 binding된다)의 사용 시***  
method 안에서 별도의 지역 변수(that)를 선언하여 객체의 this를 가리키게 한 후 (아래 경우는 obj) method의 내부함수에서는 그 지역변수를 필요에 따라 사용한다.  
>*obj와 binding되어 있는 this를 참조 대피 시킨 that*  

    var value = 1;
    var obj = {
      value: 100,
      foo: function() {
        var that = this;  // Workaround : this === obj  
              //참조 대피(할당)  
        console.log("foo's this: ",  this);  
              // obj
        console.log("foo's this.value: ",  this.value); 
              // 100
          function bar() {
            console.log("bar's this: ",  this); // window 
            console.log("bar's this.value: ", this.value);      // 1
            console.log("bar's that: ",  that); // obj    --->  that변수가 bar에는 없으니 상위로 올라가서 참조
            console.log("bar's that.value: ", that.value); // 100
            }
          bar();
      }
    };

    obj.foo();
---

***method 호출 패턴, 함수 호출 패턴 모두 내부함수의 this는 window에 binding 된다.***  
>이를 해결하기 위해서 call, apply 존재, **this binding**을 명시적으로 할 수 있다.

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

    obj2.sayName = obj1.sayName;		
    //객체 obj2에 obj1의 method를 할당한다. 그래서 둘이 같다면, this는 누구를 가리키나?
    obj1.sayName();   
    //sayName 안에 있는 this는 자신을 호출/소유한 객체에 binding 되어 있으므로 obj1.name
    obj2.sayName();   
    //sayName 안에 있는 this는 자신을 호출/소유한 객체에 binding 되어 있으므로 obj2.name

>프로토타입 객체에도 메소드 생성이 가능하다. 그래서 **프로토타입 객체의 메소드 안에서도** this는  메소드를 소유/호출한 객체에 binding된다. *프로토타입 객체에 binding된다.*

---------------------------------
    function Person(name) {
      this.name = name;    
          // 생성하게 될 객체를 가리킴. name이 그 객체의 프로퍼티가 된다.
    }

    Person.prototype.getName = function() {
      return this.name;
    }

    var me = new Person('Lee');
    console.log(me.getName());

    Person.prototype.names = 'Kim';
    console.log(Person.prototype.getName());  
          // Person.prototype의 메소드니까 this.names에서 this는 Person.prototype에 binding됨

---  

## 생성자 호출 패턴(Constructor Invocation Pattern)

**new 연산자와 함께 생성자 함수를 호출하지 않으면** 생성자 함수로 동작하지 않는다.  
그런데, new 연산자가 없으면 일반함수처럼 동작하기 때문에 그 함수의 this는 window객체에 binding된다.  
그리고 window에 동적으로 프로퍼티가 생성된다. 생성자 함수는 별도의 return이 없어도 새로운 객체를 최종적으로 반환하지만,  
일반함수처럼 동작할 때는 undefined가 리턴된다.

    var you = Person('Kim');    // 일반함수로 동작하였다.
    console.log(you); // undefined

    
    생성자 함수의 동작 순서

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


# Execution Context

## 1. 실행 컨텍스트의 개념  (정확한 내용은 ECMA Script spec. 참조)
  실행가능한 (3가지)  
  *cf. lexical scoping*  

  전역 코드 vs 함수 코드
> 각자가 갖는 정보들이 다르다. (함수에는 매개변수 arguments 객체가 있는 것처럼..)

 **중요**   
var x = 'xxx';  

function foo () {  
  var y = 'yyy';  

  function bar () {  
    var z = 'zzz';  
    console.log(x + y + z);  
  }  
  bar();  
}  

foo();  

JS의 실행 원리  
Global EC 생성 (실행가능한 코드의 정보를 담고 있는 객체 - 여기에 window 포함)
foo호출되면 foo에 대한 실행컨텍스트를 스택에 생성  
bar호출문을 만나면 bar에 대한 실행컨텍스트를 생성  
*실행 컨텍스트 콜스택에 담겨 있는 것들은 실행 중인 애들*  


## 2. 실행 컨텍스트의 3가지 객체 
1. VO (environment)
2. SC (lexical)
3. this.value (this binding)  
(정식 프로퍼티 명이 따로 있음)  
**각 실행컨텍스트에 포함되어 있는 내용들**  

코드 실행 전에 GO가 생성된다.  

1. 
함수선언문도 표현식처럼 바뀐다. 그래서 변수객체에 포함됨. 선언문과 표현식은 호이스팅에서 차이가 발생.  
(함수표현식도 변수객체에 포함. var 자체이다.)  
전역 코드는 VO가 전역객체(window), 함수는 VO가 AO(함수와 1:1대응)이다.
함수 -> AO : GO와의 차이 (매개변수/인자를 갖는다)


2. 
현재 코드의 현재 스코프를 알아야함.
GEC는 GO만. 유사배열 index 0 만 있음.
foo함수



**중요**   
var x = 'xxx';  

function foo () {  
  var y = 'yyy';  

  function bar () {  
    var z = 'zzz';  
    console.log(x + y + z);  
  }  
  bar();  
}  

foo();  


window는 그 전에 이미 생성되어 있다.(JS파일이 나누어져 있어도 모두 window에서 작동한다)  
특정 프로그램을 실행할 때 GO setting : (전역 실행 컨텍스트 생성) 전역변수, 전역함수 정보를 GO에 담는다.  
그 후에 코드가 라인단위로 실행 됨.  

cf. 실행컨텍스트 스택 = 콜 스택  

1. 스코프체인의 생성과 초기화 
2. 변수 객체화 실행 (VO를 생성)
- vo에 변수명 등록(선언단계, 메모리 사용 없음)
- 초기화 undeifned
-
3. this 결정


# Closure
### **정의** : 내부함수가 참조하는 외부함수의 지역변수가 *외부함수에 의해 내부함수가 반환된* 이후에도 life cycle이 유지되는 것  

>사용 조건 :  
내부함수가 외부함수보다 더 오래 유지 되어야 할 때  
내부함수가 외부함수의 지역변수를 참조할 때(*복사본이 아닌 실제 변수에 접근한다*)  
외부함수가 내부함수를 리턴할 때  
**필요한 경우** 전역변수를 사용 피하기 위해서 closure를 사용할 수 있으나 외부함수의 Activation Object를 내부함수가 참조하게 되므로 남발하게 되면 메모리 효율이 떨어질 수 있음

1. 전역코드  
  1.1 전역 객체, 전역 실행 컨텍스트가 생성됨  
  1.2 전역 실행 컨텍스트에서 다음 순서로 처리됨  
    1.2.1 SC 생성 및 초기화  
    1.2.2 변수 객체화  
    1.2.3 this 값 결정  

    1.2.1 SC 생성 및 초기화
      > 전역 실행 컨텍스트와 전역 객체를 연결 하는 index를 갖는 리스트(스코프 체인) 생성
    1.2.2 변수 객체화 (프로퍼티와 값을 setting)
      > 변수 객체(Variable Object)에 변수/함수 선언, 매개변수/argument 를 추가하여 객체화.  
       
    Setting 순서  (함수 코드의 매개변수/argument -> 함수 선언 -> 변수 선언)

      a. 매개변수가 프로퍼티로 argument는 값으로 설정됨  
      b. 함수명을 프로퍼티로, 생성된 함수 객체를 값으로 (함수 호이스팅의 이유)  
        VO는 GO (전역 코드일 때) : 이 때 함수객체는 [[scopes]] 프로퍼티를 갖게 된다.  

      >[[scopes]]는 함수객체가 실행되는 환경. 따라서 현재 실행컨텍스트의 스코프체인이 참조하고 있는 객체를 값으로 설정.  
      내부함수는 자신의 스코프를 포함한 외부함수 실행환경, 전역 객체를 가리키고 있으므로 외부함수의 실행 컨텍스트가 소멸하여도 **[[scopes]]를 통해서 AO는 소멸되지 않고 참조 가능**. 이것이 **클로저**

      c. 변수명을 프로퍼티로, undefined를 값으로 (실제 값은 할당단계에서.)  

    1.2.3 this 값 결정은 함수 호출 패턴에 따라서 달라짐 (일반함수, 생성자함수, method)

**과제 (독해 해보기)**
``` 
<!DOCTYPE html>
<html>
<body>
  <p>새로고침으로 다시 실행해 보세요</p>
  <script>
    var fade = function (node) { 
      // 자유변수 : step 변수에 저장된 함수에서 변수 level을 참조하고 있음
      var level = 1; // ②
      var step = function () {
        var hex = level.toString(16); // ④  toString() method는 인자값의 형태(여기서는 16진수)로 대상을 바꿔준다. // hex: '1' ~ 'f'
        
        node.style.backgroundColor = '#ff' + hex; // ⑤

        if (level < 15) { // ⑥
          level += 1;
          setTimeout(step, 100); // ⑦ 100ms 이후에 step 함수 호출
        }
      };
      // setTimeout 호출 이후 fade 함수는 종료한다. 하지만 100ms 후 함수 step이 호출된다. 즉 외부 함수 fade보다 내부 함수 step이 더 오래 유지된다.
      setTimeout(step, 100); // ③
    };

    fade(document.body); // ①
  </script>
</body>
</html>
```
# DOM
```
memo
객체화하는 이유? 컴퓨터(브라우저)에게 무의미한 텍스트를 브라우저가 읽을 수 있도록(읽어서 저장할 수 있도록) 만들기 위함. 
HTML 코딩(프로그래밍)은 구조화, 배치, 중첩관계(부자관계)가 중요함
DOCUMENT객체 밑에 DOM이 생성됨
```
>향후 공부 방법 : 현재까지는 개념이해, 이제부터는 DOM API(method)를 어떻게 사용하느냐가 중요함.

## 브라우저 동작 원리

ex) www.ㅌㅌㅌ.com/(resource) default로 index.html을 반환한다.


ex) 파싱 중 link 태그를 만나면 파싱 멈추고 해당 링크의 파일을 요청, (html / css / script 파일) 파일을 받으면 해당 파일을 파싱, 파싱 후 객체 모델을 만든다. (DOM / CSSOM / Syntax tree) 
**DOM CSSOM**는 같이 동작해서 렌더링이 되는 대상이고 Syntax tree는 Dom + Cssom 을 조작

*cf. HTML 2.0은 각 파일(Html, Css, Script)를 한꺼번에 받는다.*

>**DOM 조작 능력**  
document element를 통해서 찾아 들어가고, 원하는 node에 접근해서 API(method)로 조작할 수 있어야 한다.

*attribute 노드는 element 노드와 형제 관계*

**document.getElementById(id) (document 객체의 method)**  
id가 인자값  
객체를 반환하는  
**DOM 객체는 무겁다.**  
DOM 생성과정에서 attribute -> property로 변환된다. (attribute 명칭이 달라질 수 있음)  

'on'으로 시작하는 프로퍼티가 event를 의미.  

queryselector 클래스, 아이디, 등 CSS 선택자로 사용되는 애들을 인자값으로 받을 수 있음

getelementsByclassName('class 이름) : 여러개의 값을 반환한다. (어떻게? 유사배열로 반환)

live 객체? (htmlCollection) 클래스 이름으로 결과값을 가져온다. 클래스 이름 기준으로 DOM객체 가지고 옴 (non-live와의 차이)


**firstChild, lastChild**
숨겨진 첫번째 자식이 있어서 예상결과와 다름. 우리가 보는 요소 앞뒤에 text(스페이스, 탭, 엔터 등을 텍스트 노드로 인식하기 때문에)가 삽입되어 있음.  

attributes  : 변하지 않는, 초기값을 갖고 있는 객체, 
property : 동적으로 변하는 최신값(사용자 입력값) 갖고 있음

4.3 HTML 컨텐츠 조작

스크립트(태그)를 추가하는 순간 내용이 즉시 실행된다.  

property : textContent

**property : innerHTML**  

createElement 부자관계는 어디에도 성립되지 않음(그냥 개별 요소 생성)

style : 


Asychronous processing model 

동시성 구현을 위함


# event

이벤트 핸들러 (콜백 함수) : 

대부분의 이벤트가 비동기식으로 동작함

tick 이벤트 (setTimeout)

>**이벤트 루프와 브라우저의 환경** (그림)


form 태그의 중요성  

attribute : action, method 

DOM Level 2 Event Listener  
대상요소 : 돔 쿼리를 해야 한다.  
이벤트타입 : 클릭, 블러, 등등  
**캡처링 & 버블링**  

# 이벤트의 흐름 
이벤트는 어디서 먼저 발생하는가
하위에서 발생해도 윈도우 부터 이벤트가 내려온다. 이벤트 타겟에서 다시 위로 올라감

>(해당 개념의 존재이유? ) 
부모요소에 이벤트 리스너를 걸어서 bubbling을 잡는다. 


event는 html 요소가 발생 시키고 브라우저가 그것을 캐치한다.

addeventlistener 앞에 오는 DOM 객체가 (elem)이 발생 주체가 될 수도 있고, 캐치할 수도 있다.  

새 페이지를 다시 렌더링 하면 화면 **깜빡** : 이를 방지하기 위해서는 html자체를 요청하지 않고 일부분만 요청.  

전통적으로 서버 사이드 렌더링이었으나 (클라이언트는 요청만 해서 브라우저를 새로 고침했었다 -> 화면 깜빡임) -> AJAX와의 연관성 (**중요**)

### AJAX (+ HTML5)
>v8의 등장으로 AJAX 사용이 가속화 됨 (구글 맵스, gmail 등의 웹 애플리케이션이 등장)  
v8은 고속으로 동작.

>1 source multi use (OS에 비 의존적)  
유지보수 간편 (실시간 업데이트/패치 가능)  
상대적으로 표준화 수월 (브라우저 별 호환성 이슈는 아직 존재)  

브라우저의 고속화가 수반되면 PC 하드웨어에 대한 의존성을 현저히 낮출 수 있음  
(PC는 브라우저만 오픈, 다른 애플리케이션 설치 불가 등등)  

웹 어셈블러 (웹용 공통 언어)  

HTML5 : **플러그인 제거**하고 표준을 제공한다.  

서버에서 **데이터를 가져와서** 렌더링  

이벤트 전파 (그림 참조 DOM level 3 events)

## 이벤트 객체
브라우저(이벤트 관련 API가 만든다)가 생성, 이벤트 관련 정보를 담는다.  

## event property
### event target
### current target 
this와 동치일 수 있다 (이벤트 핸들러에서)  

### 이벤트 타입 

## 이벤트 위임 (버블링과 캡쳐링과 연관)

버블링 : 자식 요소가 조상 요소의 이벤트를 캐치할 때
캡쳐링 : vice versa
여기에 정확히 누가 발생 시켰는지 알아야 하므로 e.target 필요

>e.target.nodename 참조 이유? 어떤 요소를 특정하여 처리할 때 참조해야 한다.





# AJAX
HTML에 name attribute가 JSON의 키 값으로 된다.  

### XMLHttpRequest (생성자 함수)  

 get (read), path 데이터  
 html을 어떻게 http body에 담는가.  
 
 >get은 URL뒤에 string(query string)으로 보내고,  
 post(데이터 생성)는 request body에 key & value로 담아서 보낸다.
 post : request body에 담는 내용이 payload (send 메시지에 인자를 주는 것)  
 ID/PW 같은 내용은 POST로 보낸다.

response는 이벤트로 
응답 완료 시 이벤트 핸들러에서 잡는다.

비동기 방식이기 때문에 request의 response가 오기도 전에 코드가 실행되기 때문에 반드시 비동기함수에서는 응답값 사용은 함수 안에서 사용해야함.
그런데 이렇게 하면 indent가 계속 들어갈 수 있기 때문에 (이로 인해 call back hell 발생) 사용 지양  
비동기 프로그래밍 문제? ES6 promise를 조금 보완, await/async/generator -> RXJX

snippet : HTML의 조각


/ 와 ~(system root)의 차이

Load JSONP (타 서버의 데이터를 가져오는 방식)
동일출처 원칙 위배를 우회 방법 중 하나는 proxy 

# REST API 

get = retrive  
post (생성한다는 의미) : 서버에게 생성을 요청한다.  
put : row 전체를 바꾼다.  
patch(fetch) : row 중 일부를 바꾼다.  

1. URI는 정보의 자원을 표현해야 한다.  
  URI > URL (포함하는 개념)
  PATH + query parameter + Fragment 중요

GET /books/1
id가 1일인 데이터를 가져온다. 1이 없으면 전부다.

백엔드와 사용할 REST API들의 이름 정의.
백엔드가 서버를 구축하는 것을 기다릴 수 없으니, 자체적으로 테스트용을 만든다. 이것을 MOCK 서버라 한다.
MOCK 서버는 NODE.js, Express로 만들 수 있고 json-server로도 가능

http://localhost:5000/todos/3 id 3만 데이터를 요청한다.
= get 방식 요청

>postman 사용법
POST 방식     (POST만 데이터 생성시 201로 응답)
  BODY raw JSON
  서버에 보낼 메시지를 작성한다.

send 메시지의 인자로 json을 주는데 stringify해서 준다.

put,patch,delete 에는 어떤 row (record)를 고칠지 알려줘야 함 (ID로 알려준다)


# ES6

>3 -> 5  
JSON의 추가, strict 모드 추가

>6의 등장 다양한 application 등장으로 더 많은 기능들이 필요했다

cf. ES8이 최신

```
ES spec을 기반으로 브라우저 벤더 별 엔진을 만든다.  
spec의 모든 내용이 구현되지는 않을 수도 있다. (ECMA script browser support 참고)
```

## let / const
>변수 타입 2개 추가  
**중요 : var / let / const 각 차이와 문제점**

```
var 변수는 함수레벨 스코프만 갖는다.  
var 키워드를 생략 가능함. 이유는 스코프체이닝으로 함수내에서 찾다가 전역에서도 찾다가 최종적으로 할당해버림..
변수 호이스팅 : 선언문 이전에 참조 가능

전역 변수의 사용으로 참조처가 많아지면 수정/변경에 대한 추적이 어려울 수 있음
```

1. let

**블록 레벨 스코프 지원**
중복 선언 금지함 (syntax error 발생)  
**JS에서는 모든 선언문을 호이스팅 한다.**  
따라서 let 선언문도 호이스팅이 **발생**하는데 보여지기에는 발생하지 않는 것 처럼 동작. (refernce error 발생시킴)   

변수 초기화/선언 단계가 각각 진행됨.  
선언 : 런타임 이전에 선언문을 훑고 (VO에 등록만) undefined 하지는 않는다. 

> let과 closure

reminder :3가지 조건, 내부함수의 life cycle > 외부함수(실행컨텍스트가 더 오래 남아있다)


var funcs = [];

// 함수의 배열을 생성하는 for 루프의 i는 전역 변수다.

for (var i = 0; i < 3; i++) {
  (function (index) {             // index는 자유변수다.
    funcs.push(function () { 
      console.log(index); });
  }(i));
}

// 배열에서 함수를 꺼내어 호출한다
for (var j = 0; j < 3; j++) {
  funcs[j]();
}

외부 스코프의 지역변수를 내부 스코프에서 참조한다.  

for (let i = 0; i < 3; i++) -> i도 매개변수처럼 이해하자.  
(따라서 i는 지역변수이다.)  
// 함수의 배열을 생성하는 for 루프의 i는 for 루프의 코드 블록에서만 유효한 지역 변수이면서 자유 변수이다.  

for (let i = 0; i < 3; i++) {
  funcs.push(function () { console.log(i); });
}

// 배열에서 함수를 꺼내어 호출한다  

for (var j = 0; j < 3; j++) {  
  console.dir(funcs[j]);  
  funcs[j]();  
}  

전역 객체와 let  

## const (상수를 갖기 위해서 사용 - 사전적 정의)
실제로는 const 객체는 값/내용 변경 가능  (변경 추적이 어려워질 수 있음)

cf. **5.8 객체와 변경불가성**

var / let / const (사용 비교)

재할당은 상태 변경을 인식하기에 가장 좋은 타이밍.

## template

 백틱(backtick) 문자 `를 사용한다.

# ARROW function

사용가능한 경우를 알 수 있어야 함.. (this에 대한 이해가 선행되어야 함)
매개변수를 함수 body로 넣는다 (이미지화)

x => x * x  

## 일반함수의 this

>화살표 함수에서의 this는 **상위 컨텍스트의 this**  

두번째 인자로 this를 주기  

생성자함수에 화살표함수 사용 불가
// 화살표 함수는 prototype 프로퍼티가 없다 -> 생성자함수로 사용할 수 없다. (화살표함수는 주로 callback 용도)
원래 모든 함수는 prototype 프로퍼티를 갖는다. 생성자함수로 작동하면 프로토타입객체를 이를 통해 프로토타입객체를 참조

4.4 addEventListener 함수의 콜백 함수(이벤트 핸들러)

사용이 원천불가한 것은 아님 (내부에서 this를 사용하지 않는다면 화살표 함수 사용 가능)

## Rest 파라미터



arguments 객체 (인수들의 유사배열)
함수 내부에서 지역변수처럼 사용할 수 있는 arguments 객체를 참조하도록 한다.

Array.prototype.slice.call(arguments) ; arguments 객체를 this로 넘겨서 (호출하는 객체의 this로)
arguments는 화살표 함수 내에 없음

 **apply** 메소드의 2번째 인자는 배열.  
 이것은 개별 인자로 push 메소드에 전달된다.  
 (apply로 arr1의 this를 넘겼으므로 arr2를 풀어서 넣어준다. )  
Array.prototype.push.apply(arr1, arr2);


## 6/28 러버덕
#### 1. let / const

#### 2. this (with arrow function)  
  **기본** : this는 **함수 호출 패턴**에 따라 결정됨.  
  (3 가지 + event handler에서의 this + arrow function 의 this)  
  ```
  this는 화살표 함수에서는 무조건 상위 컨텍스트를 참조한다. 콜 스택에서 아래에 먼저 쌓인 실행컨텍스트의 SC로 연결된 AO를 참조한다. 화살표함수는 고차함수의 콜백으로 많이 사용된다.
  ```

**cf.** 화살표함수에서는 프로토타입 프로퍼티(생성자함수로 사용 못하도록) & 아규먼츠 객체를 제거 (Rest 파라미터 사용을 권장하기 위함)

# CLASS (생성자 함수의 대용) 
  >Angular / React가 class 기반

ES6에서 객체 리터럴로 생성한 OBJ의 프로퍼티 기능이 확장되었다.  

생성자함수 외부에서 
생성자함수 안에 static method

Person prototype 을 내가 원하는 다른 객체(foo)로 갈아 끼운다면,  
  Person.prototype = foo;  
이 경우의 문제는 default 프로퍼티 중 constructor 값(Person 생성자함수의 참조값)을 잃게 된다. 

cf. rest 파라미터 앞의 ...과 스프레드 연산자(...)는 다른 것이다!
1. 펼쳐진 것들을 배열로 모은다.
2. 반대(배열로 되어 있는 것을 spread 시킨다-개별 값들을 배열화 할 수도 있음 [x, ...y] = [1, 2, 3];
)

# Destructuring (활용빈도가 높으니 문법에 대한 익숙함이 필요)

>point - 무엇을, 왜 destructuring 하는가?  
배열 또는 객체를, 구조화된 데이터 중에 필요한 일부만을 사용하기 위해서 destructuring 한다.  
(배열/객체 간 차이 : 순서의 보장 여부, 값의 이름이 존재-프로퍼티 명, 메소드의 보유 여부)

*cf. this는 자신이 가지고 있는 데이터를 참조하기 위한 방식*

객체 디스트럭처링

변수명을 프로퍼티명으로 갖는 객체를 생성한다.

# CLASS

**syntactic sugar** : CLASS를 사용하더라도 내부적으로는 프로토타입 기반 프로그래밍 언어로 동작한다.  

기존 JS도 생성자함수가 클래스의 역할을 할 수 있다. CLASS 개념의 도입 이유는 타 언어 사용자를 위함?!  

    this._name = name; (숨김 프로퍼티)


class Person {
  constructor(name) {   constructor -> 생성자
    this._name = name;
  }

const me = new Person('Lee'); new 없으면 에러(typeError) 발생
new Person에서 Person은 클래스의 이름이 아니고 constructor 이다.

**인스턴스(객체)의 생성** : 클래스의 존재 이유. 객체 생성 방법이 하나 더 추가되는 것 ㅎㅎ

클래스 내부에 컨스트럭터는 반드시 1개만 존재해야 함 (**생략해도 제대로 동작**)   
클래스가 만들 객체의 프로퍼티 -> 클래스 프로퍼티 (컨스트럭터 내부에 위치해야 함)
constructor가 클래스 프로퍼티를 초기화하기 위해 사용됨

constructor 내부의 클래스 프로퍼티는 클래스의 인스턴스를 가리키는 this에 바인딩 된다. (**일반적 생성자 함수 바인딩처럼**) 
>클래스가 생성할 인스턴스의 프로퍼티가 된다는 것



호이스팅  

**getter/setter**  
  **특별한 메소드?** 클래스 프로퍼티에 접근할 때 클래스 프로퍼티의 값을 조작해야 할 때 사용.

  클래스 프로퍼티를 활용하여 동작하는 메소드
  >예) console.log(foo.firstElem); // 프로퍼티 참조하는 것처럼 메소드를 호출한다.

  >getter : 파라미터가 없으며 반드시 return값이 있어야 함.  
    get firstElem() 
  setter는 클래스 프로퍼티에 값을 할당할 때마다 클래스 프로퍼티의 값을 조작할 때 사용.  

  정적 메소드 : this를 사용할 수 없다. (참조하지 않는다.) 클래스 프로퍼티를 참조하지 않는다.  
  정적메소드 내부에서의 this는 클래스의 인스턴스가 아닌 클래스 자신을 가리킨다. 메소드 내부에서 this를 사용한다는 것은 클래스의 인스턴스 생성을 전제로 하는 것.

  클래스 이름으로 호출하기 때문에 인스턴스를 생성하지 않아도 사용할 수 있다.  
  이처럼 this를 사용할 필요가 없는 메소드는, 정적메소드로 만들면 된다. (이러한 정적 메소드는 전역에서 사용하는 utility 함수를 만들 때 사용한다.)

  예. Foo.staticMethod();
  예. Math.max  
  >프로토타입 메소드에서는 this가 필요하다.  

  예. [].concat() : [] -> this
  get firstElem() {  
    
    return this._arr.length ? this._arr[0] : null;  
  }  
  }  
위의 this는 메소드를 호출하는 객체를 참조하게 됨.   

// 프로퍼티 firstElem에 접근하면 getter가 호출된다.  

>setter : 클래스 프로퍼티에 인수를 세팅(할당)한다.

**innerHTML과의 연관성?**  

# this / prototype / class 연관성 정리 필요

# 상속 (Inheritance)

    super(radius);  -2가지 형태-
    반드시 호출되어야 하는 함수. 
    1.(부모 클래스의 컨스트럭터를 호출하는 역할을 한다? 부모의 인스턴스가 존재해야 자식 생성할 수 있다. 그래서 부모의 컨스트럭터를 호출해서 부모 instance를 생성하고 자식의 클래스 프로퍼티를 추가한다.)  
    따라서 자식 클래스의 컨스트럭터에서 super를 호출하지 않으면 referenceError가 발생한다.

    2. 부모의 메소드를 사용하기 위해서도 사용됨 (부모의 this에 대한 참조)  

    사용할 때에는 프로토타입 체이닝 개념으로 부모 클래스의 메소드에 접근 가능함.
    중복되는 메소드일 경우 자식 클래스 것을 쓰게 된다. (overriding)

  ### 복습으로 코드 쳐 봐야함


# PROMISE
비동기로 동작 : DOM (이벤트 발생 주체), setTimeout/interval, AJAX

promise는 AJAX와 관련된 것

### 콜백 헬
에러 처리가 불가능하다.

동기식 처리 : 블록킹(대기) 현상 발생, 브라우저는 single thread이기 때문에 블록킹 처리할 방법 없음

비동기식 처리 : non blocking 방식. 작업 처리의 순서를 추적하기가 어려울 수 있음  
단점은 콜백 헬, 에러 처리    
이벤트 루프에 의한 콜 스택 진입

try catch 
에러처리 불가 이유 : 콜백함수는 이벤트 큐로 이벤트 루프가 콜 스택으로, 에러는 발생원천으로 noti가 간다. 

모든 데이터의 입출력을 모두 같은 형태로 처리

비동기 함수 처리했을 떄 호출하는 함수
처리 실패 시 호출하는 함수
콜백 패턴

promise가 상태 정보를 알려준다 (fulfilled 성공/ rejected 실패 여부)

new promise 를 리턴한다. (원래는 불가능했음).

사용방법은 리턴된 프라미스 객체 

then 에 성공 콜백
catch 에 실패 콜백

콜백 헬 해결 방법 : 

>이미지화(샘플화)를 통해서 기억/이해하라.

# 7/2
## MODULE
ES6에서 MODULE 개념을 도입하였다.  
**<i>요약!</i>** 하자면, JS 파일 단위로 구현된 기능(함수)를 다른 파일에서 import하여 사용한다. 이것은 window 객체에 모든 변수/함수가 바인딩될 때 발생하는 문제로 MODULE화를 구현할 수 없었기 때문에 ES6에서 module 개념을 도입한 것.  
파일 단위로 구분(기능별로 분리해서 만든다)되는 개별 코드 조각, 재사용이 수월하여 개발 효율 높이고 유지보수도 수월하게 한다.  
모듈 내부는 공개/비공개용으로 나뉨 : public / private 프로퍼티가 있다. (정보 은닉 가능)  

JS는 전역(WINDOW)이 1개이므로 대규모 애플리케이션 개발에서 한계를 드러낸다. 외부 스크립트 파일을 참조 가능하나 하나의 window에 바인딩 되어 전역변수가 충돌하는 등의 문제 발생 가능. 이로써는 모듈화 기능 구현 불가능.  

IIFE 사용을 통해서 해결 가능, IIFE로 만들어진 함수를 사용하려면 객체 **생성자 함수**를 리턴하도록 만든다.  
예 - JQUERY : 최초에 전역 객체 밑에 자신들이 사용할 객체를 생성한다.  

**WHY** 개별적 요소(module)로 사용하는가? 재사용을 위해서.  
개발 시 정형화된 기능들(로그인, 로깅, 사용자 관리 등)을 효율적으로 구현.    
angular에서는 CBD (Component Based Development) 개념을 도입하여 구현.  
Component = module?

>NOTE. **<i>CBD</i>**  
웹 어플리케이션 개발의 3가지 언어는 다르지만 큰 **목표**는 갖기 때문에 **관심사의 분리를 적용하지 말고 CBD개념으로** 구현하자.  

모듈간에 서로가 서로를 포함하거나 사용할 수 있도록 import/export를 한다. - 공개할 내용만 public으로 export한다.  
**<i>Export</i>** 키워드가 븥으면 모듈로 동작 시킨다. 모듈화는 별도 모듈만의 스코프를 갖게 한다.  

**<i>Module & Module Consumer</i>** : export / import 주체를 의미함.  
>변수, 함수 클래스를 하나의 객체로 구성하여 공개(export)할 수도 있음  
export { pi, square, Person };  
변수/함수명이 프로퍼티명과 같으면 프로퍼티 값 생략 가능  
선언된 변수/함수/클래스 export 가능.  

**<i>IMPORT</i>**  
예. import { pi, square, Person } from './lib'; // **<i>객체 디스트럭처링의 문법을 사용</i>**, from './lib'으로부터 3개의 변수/함수를 각각 가져온다.  
디스트럭처링 필요 없이 *로 모두 가져올 수도 있다. 대표 이름 지정하거나 개별 이름을 지정할 수 도 있음.  

CommonJS > AMD(Asynchronous Module Definition)  -popularity-  
**<i>CommonJS</i>** 는 자바스크립트를 클라이언트 사이드용 언어에 국한되지 않고 서버 사이드 스크립팅, Command Line tool/Desktop GUI app./Hybrid app. 작성도 가능하게 하며, 모듈화도 가능하게 한다.

브라우저 서포트 : module 화는 스펙만 있고 실제 동작 안 함.  
**<i></i>**

**<i>Babel 6</i>** & **<i>Webpack 4</i>**

Babel은 Transpiler로 ES5 이하의 포맷으로 대상을 전환 시켜준다. Webpack은 모듈들을 하나로 묶는 역할을 한다.  
WebPack : 여러 파일을 하나로 묶어준다(MODULE bundler) -> 스크립트 태그를 하나만 써도 된다.  
*cf. 현재 브라우저들이 ES6를 완벽 지원하지 않기 때문에 Webpack 사용*  

>WebPack이 주체가 되어 hello/world/entry.js 를 하나로 뭉칠 때, babel을 이용해서 ES conversion 한다.  
**WebPack 개별 공부 필요...**  
*cf. package.json : npm install // package로 정의된 프로그램들을 일괄 설치*  


**<i>babel</i>**  
>dist 폴더에 ES3 버전의 js 생성  
src/js/entry.js -> dist/js/entry.js  
src/js/hello.js -> dist/js/hello.js  
src/js/world.js -> dist/js/world.js  

**<i></i>**
exports.default = 'Hello';    //exports는 node.js 문법  
브라우저는 모름, 브라우저 reference error

cf. 면접 때 회사의 기술스택을 알아볼 필요도 있음  

# Node.JS

>서버 사이드에서 자바스크립트를 동작하게 하는 **런타임(동작하게 하는) 환경**  
브라우저를 동작하지 않아도, NODE.JS 환경에서 JS를 동작 시킬 수 있게 한다.  

*cf. 서버 구축이 다른 언어에 비해서 수월함(이유는?? )*  

>HOST object가 다르다 (클라이언트 사이드와의 차이 **<i>window VS global</i>**)  

>Node.JS 환경에서 자바스크립트 사용하여 서버 사이드를 구현하면 I/O가 많은(사용자 interaction) SPA를 구현하는데 적합함. 복잡한 처리를 하는 (CPU 사용률이 높은) 어플리케이션에는 부적합 (게임 등)  


*cf. REPL? node 명령어로 Node.js REPL을 실행*  


요청이란? HTTP를 이용하여 메시지(GET/POST 등)를 보내는 것.  
POST : 페이로드에 메시지가 있음  

**<i>XMLHTTPRequest</i>**  
요청 보내기 위한 준비 단계로 XMLHTTPRequest객체의 인스턴스(xhr)를 생성
인스턴스 생성하고 open 메소드로 HTTP 요청을 지정한 후 send 메소드로 요청을 보낸다.


'보냈다' 라는 이벤트가 발생하고 서버로부터의 응답이 오면 readyState에 변화가 발생  
(응답 유형이 있음 200,201,404 등등)  


node.JS 서버(express)는 에러 발생 시 서버 다운.

# npm
**<i></i>**
Node.JS에서 사용 가능한 **<i>모듈</i>** 들을 패키지화 -> 그 패키지의 **<i>저장소</i>**  
패키지를 명령어에 따라 클라이언트에게 보내주기도(설치) 한다.  

**<i>package.JSON</i>** : 패키지를 관리하는 설정 파일

>package.JSON 을 전달 받아서  
**"npm install"** 입력하면 JSON에 있는 depedencies를 설치하게 된다.
"dependencies": {               // 설치된 패키지 (배포할 때 포함되는 패키지 - 서버용)  
    "node-emoji": "^1.8.1"  
  },  
  "devDependencies": {},          // 개발할 때만 필요한 패키지  --save-dev 하면 devdependencies에 설치됨.  
*cf. 옵션 -- 와 - 차이*  
    축약되지 않은 완전한 옵션 -- 사용 (--save)  
    축약형은 - 사용 (-y)  

지역 설치 & 전역 설치
지역 설치하게 되면 프로젝트 루트에 node_modules 폴더가 생성되며 해당 프로젝트 내에서만 패키지들을 사용 가능하다.  

### Sem. Ver.
>version 구성 예."babel-cli": "^6.26.0"  
[6은 major change, 26은 minor change, 0은 patch 발생할 때]  

## ROUTING

백엔드와 프론트엔드에서 차이 있음
화면 전환
백엔드 : 각각의 REST API 요청마다 분기해서 일을 하는 개념.
>예.  
app.get('/', (req, res) => res.send({id: 1, content: 'html', completed: true}));  
app.get('/todos', (req, res) => res.send([  
  {id: 22, content: 'html', completed: true},  
  {id: 2200, content: 'html', completed: true}]  
));  
**<i>라우팅 요약</i>**  
요청 URL (여기서는 "/", "/todos" 차이)과 request method에 따라 서버 사이드에서는 다른 데이터를 send(**<i>request handler</i>**)하고 있다.  
**<i>request handler</i>** 는 라우팅된 요청(서버가 할 일)을 수행하는 함수를 의미한다.  

*cf. SPA는 최초 요청 시 HTML/CSS/JS 모두 받는다. 그 이후에는 서버와 JSON만 주고 받는다. (비동기적 통신)*  

### 최초 HTML 주기
**<i></i>**
>정적 파일(HTML)을 주는 기능 추가하기<br>
app.use(express.static('public'));  
// load 시 rest API 보다 **<i>정적파일 제공</i>** 이 우선한다.  
app.get('/', (req, res) => res.send({id: 1, content: 'html', completed: true}));  
// client 요청(get)에 대한 응답 : request handler로 처리한다.

*cf. OUTPUT by Angular*  
 HTML + CSS + JS(결국 모듈의 집합)  

*cf. requestbody 의 payload를 꺼내올 package 필요 => body-parser*

**<i></i>**
 >**<i>AJAX 요약</i>**  
 서버측 스크립트와 통신하기 위한 XMLHttpRequest 객체를 사용하는 것을 말한다. 이를 위해 XMLHttpRequest의 새로운 인스턴스를 생성한다.   
 
## 환경 준비

|  <center>준비물</center> |  <center>설명</center> |  <center>keywords</center> |
|:--------|:--------|:--------|
| client side JS파일 | 서버로 요청할 내용 | GET/POST/DELETE 등의 method(요청)를 보내서 특정 행위를 수행.<br> 요청을 보내기 위한 준비 xhr 인스턴스 생성 -><br> open(method) -><br> send<br> (POST일 때)JSON 파일에 대한 stringify 필요 |
| server side JS파일 | 클라이언트 요청에 대한 응답 | req, res |
| node.JS | JS를 서버 환경에서 활용하기 위한 런타임 환경 |
| express | Node.JS 환경에서의 웹 프레임워크/라이브러리| 역할<br> - 각 URL에서 발생하는 HTTP method들을 처리하기 위한 request handler 생성<br> - *응답 생성을 위한 view rendering engine과의 결합(?)*<br> [from MDN]|

**<i></i>**

- Note<br>
This flexibility is a double edged sword. There are middleware packages to address almost any problem or requirement, but working out the right packages to use can sometimes be a challenge. There is also no "right way" to structure an application, and many examples you might find on the Internet are not optimal, or only show a small part of what you need to do in order to develop a web application. (from MDN)

