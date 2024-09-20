# Whipped F4 🧁✨

**Whipped F4**는 사용자들이 일반 제품 및 맞춤형 DIY 제품을 장바구니에 담고, 구매할 수 있는 웹 애플리케이션입니다. 실시간 업데이트와 페이지 간 매끄러운 전환을 제공하여 사용자의 쇼핑 경험을 최적화했습니다.

---

## 주요 기능 🛠️
- 🛒 **장바구니 관리**: 장바구니에 제품을 추가, 삭제하고 실시간으로 업데이트.
- 🎨 **제품 맞춤 옵션**: DIY 제품에 대한 크기, 색상 등 맞춤 설정 가능.
- 💳 **구매 과정**: 결제 정보 입력과 함께 구매 완료.
- 🌐 **반응형 디자인**: 태블릿 친화적인 인터페이스.
- 🏷️ **제품 관리**: 제품 상세 정보 확인, 수량 및 크기 선택 가능.
- 🛠️ **Redux 통합**: 장바구니 상태 관리를 위한 중앙 집중식 상태 관리.
- 🔄 **라우팅**: `React Router`를 이용한 동적 라우팅으로 페이지 간 매끄러운 전환.

---

## 사용된 기술 🛠️
- **프론트엔드**: React 
- **백엔드**: Node.js, Express
- **데이터베이스**: PostgreSql
- **버전 관리**: Git, GitHub
- **배포**: AWS EC2

---

## 설치 방법 ⚙️


### 설치 단계
1. **레포지토리 클론**:
    ```bash
    git clone https://github.com/hyeyeon-34/whipped_f4.git
    cd whipped_f4
    ```

2. **필수 패키지 설치**:
    ```bash
    npm install

3. **애플리케이션 실행**:
    ```bash
    npm run dev
    ```

4. **애플리케이션 접속**:
   - 브라우저에서 `http://localhost:3000`으로 접속하세요.

---

## 에러 및 문제 해결 

### 🛠️ 에러 및 문제 해결
#### 🚨 Uncaught SyntaxError: Unexpected token <
- 문제: 페이지를 새로고침할 때 404 에러가 발생하며, Uncaught SyntaxError: Unexpected token < 에러가 표시됩니다. 이 에러는 JavaScript 파일을 로드할 때 HTML 파일이 반환되어 < 기호를 JavaScript 문법으로 인식하지 못하는 경우 발생합니다.
- 해결 방법: index.html에 <base href='/' /> 태그를 추가하여 브라우저가 모든 상대 경로를 루트 디렉토리를 기준으로 해석하도록 설정했습니다.

#### 🌐 404 에러 발생
- 문제: 페이지를 새로고침할 때 404 에러가 발생합니다. 이는 서버가 JavaScript 파일 대신 HTML 파일을 반환하는 경우 발생할 수 있습니다.
- 해결 방법: Nginx 또는 다른 웹 서버 설정에서 모든 경로 요청에 대해 index.html을 반환하도록 설정하여 클라이언트 사이드 라우팅이 제대로 작동하도록 합니다.

---

## 폴더 구조 📂

```bash
whipped_f4/
├── public/                 # 공개된 파일 및 리소스
├── src/
│   ├── components/         # 재사용 가능한 컴포넌트들 (예: Header, ProductCard)
│   ├── pages/              # 라우트 페이지들 (예: Cart, Checkout)
│   ├── redux/              # Redux 슬라이스와 스토어 설정
│   ├── services/           # API 서비스 호출 (예: Axios 설정)
│   ├── App.js              # 메인 앱 컴포넌트
│   └── index.js            # React 진입점
├── .env                    # 환경 변수 파일
├── package.json            # 프로젝트 메타데이터 및 스크립트
└── README.md               # 현재 문서


