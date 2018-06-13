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
