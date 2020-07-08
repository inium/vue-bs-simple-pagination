# vue-bs-simple-pagination
Bootstrap Layout을 기반으로 하는 vue로 구현된 단순 Pagination 입니다.

페이지 번호를 Query String으로 사용합니다.  

## 사용방법

### 1. Clone this repository

```bash
git clone git@github.com:inium/vue-bs-simple-pagination.git
```

### 2. Component 등록

Clone 받은 프로젝트에 있는 `VueBsSimplePagination.vue`를 vue 프로젝트에 추가합니다.

```javasc
import vueBsSimplePagination from 'VueBsSimplePagination.vue';
Vue.component('vue-bs-simple-pagination', vueBsSimplePagination);
```

### 3. 사용방법

```html
<vue-bs-simple-pagination
		:current-page="{CURRENT_PAGE_NUM}"
  	:last-page="{LAST_PAGE_NUM}"
  	:base-path="{BASE_PATH}"
  	:query-page-name="page"
    :num-of-elements="10">
</vue-bs-simple-pagination>
```

props의 정보는 아래와 같습니다.

- current-page: 현재 페이지 번호입니다.
- last-page: Pagination의 마지막 페이지 번호 입니다.
- base-path: Pagination의 page 번호를 제외한 URL 입니다.
- query-page-name: page 번호를 저장할 query string의 param 이름입니다. 기본 값은 page 입니다.
  - ex) query-page-name이 'page'이고 base-path가 `http://lorem.ipsum`이며 현재 페이지 번호가 3인 경우 아래와 같이 경로가 생성됩니다.
    `http://lorem.ipsum?page=3`
  - current-page가 1인 경우 본 query-page-name 파라미터는 생략됩니다.
- num-of-elements: Pagination에 페이지 번호가 출력될 최대 개수입니다. 기본은 10 입니다.

## LICENSE

MIT

