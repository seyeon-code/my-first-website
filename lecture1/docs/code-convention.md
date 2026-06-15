# Code Convention

## 파일 및 폴더 명명 규칙

### 컴포넌트 파일
- PascalCase 사용: `MyComponent.jsx`
- 폴더명: kebab-case 또는 camelCase

### 일반 파일
- camelCase 사용: `apiService.js`, `useAuth.js`
- 상수 파일: SCREAMING_SNAKE_CASE

## 컴포넌트 작성 규칙

### 함수형 컴포넌트 사용
```jsx
const MyComponent = ({ prop1, prop2 }) => {
  return <div>{prop1}</div>;
};

export default MyComponent;
```

### Props 구조분해 할당 필수
```jsx
// ✅ 올바른 방법
const Button = ({ label, onClick, variant = 'contained' }) => { ... }

// ❌ 잘못된 방법
const Button = (props) => { const { label } = props; ... }
```

## Import 순서
1. React 관련 (react, react-dom)
2. 외부 라이브러리 (MUI, router 등)
3. 내부 컴포넌트
4. 유틸리티/훅
5. 스타일/CSS

## 상태 관리
- useState: 로컬 상태
- useEffect: 사이드 이펙트
- useCallback: 함수 메모이제이션
- useMemo: 값 메모이제이션

## 네이밍 컨벤션
- 핸들러: `handle` 접두사 (handleClick, handleSubmit)
- 훅: `use` 접두사 (useAuth, useFetch)
- 상수: UPPER_CASE
- Boolean: `is`, `has`, `can` 접두사
