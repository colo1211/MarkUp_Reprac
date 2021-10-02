# Markup Tip! 

### label 태그와 for 속성

* label 태그의 for 속성 
* input 태그의 id 속성

```
<input type="checkbox" id="subscribe">
<label for="subscribe">누르기</label>
```
label과 for 속성을 적절히 활용하면

input대신 label을 눌러도 input을 선택할 수 있다.

(input의 id, label의 for 속성을 똑같이 맞춰주면 됨)

![image](https://user-images.githubusercontent.com/63600953/135701917-b2cd4843-6994-4325-9e14-ccd9c88e3086.png)

---
### vertical-align 

* 세로 정렬
* inline(폭과 너비를 가질수 없는 존재들 ex. span 태그) / inline-block 요소간의 세로 정렬을 할 때, `vertical-align`을 쓴다. 


![image](https://user-images.githubusercontent.com/63600953/135703986-11d3cfd5-9ba0-460b-847a-be52c4ca6e5c.png)


* 다음과 같이 세로 정렬이 되어있을 때 `hi` 를 세로로 정렬할때 `vertical-align`을 사용한다. 

* vertcal-align : top 
* vertcal-align : bottom 
* vertcal-align : middle

```
<div>
    <p style='font-size:50px'>greeting <span style='font-size:10px; vertical-align : middle'>hi</span></p>
</div>
```

![image](https://user-images.githubusercontent.com/63600953/135704026-1223c365-0d93-4be2-8c93-9a8b3b6865e9.png)

---
### Pseudo-Class

* a 태그

: `link -> visited`

```
.custom-link {
    /* 밑줄 제거 */
    text-decoration: none;
}

/*방문 전*/
.custom-link : link {
    color : black;
}

/*방문 후*/
.custom-link : visited{
    color : black; 
}
```


* button 태그

: `hover -> focus -> active` 순서로 해줘야 잘 적용된다. 

```
/* hfa(암기 팁: hofa.....)순서로 써줘야 함. -> pseudo class*/
.btn-style:hover{
    background-color: cadetblue;
}

/*누르고 난 이후, 손가락 뗀 후*/
.btn-style:focus{
    background-color: dodgerblue;
}

/*누르는 중, 손가락 떼기 전*/
.btn-style:active{
    background-color: aqua;
}

```

### class 제작 요령

#### OOCSS (Objected Oriented CSS)
* 뼈대용 class, 살점용 class를 각각 제작
  ![image](https://user-images.githubusercontent.com/63600953/135705883-d5719819-3d19-4963-9aa9-e381f213fdbd.png)

html
```
<button class='btn btn-red'>더 알아보기</button>
<button class='btn btn-blue'>구매하기</button>
```

css
```
/* 뼈대 */
.main-btn{
    padding : 15px; 
    font-size : 20px; 
    border : none;
    cursor : focus; 
}


/* 살점 */
.btn-red{
    background-color : red;
}

/* 살점 */
.btn-blue{
    background-color : blue; 
}
```

#### BEM Role (Block__Element--Modifier)
* class 작명할 때 창의력이 딸리면 `BEM룰`을 따라라. 

```
class = "덩어리이름__역할--세부특징"
```

![image](https://user-images.githubusercontent.com/63600953/135705994-27905339-12dc-4d5b-be20-32f81dd3db8b.png)


요즘은, React/Vue 를 사용하여 컴포넌트별로 CSS를 작성하기 때문에 OOCSS, BEM을 사용하지 않아도 괜찮음. 
