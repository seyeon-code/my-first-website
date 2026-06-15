# New Project Setup Guide

## 새 프로젝트 시작 체크리스트

### 1. _template_settings에서 복사
```bash
# lecture1 디렉토리에서 실행
cp -r _template_settings my-new-project
cd my-new-project
npm install
```

### 2. 프로젝트 초기화
```bash
# package.json에서 프로젝트명 변경
# vite.config.js 포트 설정 (선택)
npm run dev
```

## 기본 프로젝트 구조
```
my-project/
├── public/
│   └── vite.svg
├── src/
│   ├── components/     # 재사용 컴포넌트
│   │   └── common/     # 공통 컴포넌트
│   ├── pages/          # 페이지 컴포넌트
│   ├── hooks/          # 커스텀 훅
│   ├── utils/          # 유틸리티 함수
│   ├── services/       # API 서비스
│   ├── theme.js        # MUI 테마 설정
│   ├── main.jsx        # 진입점
│   └── App.jsx         # 루트 컴포넌트
├── package.json
└── vite.config.js
```

## React Router 기본 설정
```jsx
// src/App.jsx
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import HomePage from './pages/HomePage';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<HomePage />} />
      </Routes>
    </BrowserRouter>
  );
}

export default App;
```

## MUI 컴포넌트 빠른 참조
- `<Button variant="contained">` - 주요 버튼
- `<TextField label="입력">` - 텍스트 입력
- `<Card>` / `<CardContent>` - 카드 레이아웃
- `<Grid container spacing={2}>` - 그리드 레이아웃
- `<Typography variant="h1">` - 텍스트 스타일
- `<Box sx={{ p: 2 }}>` - 유연한 컨테이너
