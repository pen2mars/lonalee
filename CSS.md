# nudge 실습

## header

nav 태그 float right, 메뉴 간 padding으로 간격 확보.
nav-items의 각 li요소는 inline-block으로 배치.
logo 이미지는 위,아래 margin으로 가운데 위치 시킴.
헤더 영역 전체를 position : fixed로 고정 시킴.

## content-wrap

2개의 자식 요소로 aside, section을 갖는다.
두 자식 요소를 float으로 배치하면 부모 요소인 content-wrap은 height가 0이 되어 버린다. 그래서 content-wrap의 after 가상 식별자에 clear: both를 한다.
section은 article 포함.

이상 layout_float.html
