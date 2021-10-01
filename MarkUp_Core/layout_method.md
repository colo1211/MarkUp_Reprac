# CSS Layout 방법

### 1. float : left

* 핵심 : `width % 조정` , `float : left` , `clear : both` 

1. 모든 요소를 감싸는 wrapper(container)를 만든다.
2. div는 display : block 의 속성을 가졌기 때문에 한 줄을 모두 차지하는 특성을 가짐
3. 따라서 wrapper를 기준으로 width 를 % 주는 것이 중요
4. 이후 `float : left` (왼쪽 정렬) , 붕 띄워서 왼쪽에 정렬해준다.  
5. 붕 띄웠기 때문에 아래에 footer는 header의 바로 아래에 배치된다. 따라서 left, right 아래에 배치되게 하기 위해서는 `clear : both` 를 사용한 이후에 해주어야 제대로 배치된다. 

### 2. display : inline-block 

* 우선 이 방법은 비추

`display : inline-block;` 
* 내 크기만큼 차지 (그림과 글이 어울림. 즉, 글자처럼 취급)
* 파란색과 coral색의 Box를 `inline-block` 속성을 넣게 되면 글자처럼 취급되기 때문에 다음과 같이 줄을 띄워서 코딩하면 다음 칸에 오게 된다. 


```
<div class='left'></div>
<div class='right'><p>안녕하세요</p></div>  
```

![image](https://user-images.githubusercontent.com/63600953/135571852-11f2982b-194c-45de-aa54-8002728bb647.png)

이를 해결하기 위해서는 글자처럼 취급하기 때문에 

```
<div class='left'>2</div><div class='right'><p>안녕하세요</p></div>   
```

![image](https://user-images.githubusercontent.com/63600953/135572186-b313945f-7f3a-4df1-b4dc-6b3541186341.png)

다음과 같이 코드를 붙여주면 바로 옆에 오게 된다. 

하지만, 코드를 옆에다가 붙이면 가독성이 매우 떨어지기 때문에 다음과 같이 주석으로 처리하는 방법도 존재한다.

```
            <div class='left'></div><--
         --><div class='right'><p>안녕하세요</p></div>   
```

하지만 coral 색으로 된 div 에 글씨를 넣어주게 되면 다음과 같이 div는 발작을 일으키게 된다. 
이는 현재 파란색과 coral 색을 inline-block으로 글자처럼 취급하였기 때문에 발생하는 현상으로 파란색을 글자로 인식하여 글의 Base-Line으로 인식하여 나타나게 되는 현상이다.
![image](https://user-images.githubusercontent.com/63600953/135572517-50844015-479a-415e-aa88-5deeede8e0ce.png)

* left-box에 `vertical-align : top` 을 해주면 된다. 
```
.left {
    width : 20%; 
    height : 400px; 
    background-color: cornflowerblue;
    display: inline-block; 
    vertical-align: top;
}
```

![image](https://user-images.githubusercontent.com/63600953/135572966-86fb85f2-85fc-4db5-ae5b-7ef18d48f05b.png)
