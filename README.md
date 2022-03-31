    #안녕하세요! react파트에 지원한 김성현(shkim787) 입니다.

## Prography 7th React Quest

> 프로그라피 React 전형의 비중은 면접(70%), 과제(30%) 입니다. 과제의 완성도보다 면접이 더 중요합니다.

## 1. 개요

프로그라피는 짧은 기간동안 멋진 서비스를 뚝딱 만들어내기 때문에 웹 클라이언트 개발 능력이 굉장히 중요합니다. 프로그라피 활동에 필요한 클라이언트 개발 능력 확인하기 위해 사전과제를 진행하고 있습니다. 사전과제에서는 간단한 기획과 요구사항에 맞춰 기능을 구현할 수 있는 지를 확인합니다.

더 궁금한 것이 있으시면 [해당 프로젝트 이슈](https://github.com/prography/prography-7th-react-quest/issues/new)로 남겨주세요! 늦어도 당일 이내에 답변을 남기도록 하겠습니다.

## 2. 과제

아래의 `a.기획`, `b.요구사항(필수)` 그리고 `c.요구사항(선택)`을 잘 읽고 적절한 웹 프로그램을 구현해주시기 바랍니다. 리액트 사용은 필수이며, 이외의 라이브러리 사용은 제한이 없습니다.

> 과제는 요구사항 선택을 포함하여 **10시간**을 목표로 작성되었습니다.

**과제는 해당 Repository를 fork하여 진행합니다.**

### a. 기획

할 일(Todo) 관리 프로그램(이하 "투두리스트")을 제작합니다. 투두리스트가 무엇인지 궁금하다면 [TodoMVC](https://todomvc.com/examples/react/#/)를 확인해주세요.

투두리스트는 할 일을 등록하고 수정/삭제 할 수 있으며, 각 할 일에 태그를 등록하여 관리 할 수 있습니다.

투두리스트에서 관리해야하는 데이터는 아래와 같습니다.

- **할 일**
  - 제목
  - 상세설명
  - 태그
  - 생성일
  - 수정일
  - 마감목표일
  - 완료일
  - 완료여부

- **태그**
  - 이름
  - 글자 색상
  - 배경 색상
  - 생성일
  
### b. 요구사항(필수)

**할 일**
- [x] 할 일 입력 폼에는 제목, 상세설명, 태그, 마감 목표일을 입력할 수 있습니다.
- [x] 마감 목표일은 달력 UI를 이용합니다.
- [x] 입력폼에서 "제출하기" 버튼을 누르면 목록에서 추가된 할 일을 확인할 수 있습니다.
- [x] 목록에서 바로 체크박스를 누르면 완료여부를 체크할 수 있습니다.
- [x] 목록에서 "수정" 버튼을 누르면 해당 투두를 수정 할 수 있습니다.
- [x] 목록에서 "삭제" 버튼을 누르면 삭제 됩니다.
- [x] 완료한 할 일 목록을 필터하여 볼 수 있습니다.
- [x] 완료한 할 일들은 일괄 삭제가 가능합니다.

**태그**
- [x] 할 일 입력 폼에서 태그를 여러개 입력할 수 있습니다.
- [x] 같은 이름의 태그는 중복입력이 안됩니다.
- [x] 할 일 목록에서 태그는 색상으로 구분되어야 합니다.
- [x] 목록에서 서로 다른 할 일에 같은 태그가 있다면, 같은 색으로 표시됩니다.

### c. 요구사항(선택)

선택 요구 사항은 가산점 항목입니다.

- [x] 입력할 때 validation 처리.
- [x] 입력 중 뒤로가기 또는 브라우저를 닫으려고 할 때 입력된 내용 삭제 알림창.
- [x] 마감일이 3일 이내인 할 일은 긴급함 표시가 보입니다.
- [x] 태그의 색상을 커스텀하게 바꿀 수 있습니다.
- [x] 할 일 삭제시 진짜로 삭제할 것인지 한번 더 물어보고 삭제됩니다.
- [ ] 할 일은 태그별, 완료여부별, 마감 기간, 생성일 기준으로 필터를 할 수 있습니다.
- [x] 브라우저창을 닫았다가 다시 열어도 데이터가 남아있습니다.
- [x] 서비스 배포가 되어 어디서든 접속이 가능할 수 있으면 좋겠어요. (배포 후 API 링크를 아래에 적어주세요) \
배포 URL: https://quest-f4bac.firebaseapp.com/

## 3. 제출방법

fork를 한 뒤 진행하기 때문에 따로 제출은 필요 없으나, 마감일 기준 23:59:59 까지의 커밋까지만 인정됩니다.

## 4. 설명

- 전체적인 디자인은 material-ui를 사용하여 진행하였습니다. 
- 우측 상단의 TODOLIST 추가버튼을 눌러 Modal창을 통해 새로운 '할 일'을 추가할 수 있습니다. 
  - 제목, 추가 설명,마감 목표일, 태그(배경색, 글자색)을 작성할 수 있습니다.
  - material-ui의 달력ui와 시계ui를 사용하여 목표일을 상세하게 지정할 수 있습니다.
  - 입력할 때의 validation 
    + 제목, 추가 설명 부분은 제재할 형식이 따로 없다고 생각하여 required만 넣었습니다
    + 목표일은 잘못 들어가는 것을 막기위해 ui통해 입력하는 것만 가능하도록 하였습니다
    + 태그는 최대 5글자, 5개만 들어가도록 하였고, 같은 이름이 들어가는 것 또한 방지하였습니다.
    + 태그는 서로 다른 할 일에 같은 이름의 태그가 입력된다면 기존의 태그와 같은 색으로 표시됩니다.
    + 화면 바깥 클릭, 뒤로가기, 닫기, 새로고침 evenet가 감지되면 confirm창이 뜨도록 하였습니다.
- list를 볼 수 있는 화면에서는 우측 상단의 버튼을 통해 '남은시간 순', '생성 순'으로 정렬해 볼 수 있습니다.
- 리스트의 상태는 완료됨, 진행중, 시간초과를 구분됩니다
  - 진행중인 할 일은 파란색으로 표시되며 3일이하로 남게된다면 빨간색으로 표시됩니다.
  - 목표 시간이 초과된 할 일은 빨간색으로 표시됩니다.
  - 완료된 할 일은 회색으로 표시됩니다.
  - 완료된 할 일은 한번에 삭제가 가능합니다.
- 각 리스트 좌측의 체크박스를 통해 완료여부를 즉시 교체할 수 있습니다. 
- 할 일을 누르면 상세 설명과 태그들, 생성일, 목표일, 완료일을 볼 수 있고 수정,삭제 기능을 수핼할 수 있습니다.
  - 상세설명은 띄어쓰기나 줄바꿈이 입력할 때와 같게 보여집니다. 
- 파이어베이스르 사용하여 데이터를 관리하고, 호스팅하였습니다.
    