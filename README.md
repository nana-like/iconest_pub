# Go Vote

**nykim@nykim.net**

_Last Modified: 2018-08-29_

## Tree Structure

- images/
- html/
- fonts/
- css/
  - scss-helpers/
    - \_colors.scss
    - \_mixins.scss
    - \_variables.scss
  - scss/
    - base/
      - \_common.scss
      - \_reset.scss
      - \_font.scss
      - base.scss
    - hs/
      - hs.scss
    - ny/
      - ny.scss
  - base.css
  - hs.css
  - ny.css
- index.html
- README.md

---

## Git Repository

- 파일 공유는 기본적으로 깃헙(Github)을 사용합니다.
- 원격 저장소 주소는 다음과 같습니다.
  - [https://github.com/AnnYKim/iconest_pub/](https://github.com/AnnYKim/iconest_pub)
- 현재 총 3 개의 브랜치가 있습니다.
  1. master
  2. style-hs
  3. style-ny
- 작업 전 master 브랜치를 pull 해주세요.
- 기본적인 작업은 자신의 브랜치에서 진행하고, 작업이 완료되면 master 브랜치에 merge 해주세요.

---

## CSS Management

- css/ 폴더 내 scss/, scss-helpers/ 폴더가 있습니다.
- scss-helpers/ 폴더는 믹스인이나 변수 등을 담고 있습니다. 필요시 추가하시면 됩니다.
- scss/ 폴더 내에는 base/, hs/, ny/ 폴더가 있습니다.

  1. base: 리셋, 폰트를 정의하고 있습니다. 수정 시 충돌이 일어날 가능성이 높아서, base 를 덮어씌우려면 개별 폴더 내에서 따로 정의해야할 것 같습니다.
  2. hs: 혜성님은 여기서 작업해주세요 :) 컴파일한 hs.css 가 css/ 폴더 내에 들어가도록 해주세요.
  3. ny: 저는 여기서 작업합니다~

- scss 파일들은 **각각 컴파일**하여, base.css, hs.css 와 ny.css 를 만듭니다. 이 css 는 html 페이지를 띄었을 때 view 확인 용이며, **프론트단에는 scss 만 전달할 예정**입니다.
- 컴파일러는 원하시는 걸로 사용해주세요!

- 공통으로 사용할 폴더

  1. scss-helpers/
  2. scss/base/

- 개별로 사용할 폴더

  1. scss/hs/
  2. scss/ny/

- 스타일 작업은 개별 폴더에서 진행해 주세요. 컴파일하실 때, 자신이 작업한 파일들을 scss 에 import 하면 됩니다. 개별 폴더 내 하위폴더를 더 만드셔도 상관 없습니다(예. modules/, layout/ 등).

- 예를 들면, hs.scss 는 우선 scss-helpers 폴더의 scss 를 import 합니다.
- 그런 다음, 자신이 작업한 table.scss 등을 import 합니다.

  ex)
  ```
  @import "../../scss-helpers/mixins";
  @import "modules/table.scss";
  @import "layout/transaction.scss";
  ...
  ```

- html 파일에서는 공통 CSS(base.css)와 개별 CSS(hs.css, ny.css)를 모두 연결합니다.

  ex)
  ```
  <link rel="stylesheet" href="css/base.css" /> 
  <link rel="stylesheet" href="css/hs.css" /> 
  <link rel="stylesheet" href="css/ny.css" />
  ```

- **공통으로 사용할 요소는 components.html** 파일에도 작성합니다. 따라서 마크업 중, 다른 사람이 작업한 요소(버튼 등)가 필요하면, components 페이지에서 확인해 복사하여 사용합니다.

---

## Markup Guide

- 전체를 .wrap 이라는 div 로 감쌉니다.
- 이외에는 가능한 빨리 작성할 수 있게 원하시는 방식으로 작성해 주세요. 혜성님이 작업해 주신 부분을 보고 제가 가능한 맞춰 작업하겠습니다.

---

## Class Name Guide

- suffix 와 스타일 네임은 하이픈(-)로 연결합니다. (예. button-blue)
- 선택자 대신 가능한 clss name 으로 셀렉팅합니다.
- 이외에는 가능한 빨리 작성할 수 있게 원하시는 방식으로 작성해 주세요. 혜성님이 작업해 주신 부분을 보고 제가 가능한 맞춰 작업하겠습니다.

---

## CSS Guide

### 1.fonts

- 기본 폰트는 'Noto Sans'를 사용하며, /\_font.scss 에서 정의합니다.
  - normal
  - bold

### 2.crowss browse

- 크롬 / 모던 브라우저 기준으로 작업합니다.

---
