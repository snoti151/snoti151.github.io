---
title: "마인크래프트 모델링 #2"
date: 2020-10-22 17:35:00 +0900
categories: [Modeling, Practice]
tags: [modeling]
toc: false

---

> 해당 게시글은 PC 작업환경에서 작성 되었으며 모바일에서 보기에는 부적합 할 수 있으니 PC로 접속해주시길 바랍니다.

[TOC]



## 3차원 모델링이란?

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMzMg/MDAxNTk4MDY1NTkyMzY4.JQdYHhcXcZogS_G6gKCeIo2k63l7YXQ_i-mmOhPC3lEg.RaHyv3bTOKnYkOI9KyzXh72hDzpznWbPvwteN6jkf9cg.PNG/0.PNG?type=w1600)

<img src="https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMjQz/MDAxNTk4MDY2NTk4NjM5.fWGthqYdX_Jw6uWVz3XWImz8NKNHgxhymrrjnr6X8pIg.cfLUC9lQ-h5sCzaGCCxewrGqD9mPEkDuFofCPZ5VEvMg.GIF/%EC%95%84%EC%9D%B4%EB%B2%88_%EC%84%9C%EB%8D%9C%EB%9E%9C%EB%93%9C%EC%9D%98_%EC%8A%A4%EC%BA%90%EC%B9%98%ED%8C%A8%EB%93%9C.gif?type=w1600" alt="img" style="zoom: 150%;" />

아이번 서덜랜드(Ivan Sutherland)의 스케치패드

### 모델링 ( Geometric modeling )

과거의 모델링은 도면을 따로제작하고, 진흙과 같은 모형을 만들고, 실물을 만드는 과정이 복잡하고, 불편하고, 정확성과 효율면에서 떨어짐에 있어서 해답을 찾을려고 했습니다.

이를 해소하기 위해 모델링 설계자들에게 편한방식으로 만든 것이 지금 현재 지오메트릭 모델링 방식입니다.

보다 설계자가 더욱 더 편한 환경을 조성하기 위해서 개발된 만큼 제품설계시 설계자가 평면 데이터인 도면을 그린 후 컴퓨터 화면에  3차원의 모델을 만들어주고, 실물과 유사한 환경을 조성 및 물체의 질감이나 형태를 보다 쉽게 보고 수정 할 수 있게 수 많은  소프트웨어가 등장했습니다.

이 후에도 여러 분야로 파생되면서 오직 도면 제작만이 아닌 디자인, 예술적인 부분들과 결합되어 현재 우리가 하는 게임, 영화,  애니메이션에서 자주 접할 수 있습니다. 모델링의 분야를 크게 나누자면 시각적인 디자인, 공학적인 엔지니어링으로 두개를 나눕니다.

그 수많은 소프트웨어중 저희는 마인크래프트에서 사용되는 3D모델링 프로그램를 소개 할 것 입니다.



### 작업방식

· 폴리곤 모델링 (Polygon modeling): 점, 모서리, 면 3가지를 이용해서 작업, 작업처리 속도가 가장빠름 곡선 표현에 어려움이 있음.

· 커브 모델링 (Curve modeling): 비균일 유리 B-스플라인 (NURBS) 을 이용해서 작업, 곡선이 많은 공업설계을 위해 선호됨

· 스컬프트 모델링 (Scuplt modeling): 찰흙을 이용해서 조소를 하는것 과 유사한 방식으로 작업, 개인의 예술적 능력이 요구 됨.

### 마인크래프트의 모델링

마인크래프트는 **LWJGL** (Light Weight Java Game Library) 엔진을 이용해서 만들어진 게임 입니다. 

따라서 모델링 방식은 게임에 적합한 폴리곤 모델링 방식 입니다.

그렇지만 우리가 작업하는 리소스팩에 들어가는 모델링은 폴리곤 모델링과는 다르게 지극히 제한적입니다.

