# An overview of the engine, the runtime, and the call stack

As JavaScript is getting more and more popular, teams are leveraging its support on many levels in their stack - front-end, back-end, hybrid apps, embedded devices and much more.
```
JS가 점점 더 유명해지면서 개발팀들은 스택 별(프론트/백엔드, 하이브리드 앱, 임베디드 디바이스 등등)로 여러 레벨에서 JS의 이점을 유용하게 활용하고 있다.  
```
This post is meant to be the first in a series aimed at digging deeper into JavaScript and how it actually works: we thought that by knowing the building blocks of JavaScript and how they come to play together you’ll be able to write better code and apps. 
```
이 포스트는 JS에 대한 심도 있는 이해와 JS가 실제로 어떻게 동작하는지 알아보기 위한 연재 중 첫번째에 해당한다.
```
We’ll also share some rules of thumb we use when building SessionStack, a lightweight JavaScript application that has to be robust and highly-performant in order to stay competitive.
```
이 연재에서는 우리가 SessionStack, 견고하고 뛰어난 경량형 JS 어플리케이션을 만들 때 사용하는 일종의 실무적인 노하우 또한 공유할 예정이다.
```
As shown in the GitHut stats, JavaScript is at the top in terms of Active Repositories and Total Pushes in GitHub. It doesn’t lag behind much in the other categories either.
```
Githut stat에서 확인한 바와 같이 JS는 활성화 상태인 저장소와 Push 총 개수 측면에서 최상위에 위치한다. 또한 다른 카테고리에서도 크게 뒤쳐지지는 않고 있다.
```
If projects are getting so much dependent on JavaScript, this means that developers have to be utilizing everything that the language and the ecosystem provide with deeper and deeper understanding of the internals, in order to build amazing software.
```
프로젝트가 JS에 크게 의존적이 된다면, 개발자들은 언어와 그것의 생태계가 제공하는 모든 것들을 내부 동작 원리에 대한 깊은 이해를 바탕으로 JS를 활용해야 한다. 더 멋진 SW를 만들기 위해서 말이다.
```
As it turns out, there are a lot of developers that are using JavaScript on a daily basis but don’t have the knowledge of what happens under the hood.
```
알려진 바와 같이 요즘은 매일 같이 JS를 사용하는 많은 개발자들이 있다. 그러나 JS 안에서 어떤 일들이 벌어지는지 알고 있는 개발자는 많지 않다.
```

## Overview
Almost everyone has already heard of the V8 Engine as a concept, and most people know that JavaScript is single-threaded or that it is using a callback queue.
```
거의 모두들 v8엔진이 무엇인지 들어는 보았다. 그리고 대부분 JS는 단일 스레드라는 것 또는 callback queue를 이용한다는 것을 알고는 있다.
```
In this post, we’ll go through all these concepts in detail and explain how JavaScript actually runs. By knowing these details, you’ll be able to write better, **non-blocking** apps that are properly leveraging the provided APIs.
>**non-blocking** : 비동기 처리를 할 수 있는, JS가 아닌 동작이 끝날 때 까지 기다릴 필요가 없는 동작 방식 *(보완필요)* 
```
이 포스트에서 이러한 개념들을 깊이 있게 다뤄보고 JS가 어떻게 동작하는지 설명할 것이다. 이러한 세부사항을 알게 됨으로써 더 나은 코딩을 할 수 있고 API를 적절히 활용하는 non-blocking 앱도 작성할 수 있을 것이다.
```
If you’re relatively new to JavaScript, this blog post will help you understand why JavaScript is so “weird” compared to other languages.
```
당신이 JS가 상대적으로 낯설다면 이 포스트가 왜 JS가 다른 언어와 비교했을 때 조금은 이상해? 보이는지에 대한 이해를 도울 수 있을 것이다.
```

And if you’re an experienced JavaScript developer, hopefully, it will give you some fresh insights on how the JavaScript Runtime you’re using every day actually works.
```
또는 JS에 경험이 있는 개발자라면 매일 같이 사용하는 JS의 Runtime이 어떻게 동작하는지에 대한 새로운 시각을 얻을 수 있을 것이다.
```

V8 used to have two compilers
Before version 5.9 of V8 came out (released earlier this year), the engine used two compilers:
V8은 2개의 컴파일러를 갖고 있었다. 버전 5.9 V8 엔진(2017년 초반 출현)의 출시 이전에 엔진은 두 개의 컴파일러를 갖고 있었다는 뜻이다.

full-codegen — a simple and very fast compiler that produced simple and relatively slow machine code.
Crankshaft — a more complex (Just-In-Time) optimizing compiler that produced highly-optimized code.
The V8 Engine also uses several threads internally:

