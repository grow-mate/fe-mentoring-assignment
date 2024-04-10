# Week 01 - 레벨 테스트

## 구현 목표

- 아래 요구 사항에 따라 회원가입/로그인 기능이 있는 To-do List를 만들어보며 레벨 테스트를 진행합니다.

## 의존성

- TypeScript, React(react, react-dom), react-router-dom, axios를 필수적으로 사용합니다.
- 상태 관리 라이브러리 사용은 선택입니다. (redux, mobx, recoil 등)
- 프로젝트 세팅에 CRA(Create React App)를 사용하지 않습니다.
- 패키지 매니저(npm, yarn, pnpm 등) 사용은 자유입니다.
- 위에 명시한 라이브러리 이외에는 사용이 제한됩니다.

## 요구 사항

> **아래 요구 사항에 따라 구현하되, 명시되어 있지 않은 요구 사항에 대해서는 자유롭게 구현해도 됩니다.**

### 1. 회원가입 페이지 (/sign-up)

- 회원가입 Form에는 아래 항목이 필수적으로 들어갑니다.
  - 이메일
    - 이메일 형식에 맞는 양식(@ 포함)만 허용합니다.
    - 이미 존재하는 이메일로 회원가입을 시도했을 경우, `이미 존재하는 이메일입니다.` 라는 에러 메세지가 나타나며 이메일 입력창이 포커스되어야 합니다.
  - 닉네임
    - 영문 소문자 및 숫자, 언더바(\_)만 가능하며 최소 2자 ~ 최대 10자만 허용합니다.
  - 비밀번호
    - 비밀번호는 영문 소문자 및 숫자를 하나 이상 포함하며 최소 6자 ~ 최대 12자만 허용합니다.
  - 비밀번호 확인
    - 위에서 입력한 비밀번호와 일치하지 않을 경우, `비밀번호가 일치하지 않습니다.` 라는 에러 메세지가 입력창 아래에 보여야 합니다.
- 각 항목의 제한 사항을 통과하지 못했을 경우, 제출 버튼이 비활성화된 상태여야 합니다.
- 로그인 페이지로 이동할 수 있는 버튼이 있어야 합니다.

### 2. 로그인 페이지 (/login)

- 로그인 Form에는 아래 항목이 필수적으로 들어갑니다.
  - 이메일
    - 존재하지 않는 이메일을 제출했을 경우, `존재하지 않는 이메일입니다.` 라는 에러 메세지가 나타나며 이메일 입력창이 포커스되어야 합니다.
  - 비밀번호
    - 비밀번호가 일치하지 않을 경우, `비밀번호가 일치하지 않습니다.` 라는 에러 메세지가 나타나며 비밀번호 입력창으로 포커스되어야 합니다.
- 이메일 또는 비밀번호가 입력되지 않았을 경우, 제출 버튼이 비활성화된 상태여야 합니다.
- 로그인 성공 시, API 응답값에서 access token을 전달 받아 로컬 스토리지에 저장합니다.
- 회원가입 페이지로 이동할 수 있는 버튼이 있어야 합니다.

### 3. Todo List 페이지 (/todo)

- 로그인 되어 있지 않은 경우, 접근이 제한되며 로그인 페이지로 리다이렉트 됩니다.
- 입력창을 통해서 Todo를 생성할 수 있습니다.
  - 생성된 Todo는 목록에 보여야 하며, 수정 및 삭제가 가능합니다.
- Todo에는 다음과 같은 2가지 상태가 존재합니다.
  - 진행 중 (기본값)
  - 완료
    - 완료된 Todo는 텍스트에 취소선이 그어지며, 진행 중인 Todo보다 아래로 정렬되어야 합니다.
- 탭을 통해 각 상태에 해당하는 Todo 목록을 볼 수 있어야 합니다.
  - 탭은 전체, 진행 중, 완료 3가지가 있어야 합니다.
  - 브라우저 새로고침 이후에도 탭 상태가 유지되어야 합니다.

## 참고 자료

- [Simple Login Page UI](<https://www.figma.com/file/hlxPK0mSudqN6Lfbb2LeVP/%F0%9F%92%BB-Simple-Login-Page-UI-(Community)?type=design&node-id=0%3A1&mode=design&t=mt2TkV820L6ctVVh-1s>)
- [Simple To Do List Figma](<https://www.figma.com/file/lJ5fbnWqh2JUdZCWGqKLZk/Simple-To-Do-List-(Community)?type=design&node-id=0%3A1&mode=design&t=H0dkpSF2XXOfvZ8C-1>)