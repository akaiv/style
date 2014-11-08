# akaiv/style

## 개요
* 웹프로젝트 스타일링을 돕는 [LESS](http://lesscss.org) 파일들입니다.
* [아카이브](http://akaiv.com)에서 작성하는 모든 프로젝트에 이 라이브러리가 사용됩니다.
* [아카이브 연구소](http://akaivlabs.com)의 [심철환](http://simcheolwhan.com)이 작성했습니다.

## 시작
- 이 저장소를 프로젝트의 서브모듈로 추가합니다.
```
git submodule add https://github.com/akaiv/style.git
```
- LESS 파일에서 서브모듈을 포함시킵니다. 단, [부트스트랩](http://getbootstrap.com)과 같은 프레임워크를 사용중이라면 그보다 뒤에서 선언합니다.
```
@style-path: "../style";
@import "@{style-path}/akaiv/akaiv";
```

## 내용
```
style/
├── akaiv/
│   ├── mixins
│   ├── _layout.less
│   ├── _mixin.less
│   ├── _variables.less
│   ├── akaiv.less
│   ├── classes.less
│   └── color.less
├── font-awesome/
└── wordpress/
    ├── core.less
    ├── entry.less
    ├── icons.less
    └── image.less
```

## 사용법
### 글꼴 크기
```LESS
.font-size(@sizeValue);
.10px() { .font-size(10) }
.11px() { .font-size(11) }
.12px() { .font-size(12) }
.13px() { .font-size(13) }
.14px() { .font-size(14) }
.15px() { .font-size(15) }
.16px() { .font-size(16) }
```

### 글꼴 클래스
```LESS
.serif      // serif
.strong     // font-weight: 700
.fwn        // font-weight: 400
.underline  // text-decoration
.lowercase  // text-transform
.uppercase  // text-transform
.capitalize // text-transform
```

### 링크 색상
```LESS
// @value에 따라 마우스오버 색상 설정
// @value: 10%   → @color를 10% 어둡게
// @value: color → @value색상으로
.link(@color;@value);
```

### 테두리
```LESS
.border(@color) { border: 1px solid @color }
.no-border();
.no-radius();
.no-shadow();
.no-underline();
.no-outline();
```

### 배경
```LESS
.background(@size:cover;@posx:center;@posy:center);
```

### 필터
```LESS
.blur(@blur:3px);
```

### 셀렉션
```LESS
.selection(@background);
```

### 텍스트
```LESS
.text-overflow-line-clamp(@line:3)
```

### 컬럼
```LESS
.columns(@colwidth: 250px, @colcount: 0, @colgap: 50px, @columnRuleColor: #EEE, @columnRuleStyle: solid, @columnRuleWidth: 1px)
```

## Copyright and license
Licensed under the [MIT License](//opensource.org/licenses/mit-license.html)
