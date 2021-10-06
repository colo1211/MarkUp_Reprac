# Animation

### 방법
1. 시작 스타일 제작
2. 최종 스타일 제작
3. 언제 최종 스타일로 변하는지 (Trigger 제작)
4. transition 으로 애니메이션을 준다. 

### opacity 
0 : 투명 ~ 1 : 완전 불투명  

### 예제1
* 그림 위에 마우스를 올리면 회색 박스가 서서히 나오게 되는 animation

1. 시작스타일 

![image](https://user-images.githubusercontent.com/63600953/136142159-a818ff27-fa61-439e-978f-83be4de7d292.png)

html 
```
<div class="shop-item">
  <div style='position: relative'>
   <div class='overlay'></div>
    <img src='../이미지파일/product1-1.jpg'>
    </div>
</div>
```

css

```
.overlay {
    position: absolute; 
    width : 100%;
    height : 100%; 
    background-color: rgba(0,0,0,0.5);
    opacity : 0;
    transition: all 1s; 
/*    위에 있는 스타일이 변하게 된다면, 1초에 걸쳐서 서서히 변하게 해주세요. */
}
```
2. 최종스타일
  
![image](https://user-images.githubusercontent.com/63600953/136142233-f90c94ab-22cd-4b57-9199-4c06bc1cb0c2.png)

```
.overlay:hover{
    opacity: 1; 
}

```

3. Trigger : hover


4. `transition : all 1s` 은 시작화면에서 써준다.  

### 예제2 

* 그림 위에 마우스를 올렸을 때, 아래서부터 천천히 네모박스가 올라오는 것

1. 시작스타일
   

![image](https://user-images.githubusercontent.com/63600953/136145127-64ba1de9-9061-4721-993d-00a8b5e47ba6.png)

* html 
```
<div class="shop-item">
  <div style='position: relative'>
  <div class='overlay-wrap'>
   <div class='overlay price'>3000$</div>
  </div>
    <img src='../이미지파일/product1-1.jpg'>
    </div>
</div>
```

* css

```
.overlay-wrap {
    position: absolute;
    width : 100%;
    height : 100%;
    overflow: hidden;
}

.overlay {
    position: absolute;
    width : 100%;
    height : 50%;
    background-color: rgba(0,0,0,0.3);
    top : 100%;
    transition : all 1s; 
}
```

2. 최종스타일

![image](https://user-images.githubusercontent.com/63600953/136145261-246a5a06-3ad3-4585-af52-2cf0cd2eede9.png)

```
/*wrap에 hover하면 overlay가 올라온다.*/
.overlay-wrap:hover .overlay{
    top : 50%;
}

```
3. 트리거 : hover

: CSS에서는 Selector 가 없기 때문에 html 을 overlay를 감싸는 wrap을 만든다. 

* overlay-wrap(부모) 을 hover 하면 overlay(자식)이 올라오는 것이 가능
* 하지만, 형제끼리는 이것이 불가능

```
부모와 자식간의 관계만 가능하다. 
```


4. transition 