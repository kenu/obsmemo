AI 지원 코딩의 냉혹한 진실

---
너무 잘 정리된 글이라 공유합니다.

숙련된 개발자와 초급 개발자 간의 AI 활용 차이 <-- 이게 AI가 있어도, 줘도 못 먹는 경우가 있기는 합니다.

---

▲
# GN⁺: 70% 문제: AI 지원 코딩의 냉혹한 진실

https://addyo.substack.com/p/the-70-problem-hard-truths-about (addyo.substack.com)

23P by [neo](https://news.hada.io/user?id=neo) 4일전 | favorite | [댓글 12개](https://news.hada.io/topic?id=18131)

- 개발자들이 AI를 활용하는 두 가지 주요 패턴이 있음
    - **부트스트래퍼**:
        - Bolt, v0, screenshot-to-code AI 같은 도구를 사용하여 빠르게 초기 프로토타입을 생성함.
        - 디자인이나 개념을 시작점으로 AI를 활용하여 초기 코드베이스를 생성하고, 몇 시간 또는 며칠 만에 작동하는 프로토타입을 개발함
    - **이터레이터**:
        - Cursor, Cline, Copilot, WindSurf 같은 도구를 일상 개발에 사용하여 코드 완성, 복잡한 리팩토링, 테스트 및 문서 생성을 수행함

## 숙련된 개발자와 초급 개발자 간의 AI 활용 차이

- **숙련된 개발자**: AI가 제안한 코드를 지속적으로 리팩토링하고, 에지 케이스를 처리하며, 타입 정의를 강화하고, 아키텍처 결정을 검토함
- **초급 개발자**: AI의 출력을 그대로 수용하는 경향이 있어, 실제 환경에서 문제가 발생할 수 있는 '카드로 만든 집'과 같은 코드를 생성할 위험이 있음

## AI 도구의 역설: 지식의 역설

- **숙련된 개발자**: 이미 알고 있는 작업을 AI를 통해 가속화함
- **초급 개발자**: 무엇을 해야 할지 배우기 위해 AI를 사용하려 함
- **결과**: 숙련도에 따라 AI 활용의 효과가 크게 달라짐

## 비전문가의 AI 코딩 도구 사용 시 70% 문제

- **초기 진행**: AI 도구를 사용하여 원하는 기능의 70%를 빠르게 구현할 수 있음
- **남은 30%**: 작은 버그를 수정하려 할 때 새로운 문제가 발생하며, 이를 해결하려다 더 많은 문제가 생기는 악순환에 빠질 수 있음

## AI 도구를 효과적으로 활용하기 위한 전략

- **AI 초안 패턴**: AI로 기본 구현을 생성하고 수동으로 검토 및 리팩토링함
- **AI를 학습 도구로 활용**: 지속적인 대화로 AI가 생성한 코드를 이해하고, 기본적인 프로그래밍 개념을 함께 학습하며, 점진적으로 지식을 쌓아감
- **AI의 한계 인식**: AI 도구는 프로토타입 개발, 학습 보조, 아이디어 검증에는 유용하지만, 생산 준비가 된 유지 보수 가능한 소프트웨어를 개발하려면 여전히 실제 엔지니어링 지식이 필요함

## 에이전틱(Agentic) 소프트웨어 엔지니어링의 부상

- **에이전틱 시스템**: 명령에 응답하는 것을 넘어, 계획하고 실행하며 반복할 수 있는 시스템으로 발전하고 있음
- **미래 전망**: AI는 개발자를 대체하는 것이 아니라, 점점 더 능동적인 협력자로서 인간의 지침과 전문성을 존중하며 주도적으로 문제를 해결하는 방향으로 나아가고 있음
- AI는 이미 알고 있는 패턴을 구현하는 데 도움을 주고, 아이디어를 빠르게 프로토타입하고 다양한 접근 방식을 탐색하는 데 유용함
- 반복적이고 일상적인 코딩 작업을 자동화하여 더 흥미로운 문제에 집중할 수 있게 함

## AI 도구 사용 시 주의사항

- **사용자 경험의 중요성**: AI를 활용하여 빠르게 데모를 만들 수 있지만, 실제 사용자가 사용할 때 발생할 수 있는 에러 메시지, 에지 케이스, UI 상태 등을 세심하게 다루지 않으면 사용자에게 불편을 줄 수 있음
- **장인 정신의 부활**:
    - AI가 소프트웨어 개발을 빠르게 만들었지만, 진정한 소비자 품질의 경험을 만드는 예술을 잃을 위험이 있음.
    - AI 도구는 일상적인 코딩 작업을 처리하여 개발자가 중요한 세부 사항에 집중할 수 있도록 도와줄 수 있음.

## 결론

- **AI의 역할**:
    - AI는 더 많은 코드를 빠르게 작성하는 것이 아니라, 더 나은 소프트웨어를 구축하는 데 도움을 줌
    - AI는 소프트웨어 품질을 극적으로 향상시키지 않음.
- 소프트웨어 개발의 어려운 부분은 여전히 인간의 판단이 필요함.
- AI는 더 나은 솔루션을 찾기 위한 빠른 탐색을 가능하게 하지만, 좋은 소프트웨어 관행을 대체할 수는 없음.
- **인간의 책임**: AI를 현명하게 사용하여 엔지니어링 원칙을 유지하고, 소프트웨어 품질을 향상시키는 것은 여전히 인간의 몫임

---

몇 일 전에 React.js 19버전이 발표되었습니다.

---

## 명명 규칙

### [컴포넌트](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#components)

React 컴포넌트에 설명적이고 의미 있는 이름을 사용하세요. 
컴포넌트 이름에는 **PascalCase** (각 단어의 첫 글자를 대문자로 표기)를 사용하세요.

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fw2ehvyqfs9ixkektwsws.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fw2ehvyqfs9ixkektwsws.png)