이 밑의 내용들은 **JE버전용 리소스팩**을 만드실 때 유의 하셔야 할 점들입니다.

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMjYx/MDAxNTk4MDM1MjIyMTk5.wyBqpjmM_Sh12GVnWJjFW85-37MiwvqCUJuCahFXE4Yg.6GwtAr13Aeny0QwnOEKCyGtjiU4O20rfJMP620arm-wg.PNG/1.PNG?type=w1600)

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMjcw/MDAxNTk4MDM1MjIyMTk5.LX3a4EcwV79nabnz_eJZazPnrtCNKqFPpb9dXbQG9G0g.AcxDq60KXr8vyZ9H_sHdt-O9m06zcfc4cUWBvL4pmz0g.PNG/2.PNG?type=w1600)

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMTg2/MDAxNTk4MDM1MjIyMTk1.L3_AwODLUOCpYbDsK0Xx22l_ikO-heWeexqnHNoH6C8g.IIq3_AnXJ065kW75pkXaAEem9d6iwwdrAtI0O0b4qkgg.PNG/3.PNG?type=w1600)

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfOTgg/MDAxNTk4MDM1MjIyMjQy.hPnPR3KFWZZgDxHWylLri1_tQ2_IAVjUTYb4JTUUn9Qg.WE0OSafkb9TuVIeOL7Jkl5dHAh44KDXDMozR7fTUzCog.PNG/5.PNG?type=w1600)

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMTAx/MDAxNTk4MDM1MjIyMjM0.j3E6Rbf0Si-zauU45Im9fTg6aumzn9pkVpDM3pQrPZYg.L9w9yDBO2pLM7o4yc5AGddVvW2ulwu0lOHOH6ij5UPwg.PNG/4.PNG?type=w1600)

------



## 리소스팩



### **리소스팩과 텍스쳐팩의 차이**

~ 1.7.X : 텍스쳐팩 ( 텍스쳐만 변경이 가능함 )

1.8 ~ 1.16 : 리소스팩 ( 3D 모델링이 적용이 가능함 )



### **리소스팩의 구조**

<img src="https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMTQx/MDAxNTk4MDcyNzI2MzYx.bgqVpRwlwLaU9qaO1irm9yXwJcjNJKDmxfCzZ6VRJgQg.SgpGd0Au6U0Y0OODEPOSWEjNERKsKNRt8gKGk7FAb_sg.PNG/%EB%A6%AC%EC%86%8C%EC%8A%A4%ED%8C%A9_%EA%B5%AC%EC%A1%B0.png?type=w1600" alt="img" style="zoom:50%;" />

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMTQ3/MDAxNTk4MDcyODYyODcw.8MqdnDWRt_-EUgijEllQLlQYZGNuS-Jry1pj1QCHOMQg.bxcsMj8is6WV8YA4_A6P-beYI7j9p8UaeM9AMmj82Log.PNG/SE-a490ceb7-3ccc-4279-9295-ff2cbf885454.png?type=w1600)



#### pack.png

2의 거듭제곱 정삭각형 픽셀 크기의 이미지를 적용하실 수 있습니다. ( 64 x 64 크기를 추천 )



#### .json 파일

3D 모델들의 저장 방식은 함수값의 정보를 가지고 있고 게임 엔진, 프로그램에서 이를 시각화하게 도와주는 지표같은 역할을 하고  있습니다. 마인크래프트 리소스팩에서 사용하는 모델 파일들 역시 함수값을 저장하고 있습니다. 구조 자체가 매우 단순하고 일반적인  모델링의 개념이 포함 되어 있어서 3D 라는걸 처음 접할 때 3D 모델링에 대해 쉽게 이해 할 수 있게 도와줍니다.

그렇다면 함수값을 저장을 한다면 단순한 코딩으로 3D 모델을 만들 수 있습니다. 아래 링크는 별도의 프로그램을 사용하지 않고 단순한 문서를 작성하는 것 만으로 모델링 만드는 것을 볼 수있습니다.

[[ **바닐라 모델 튜토리얼(영문)** ]](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/resource-packs/resource-pack-discussion/1256334-vanilla-model-tutorial)

물론, 참고만 하시기 위해 자료로써 가져온것이지 굳이 저런 방식으로 하기엔 비효율적인 부분이 있지만 .json 파일의 구조를 이해하기 위해선 가장 효율적인 방법이라고 생각합니다.

그렇다면, 초심자분들이 가장 접근하기 쉽고 편의성, 효율성 면에서 두각을 드러내는 좋은 프로그램을 살펴보겠습니다. 대표적인 바닐라 리소스팩용 모델링 프로그램은 **Blockbench** 와 **CubikStudio** 입니다.

