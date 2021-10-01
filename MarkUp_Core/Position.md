# Position 

: margin으로 물체의 위치를 이동시키는 것도 가능하지만, `좌표 속성`으로 배치를 가능하게 하는 것이 `Position` 개념이다.
* 특징 
  1. position 속성을 활용하게 되면 공중에 붕 뜬다. (따라서, 글자에 따라 아래로 밀려나지 않고 붕 띄워서 위치함을 알 수 있다)
  2. 좌표 이동 가능
    
### 1. position : relative

* `내 원래 위치를 기준`으로 이동
* 기준점 position : relative
* 좌표 이동 : top / bottom / left / right 

```
    position: relative; /* 기준점을 잡는 속성 */
    top : 100px;
    left : 100px;
```

![image](https://user-images.githubusercontent.com/63600953/135607737-0fe9b7a6-ffa9-4272-81a7-25bc05e1312a.png)


### 2. position : static (default 값)

* 좌표 이동 X

### 3. position : fixed 

* 화면 고정 
* `현재 화면(View Port)`이 기준
* 화면에 달라 붙는 요소를 구현이 가능해진다. 
* 스크롤과 상관없이 따라오는 상단 고정 메뉴 (NavBar) 등을 구현하고 싶을 때 사용하는 position 속성

![image](https://user-images.githubusercontent.com/63600953/135608337-e06fc813-b512-44a8-8dcb-3b75de2d7aab.png)

### 4. position : absolute 

* 내 `부모 태그가 기준`
* 부모 태그 중에 `position : relative` 를 가진 부모가 기준

![image](https://user-images.githubusercontent.com/63600953/135608781-c07673bd-da3e-430f-bd2c-d467d724ebc6.png)

* 부모 태그 (이미지) 에는 `position : relative`
* 자식 태그 (버튼) 에는 `position : absolute` + `좌표속성`
* 자식 태그가 부모태그에 착 달라 붙어 좌표속성을 지정하여 위치를 조정할 수 있다

```
    position: absolute;
    bottom : 0px;
    right : 0px;
```

Tip! position : absolute 가운데 정렬하는 방법

```
    position: absolute;
    left : 0;
    right : 0;
    margin : auto;
    width : 적절한 px;
```