---

### [파일](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#files)

**PascalCase를** 사용하여 파일 이름을 지정 하고 구성 요소 이름과 일치시킵니다. 예를 들어, UserCard라는 이름의 구성 요소가 있는 경우 파일 이름은 UserCard.js여야 합니다.

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fnixrtb1zy56bdlnfr1mq.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fnixrtb1zy56bdlnfr1mq.png)

---

### [Props](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#props)

Props에 대한 설명적 이름을 사용하여 목적을 명확히 나타내세요. 프로젝트 맥락에서 널리 이해되지 않는 한 약어나 두문자어는 피하세요.

_예를 들어:_

- usr 대신 user를 사용하세요.

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F0ghet9pry2aw6dv7tmec.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F0ghet9pry2aw6dv7tmec.png)

이 예에서 prop user는 사용자 데이터를 UserCard 구성 요소로 전달하는 데 사용됩니다. user와 같은 설명적 이름을 사용하면 prop이 사용자 데이터를 나타내므로 코드를 더 읽기 쉽고 이해하기 쉽게 만듭니다.

예전에는 8.3 이라고 파일명 8, 확장자 3인 시대도 있었습니다.
하지만, 지금은 달라졌습니다.

---

### [상태 변수](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#state-variables)

부울 값을 나타내려면 상태 변수에 **is** , **has** , **should 접두사를 붙입니다.**

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F2zxl87qe134uyji36f0a.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F2zxl87qe134uyji36f0a.png)

_이 예에서는 세 개의 상태 변수가 있습니다._

- isActive
- hasError
- shouldRender

이러한 변수는 명명 규칙에 따라 각각 **is** , **has** , **should라는** 접두사가 붙습니다 .

해당 상태 업데이트 함수인 **setIsActive** , **setHasError** 및 **setShouldRender는** 상태를 수정하는 데 사용됩니다.

명명 규칙을 따르면 이러한 상태 변수의 목적과 의미가 명확해지고, 코드의 가독성과 유지 관리가 더 좋아집니다.

---

### [이벤트 핸들러](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#event-handlers)

이벤트 핸들러 함수의 접두사로 **handle을** 사용합니다 . 예를 들어, handleClick, handleInputChange.

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fn1zz8630vpib8ivg043h.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fn1zz8630vpib8ivg043h.png)

---

### [CSS 클래스](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#css-classes)

CSS 클래스 이름에는 **소문자** 와 **하이픈을** 사용하세요 .

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Furp5dsu71q3bvtvw1xnr.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Furp5dsu71q3bvtvw1xnr.png)

---

### [상수](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#constants)

**JavaScript에서 상수를 나타내려면 대문자와 밑줄을** 사용합니다 .

_예를 들어, API_URL, MAX_RESULTS._

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fn2hpxeqjyneqe9z84o18.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fn2hpxeqjyneqe9z84o18.png)

---

### [유틸리티 기능](https://dev.to/kristiyan_velkov/react-js-naming-convention-lcg#utility-functions)

목적이나 기능을 나타내는 설명적인 이름을 선택하세요.

_예를 들어, formatDate, generateUniqueId._

[![이미지 설명](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F1szgazv0lh79o2trfo72.png)](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F1szgazv0lh79o2trfo72.png)

---

기억하세요, 명명 규칙의 가장 중요한 측면은 프로젝트나 팀 내의 일관성입니다. 

---

오늘은 여기까지입니다.
시청 감사합니다.
🙇🏻‍♂️

---
아, 하나 더요.
https://sora.com