일단 JSON 파일로 작성되는 수많은것 들이 있지만 기본적으로 우리가 모델링을 만들고 최종 결과물은 크게 두개로 나뉩니다. 블록,  아이템 모델로 아래 내용들은 해당 .json 파일의 구조를 설명하고 있습니다. 본문은 마인크래프트 공식위키를 참고 및 번역했음을  밝힙니다.



\* JSON 파일은 사운드파일 속성, 데이터팩의 구문들 같이 여러분야로도 활용됩니다. 지금은 모델링에 관련된 JSON 파일들을 알아보는 과정입니다.

[[ **마인크래프트 공식위키 - 모델 JSON(영문)** ]](https://minecraft.gamepedia.com/Model)



### 모델링

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMjk1/MDAxNTk4MDczMzc2MjA5.ZJWPxC5uP2pvHhzqDqWwMFn9y8FGs6nyT3Qq3pVS5Isg.OwXVijT0nf0N4KD_OsSASgJ-P1PPJzsimuGRvonFma0g.PNG/%EB%B8%94%EB%A1%9D%EB%AA%A8%EB%8D%B8.png?type=w1600)

**[아이템모델 구조 번역문 사진]**

![img](https://cafeptthumb-phinf.pstatic.net/MjAyMDA5MTZfMjQg/MDAxNjAwMjMyMDkxNjM4.I2OrRvuPaPIuG1ipOs1_PDuiLYt0Raan8kBqp8XeHQcg.nmo93gkQuKe3REEkdcp8Tvg1P_ESNXxwe0aUPvB0i-0g.PNG/%EC%9D%B4%EB%AF%B8%EC%A7%80_1.png?type=w1600)

------



## 텍스처

블록, 아이템 텍스쳐에 관한 기능들입니다. 텍스쳐 크기는 무조건 폭(Height), 너비(Width)의 길이가 동일해야 합니다 

(만약, 텍스쳐 애니메이션을 사용한다면 너비의 크기의 배수가 되도록 폭 길이를 늘려야합니다)

| <img src="https://cafeptthumb-phinf.pstatic.net/MjAyMDA4MjJfMTk0/MDAxNTk4MDY5NDI5NDI5.IVPrjHyCl2zLY6b9C8jiieBISLsecPWfzakoElsAzBEg.FAo_NJYkI6LF5du2EIBciTeXYVGtCIJyEUqavn7Bzpkg.PNG/%EB%AF%B8%EC%8B%B1%ED%85%8D%EC%8A%A4%EC%B3%90.png?type=w1600" alt="img"  /> | ![](D:\Users\admin\Documents\GitHub\snoti151.github.io\assets\img\modelings\30.png) |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 텍스쳐가 적용이 안될경우 자홍색과 검은색으로 이루어진 체크무니 텍스쳐를 볼 수 있습니다. | 왼쪽부터 돌, 참나무 잎, 유리, 빨간색 유리 입니다. 4개의 블럭 모두 똑같은 텍스쳐를 사용합니다.대부분의 블럭은 투명도를 지원하지 않으며 유리와 같은 블럭만 투명도를 지원합니다. |

블록모델용 텍스쳐는 유리와 같이 반투명, 투명값이 적용된 텍스쳐들은 텍스쳐 수정을 통해서 투명도를 표현할 수 있습니다. 하지만, 불투명 블럭의 텍스쳐는 투명한 텍스쳐를 적용할수 없습니다.

블록 모델은 blocks 폴더안, 아이템 모델은 items 폴더 안에 텍스쳐 파일을 넣는것을 권장합니다.

텍스쳐 폴더 안에서는 개인이 지정해놓은 폴더를 불러올 수 있기 때문에 자신이 원하는 이름의 폴더를 만드시고 불러오실수도 있습니다.  텍스쳐 파일들은 2의 거듭제곱 정삭각형 픽셀 크기의 .png 파일로 이루어져 있습니다. 마인크래프트의 기본 텍스쳐를 대체하거나  개인이 지정해놓은 이름으로 된 파일도 적용하실수 있습니다.



[ 애니메이션 구조 번역문 사진 ]

------



### 마인크래프트 기본 리소스팩

**[ 다운로드 링크 ]**

**파일 첨부** [ [1.12.2 - Default Resourcepack.zip]()  ]

**파일 첨부** [ [1.16.2 - Default Resourcepack.zip]() ]

※주의사항 - 해당 파일은 **마인크래프트 기본 리소스팩**으로 추후 문제가 생길 경우 삭제될 수 있습니다.



### 외부 그래픽소프트웨어 소개

**$** 유·무료 공존/부분유료, **O** 오픈소스, **F** 프리웨어

**[마인크래프트 모델링 프로그램]**

CubikStudio **OF**: https://cubik.studio/

Blockbench **$**: https://blockbench.net/

MagicaVoxel **OF[1]**: https://ephtracy.github.io/

Blender **OF[1]**: https://www.blender.org/

**[1]** 해당 프로그램은 일반적인 방법으로 마인크래프트에 적용되지 않고 Cubikstudio, Blockbench 같은 프로그램을 거쳐야 적용이 됩니다.



**[이미지 및 텍스쳐 편집 프로그램]**

Gimp **OF**: https://www.gimp.org/

Paint.NET **$**: https://www.getpaint.net/

Krita **O$**: https://krita.org/ko/download-ko/krita-desktop-ko/

Medibang **F**: https://medibangpaint.com/ko/app-download/

Aseprite **$**: https://www.aseprite.org/



**[구문 프로그램]**

VSCode **F**: https://code.visualstudio.com/

Sublime Text: https://www.sublimetext.com/

Atom **OF**: https://atom.io/

Notepad++ **OF**: https://notepad-plus-plus.org/

JSONLint: https://jsonlint.com/



**[렌더링 사이트 및 툴]**

Blockmodels: https://blockmodels.com/

Sketchfab**[2]**: https://sketchfab.com/

Sketchfab Labs: https://labs.sketchfab.com/experiments/screenshots/

Marmoset Viewer: https://marmoset.co/toolbag/viewer/

Light Tracer: https://lighttracer.org/

Blender: https://www.blender.org/

**[2]** 해당 사이트는 베이식 유저의 경우 한달에 한번 업로드가 제한되고, 유료구독결제시 권한이 상승됩니다.



**[특별한 툴들]**

JE 모델링 텍스쳐 애니메이션 사이트: https://vberlier.github.io/animated-models/

텍스쳐 애니메이션 에디터: https://dokucraft.co.uk/stash/?animation-editor

아이템 내구도 제작 사이트: https://geenium.github.io/damage-value-generator/

BE 파티클 제작 사이트: https://jannisx11.github.io/snowstorm/

JSON 최적화 사이트: https://jsonlint.com/?reformat=compress

PNG 최적화 사이트: https://tinypng.com/



**[팔레트 자료]**

팔레트 모음: https://lospec.com/palette-list



**[팁과 가이드]**

블록벤치 공식 튜토리얼: https://cafe.naver.com/minecraftgame/1765180

베드락 버전에서 엔티티 모델링 적용하기: https://youtu.be/xoybMf05Jl8



**[리소스팩을 활용한 플러그인]**

BE용 애니메이션을 JE버전에 쓸 수 있게 컨버팅 해줍니다. [ [모델API](https://www.spigotmc.org/resources/modelapi-custom-entity-model-manager.68014/) ] [ [모델엔진(유료)](https://www.spigotmc.org/resources/conxeptworks-model-engine—ultimate-entity-model-manager-1-14-1-16-1.79477/) ]

열차에 리소스팩을 적용시켜 다양한 열차를 만들수 있는 플러그인 [ [Traincarts](https://www.spigotmc.org/resources/traincarts.39592/) ]

다양한 탈것을 만들수 있는 플러그인, 라이트버전이라 유료버전이 따로 존재합니다. [ [VehiclePlusLite](https://www.spigotmc.org/resources/vehiclesplus-lite.53588/) ]

------



## 강좌

**[ 블록벤치 모든 강좌 ]**



  **0강 - BlockBench** **빠른 시작도움말 한글번역**

https://cafe.naver.com/minecraftgame/1765180

  **1강 - lockBench** **소개 및 인터페이스 소개**

https://cafe.naver.com/minecraftgame/1765245

  **2강 - BlockBench** **조작키 및 사용법**

https://cafe.naver.com/minecraftgame/1765275

  **3강 - BlockBench** **블록벤치 모델링 실전 및 적용법**

https://cafe.naver.com/minecraftgame/1768308