full-codegen과 crankshaft
full-codegen은 단순하고 빠른 컴파일러이다. 심플하고 상대적으로 느린 기계어를 산출해 낸다.
crankshaft는 더 복잡한(JIT) 최적화용 컴파일러이다. 
```
The V8 Engine also uses several threads internally:
The main thread does what you would expect: fetch your code, compile it and then execute it
There’s also a separate thread for compiling, so that the main thread can keep executing while the former is optimizing the code
A Profiler thread that will tell the runtime on which methods we spend a lot of time so that Crankshaft can optimize them
A few threads to handle Garbage Collector sweeps
```
V8엔진은 내부적으로 몇몇의 스레드를 사용한다.
메인 스레드는 우리가 기대하는 대로 동작한다. 코드의 fetch -> 컴파일 -> 실행이 그것이다.
또한 컴파일을 위한 분리된 스레드도 존재한다. 그래서 이 스레드가 코드를 최적화하는 동안에도 메인 스레드는 지속적으로 코드를 실행할 수 있다.
시간이 많이 소요되는 메소드에 대한 런타임을 알려주는 ***프로파일러 스레드*** 가 있어서 Crankshaft가 그것들을 최적화할 수 있다.
```
When first executing the JavaScript code, V8 leverages full-codegen which directly translates the parsed JavaScript into machine code without any transformation. This allows it to start executing machine code very fast. Note that V8 does not use intermediate bytecode representation this way removing the need for an interpreter.
```
JS 코드를 처음 실행할 때, V8은 그 어떤 형태 변형 없이도 파싱된 JS를 기계어로 바로 해석하는 full-codegen을 활용한다. 이는 full-codegen이 기계어 코드를 매우 빠르게 실행할 수 있게 한다. V8 엔진은 중간 단계의 바이트 코드 표현(intermediate bytecode representation) 을 사용하지 않는다.  
```
When your code has run for some time, the profiler thread has gathered enough data to tell which method should be optimized.
Next, Crankshaft optimizations begin in another thread. It translates the JavaScript abstract syntax tree to a high-level static single-assignment (SSA) representation called Hydrogen and tries to optimize that Hydrogen graph. Most optimizations are done at this level.
```
코드가 일정 시간동안 실행 되었다면 ***프로파일러 스레드*** 가 어떤 메소드가 최적화 되어야 하는지를 알려주기 위한 충분한 데이터를 모은다.  
그 다음으로 Crankshaft 최적화는 다른 스레드에서 시작된다. 이것은 JS의 추상적인 syntax tree를 고수준의 정적 단일 할당 표현-static single-assignment (SSA)-(hydrogen이라고 불리기도 함)으로 해석한다. 그리고 Hydrogen 그래프를 최적화하려 한다.  대부분의 최적화 작업은 이 단계에서 끝난다.  
```
Inlining
The first optimization is inlining as much code as possible in advance. Inlining is the process of replacing a call site (the line of code where the function is called) with the body of the called function. This simple step allows following optimizations to be more meaningful.
```
인라이닝
최초 최적화는 사전에 가능한 많은 코드들을 inlining한다. inlining은 호출된 함수 몸체와 call site를 대체하는 프로세스이다.  
>call site? 함수가 호출되는 코드 라인
이 간단한 단계는 후속 최적화 단계들을 보다 의미 있게한다.  
```
Hidden class
JavaScript is a prototype-based language: there are no classes and objects are created using a cloning process. JavaScript is also a dynamic programming language which means that properties can be easily added or removed from an object after its instantiation.
```
숨겨진 클래스  
JS는 프로토타입 기반 언어이다. 클래스라는 개념은 없고 객체가 복제 과정을 이용하여 생성된다. JS는 또한 ***동적 프로그래밍*** 언어이다. 객체의 객체화 단계 이후에 프로퍼티들이 쉽게 추가되거나 삭제될 수 있다는 것을 말한다.  
```
Most JavaScript interpreters use dictionary-like structures (hash function based) to store the location of object property values in the memory. This structure makes retrieving the value of a property in JavaScript more computationally expensive than it would be in a non-dynamic programming language like Java or C#. 
In Java, all of the object properties are determined by a fixed object layout before compilation and cannot be dynamically added or removed at runtime (well, C# has the dynamic type which is another topic). 
As a result, the values of properties (or pointers to those properties) can be stored as a continuous buffer in the memory with a fixed-offset between each. The length of an offset can easily be determined based on the property type, whereas this is not possible in JavaScript where a property type can change during runtime.
```
대부분의 JS 인터프리터는 해쉬 함수 기반의 유사 사전 구조(dictionary-like structures)를 사용한다. 이는 객체의 프로퍼티 값의 위치(in memory)를 저장하기 위함이다.  이러한 구조는 비 동적 프로그래밍 언어(JAVA, C# 등)와 비교했을 때 프로퍼티 값을 획득하는 것을 보다 비용 소모적으로 만든다.  
자바에서는 모든 객체의 프로퍼티들은 컴파일 이전에 고정된 객체 레이아웃에 의해 결정되고 런타임 동안에 동적으로 추가/제거될 수 없다.  
결과적으로 프로퍼티 값은 고정된 offset을 갖는 연속적인 버퍼에 저장될 수 있다. offset의 길이는 프로퍼티 유형에 따라 결정된다. (JS에서는 이렇게 할 수 없다. 심지어 런타임 중에 프로퍼티가 변경 가능하다.)
```
Since using dictionaries to find the location of object properties in the memory is very inefficient, V8 uses a different method instead: hidden classes. Hidden classes work similarly to the fixed object layouts (classes) used in languages like Java, except they are created at runtime. Now, let’s see what they actually look like:
```
사전을 이용해서 메모리에 있는 객체 프로퍼티의 위치를 찾는 것은 매우 비효율적이기 때문에 V8엔진은 다른 방법을 택했다: 숨겨진 클래스가 그것이다. 숨겨진 클래스는 자바와 같은 언어에서 사용되는 고정 객체 레이아웃(클래스)과 유사하게 동작한다. 단 숨겨진 클래스들은 런타임에 생성된다.  
```
function Point(x, y) {
    this.x = x;
    this.y = y;
}
var p1 = new Point(1, 2);
```