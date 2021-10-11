# HTML / CSS 

* HTML / CSS / SASS / Bootstrap 등 마크업을 학습하면서 배웠던 내용들을 토대로 웹사이트를 Targeting 하여 그대로 만들어 보거나 응용하는 학습을 진행하였음
* 4개 중 1개는 내용을 익혀가면서 만든 결과물 (쇼핑몰)
* 4개 중 3개는 타겟을 본 후 스스로 만든 결과물 (Landing Page, SNS, Admin Page)

---
## 1. Shopping Mall

`PC View`

![127 0 0 1_63577_part2_LandingPage html](https://user-images.githubusercontent.com/63600953/136647409-d3f82e36-f2b0-4911-b743-601c424bf81b.png)

`Tablet View`

![127 0 0 1_63577_part2_LandingPage html (2)](https://user-images.githubusercontent.com/63600953/136647569-a60752ef-aadd-4c16-8f07-2a2b8f5f4fb5.png)

`Mobile View`

![127 0 0 1_63577_part2_LandingPage html (3)](https://user-images.githubusercontent.com/63600953/136647593-5099c4ef-4e1c-4e54-bc89-95d60d7ad820.png)



* 애니메이션을 적용
  
![image](https://user-images.githubusercontent.com/63600953/136647439-974e4354-1d88-4b9d-9cf3-f7a08319d333.png)

신발 사진에 Hover하게 되면 그에 해당하는 가격을 회색 박스로 절반정도 띄우게 설정하였음

---
## 2. Landing Page

* 휴대폰 판매 사이트의 랜딩페이지를 가정하고 제작하였음. 
* 반응형 제작할 때 `미디어 쿼리`와 `float : left` 만을 사용하였음. 

`PC View`

![127 0 0 1_63577_part2_LandingPage_2 html](https://user-images.githubusercontent.com/63600953/136647624-c41ac67f-c5b1-4fc7-992e-87e95d268783.png)

`Mobile View`

![127 0 0 1_63577_part2_LandingPage_2 html (1)](https://user-images.githubusercontent.com/63600953/136647675-873703a3-7a9d-4c57-97f2-e4acbaeed28b.png)



---
## 3. SNS Profile 

* 반응형을 제작할 때 미디어쿼리, `float : left` 가 아닌 bootstrap의 `grid` layout을 사용하였음


* sm/md/lg 의 조건을 활용하여 반응형을 쉽게 만들었음 


`PC View`

![127 0 0 1_63577_part2_SNS_Profile html](https://user-images.githubusercontent.com/63600953/136647471-01fefc14-fbc1-4c04-8454-934d05b3b45c.png)

`Mobile View`

![127 0 0 1_63577_part2_SNS_Profile html (1)](https://user-images.githubusercontent.com/63600953/136647746-1f90ccf3-5310-4226-b71d-a97f53aa08e1.png)


* 애니메이션을 따로 적용하지 않았고 반응형에 집중하였음

--- 
## 4. Admin Page

* side-bar-menu를 구현
* search bar 에 애니메이션을 부여 ( focus시, width 증가 )
* 차트 그래프를 `Canvas` 를 활용하여 가져와 보았음

`PC View`

![127 0 0 1_63577_part3_AdminPage html](https://user-images.githubusercontent.com/63600953/136647834-e83ad297-1498-42fe-b56a-f1cbaa6f773f.png)

`Mobile View`

* 현재 캡쳐를 Chrome 스크린샷을 활용하였고, 실제 작동시에는 side bar가 height 가 100vh이다. 
따라서 사용자가 스크롤을 아래로 내릴 때, side-bar가 viewport에 맞게 맞춰지기 때문에 아래와 같이 캡쳐된 것이다.

![127 0 0 1_63577_part3_AdminPage html (3)](https://user-images.githubusercontent.com/63600953/136647962-42d82b5a-6dd0-498a-b4c1-70a85e43daeb.png)

* Side Bar 애니메이션 </br> 
: side bar에 hover(마우스를 사이드바에 올림) 하게 되면 아이콘에 맞는 글씨들이 정렬되도록 애니메이션을 설정 
  * 모두 `transform : translateX( px);` 로 해결

![image](https://user-images.githubusercontent.com/63600953/136648043-2e101f05-f466-44a1-99d9-af62e9923a79.png)


* Search Bar 애니메이션 </br>
: 사용자가 Search Bar에 Focus (클릭) 했을 때 Search Bar가 길이가 길어진다. 

![image](https://user-images.githubusercontent.com/63600953/136648133-efa7ede2-1843-4979-a8b0-c83b0eb7b4f2.png)
