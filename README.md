# Whipped F4 🧁✨

**Whipped F4**는 사용자들이 일반 제품 및 맞춤형 DIY 제품을 장바구니에 담고, 구매할 수 있는 웹 애플리케이션입니다. 실시간 업데이트와 페이지 간 매끄러운 전환을 제공하여 사용자의 쇼핑 경험을 최적화했습니다.

---

## 목차
1. [주요 기능](#주요-기능)
2. [데모](#데모)
3. [사용된 기술](#사용된-기술)
4. [설치 방법](#설치-방법)
5. [사용법](#사용법)
6. [API 엔드포인트](#api-엔드포인트)
7. [폴더 구조](#폴더-구조)
8. [기여 방법](#기여-방법)
9. [라이선스](#라이선스)

---

## 주요 기능 🛠️
- 🛒 **장바구니 관리**: 장바구니에 제품을 추가, 삭제하고 실시간으로 업데이트.
- 🎨 **제품 맞춤 옵션**: DIY 제품에 대한 크기, 색상 등 맞춤 설정 가능.
- 💳 **구매 과정**: 결제 정보 입력과 함께 구매 완료.
- 🌐 **반응형 디자인**: 모바일, 태블릿 친화적인 인터페이스.
- 🏷️ **제품 관리**: 제품 상세 정보 확인, 수량 및 크기 선택 가능.
- 🛠️ **Redux 통합**: 장바구니 상태 관리를 위한 중앙 집중식 상태 관리.
- 🔄 **라우팅**: `React Router`를 이용한 동적 라우팅으로 페이지 간 매끄러운 전환.

---

## 데모 🎥
[라이브 데모](https://c.hyee34.site)  
*참고: 라우트가 정상 작동하지 않을 경우, 새로고침을 해주세요.*

---

## 사용된 기술 🛠️
- **프론트엔드**: React (Hooks, Context API, React Router 사용)
- **백엔드**: Node.js, Express
- **데이터베이스**: MongoDB
- **상태 관리**: Redux Toolkit
- **스타일링**: CSS Modules, Styled Components
- **API 통신**: Axios
- **버전 관리**: Git, GitHub
- **배포**: AWS EC2, S3

---

## 설치 방법 ⚙️

### 사전 준비
- Node.js (버전 14.x 이상)
- MongoDB (데이터베이스)

### 설치 단계
1. **레포지토리 클론**:
    ```bash
    git clone https://github.com/hyeyeon-34/whipped_f4.git
    cd whipped_f4
    ```

2. **필수 패키지 설치**:
    ```bash
    npm install
    ```

3. **환경 변수 설정**:
   - 루트 디렉토리에 `.env` 파일을 생성하세요.
   - MongoDB 연결 문자열 및 API 키 등 필요한 환경 변수를 추가하세요:
     ```bash
     MONGO_URI=your_mongodb_connection_string
     PORT=8080
     ```

4. **애플리케이션 실행**:
    ```bash
    npm run dev
    ```

5. **애플리케이션 접속**:
   - 브라우저에서 `http://localhost:3000`으로 접속하세요.

---

## 사용법 🖥️

1. **장바구니에 제품 추가**:
   - 제품 페이지로 이동하세요.
   - 수량, 크기 또는 맞춤 옵션(DIY 제품의 경우)을 선택하세요.
   - "장바구니에 추가" 버튼을 클릭해 장바구니 상태를 실시간으로 업데이트하세요.

2. **장바구니 관리**:
   - 장바구니 아이콘을 클릭해 현재 장바구니 상태를 확인하세요.
   - 장바구니에서 아이템을 제거하거나 수량을 수정할 수 있습니다.

3. **구매하기**:
   - 장바구니 내용을 확인한 후 "구매하기" 버튼을 눌러 결제 페이지로 이동하세요.
   - 배송 정보 및 결제 정보를 입력해 주문을 완료하세요.

---

## API 엔드포인트 🛠️

### 장바구니 관리
- **`GET /get_cart/:userId`**: 주어진 사용자 ID에 해당하는 장바구니를 가져옵니다.
- **`POST /add_to_cart`**: 장바구니에 아이템을 추가합니다.
  - 요청 본문 예시:
    ```json
    {
      "userId": "1234",
      "productId": "5678",
      "quantity": 2,
      "customizations": {
        "size": "M",
        "color": "red"
      }
    }
    ```
- **`DELETE /delete_item`**: 장바구니에서 아이템을 제거합니다.
  - 요청 본문 예시:
    ```json
    {
      "cartItemId": "9876"
    }
    ```

### DIY 제품 커스터마이징
- **`GET /get_diy_details/:cartItemId`**: 맞춤형 DIY 제품에 대한 상세 정보를 가져옵니다.

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


## 🛠️ 에러 및 문제 해결
### 🚨 Uncaught SyntaxError: Unexpected token <
- 문제: 페이지를 새로고침할 때 404 에러가 발생하며, Uncaught SyntaxError: Unexpected token < 에러가 표시됩니다. 이 에러는 JavaScript 파일을 로드할 때 HTML 파일이 반환되어 < 기호를 JavaScript 문법으로 인식하지 못하는 경우 발생합니다.
- 해결 방법: index.html에 <base href='/' /> 태그를 추가하여 브라우저가 모든 상대 경로를 루트 디렉토리를 기준으로 해석하도록 설정했습니다.

### 🌐 404 에러 발생
- 문제: 페이지를 새로고침할 때 404 에러가 발생합니다. 이는 서버가 JavaScript 파일 대신 HTML 파일을 반환하는 경우 발생할 수 있습니다.
- 해결 방법: Nginx 또는 다른 웹 서버 설정에서 모든 경로 요청에 대해 index.html을 반환하도록 설정하여 클라이언트 사이드 라우팅이 제대로 작동하도록 합니다.





### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
