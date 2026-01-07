# 💀 GHOST HUB - AI 블로그 자동화 시스템

매번 다른 페르소나와 구조로 AI 흔적을 완벽히 숨기는 블로그 콘텐츠 생성기

## 🎯 주요 기능

### 🟢 네이버 수익형 (FOMO 극대화)
- **페르소나 5개 랜덤**: 30대 워킹맘, 20대 직장인, 40대 전문가 등
- **구조 5가지 랜덤**: 스토리텔링형, 데이터 분석형, 비교 대결형 등
- **FOMO 마케팅**: 손해/긴급성/후회 자극 문구 자동 생성
- **CTA 2개 자동 삽입**: 구매 유도 최적 위치
- **나눔고딕 15px, 소제목 19px**: 네이버 최적화

### 🟢 네이버 정보성 (전문 칼럼)
- **체크리스트 자동 생성**: 핵심 정보 요약
- **Q&A 3~5개**: 독자 궁금증 해결
- **속성표 자동 생성**: 정보 정리 테이블
- **전문가 페르소나 3개**: 칼럼니스트, 큐레이터, 업계 전문가

### 🟠 티스토리 정보성 (주제 집중)
- **주제 이탈 방지**: 관련 없는 경제/투자 이야기 차단
- **글자수 제한**: 1800~2400자로 최적화
- **화려한 HTML**: 그라데이션, 색상 자유
- **페르소나 3개**: 트렌드 분석가, 큐레이터, 전문가

### 🟠 티스토리 수익형
- 기존 t정보.py 파일 사용
- 애니메이션 CTA, 깜빡이는 효과

---

## 📋 목차

- [설치 방법](#설치-방법)
- [실행 방법](#실행-방법)
- [사용 방법](#사용-방법)
- [환경 변수 설정](#환경-변수-설정)
- [트러블슈팅](#트러블슈팅)
- [라이선스](#라이선스)

---

## 🚀 설치 방법

### 1. 저장소 클론

```bash
git clone https://github.com/YOUR_USERNAME/ghost-hub.git
cd ghost-hub
```

### 2. Python 가상환경 생성 (권장)

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**Mac/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. 필요한 패키지 설치

```bash
pip install -r requirements.txt
```

### 4. 환경 변수 설정

`.env` 파일을 프로젝트 루트에 생성:

```env
GEMINI_API_KEY=your_api_key_here
```

> **API 키 발급 방법**: [Google AI Studio](https://makersuite.google.com/app/apikey)에서 무료로 발급 가능

---

## ▶️ 실행 방법

### 방법 1: 기본 실행

```bash
streamlit run GHOST_HUB_FINAL.py
```

### 방법 2: 포트 지정 실행

```bash
streamlit run GHOST_HUB_FINAL.py --server.port 8501
```

### 방법 3: 브라우저 자동 열기 끄기

```bash
streamlit run GHOST_HUB_FINAL.py --server.headless true
```

**실행 후 브라우저에서 자동으로 열립니다:**
```
http://localhost:8501
```

---

## 📖 사용 방법

### 1️⃣ 모드 선택
왼쪽 사이드바에서 원하는 모드 선택:
- 🟢 네이버 수익형 (FOMO)
- 🟢 네이버 정보성 (체크리스트)
- 🟠 티스토리 정보성 (주제집중)
- 🟠 티스토리 수익형 (기존파일)

### 2️⃣ 정보 입력

**네이버 수익형:**
- 키워드: 무선 청소기 추천
- 상품명: 다이슨 V15
- 제휴 링크: https://link.coupang.com/...

**네이버/티스토리 정보성:**
- 키워드: 건강보험 환급 방법

### 3️⃣ 생성 버튼 클릭
- AI가 페르소나와 구조를 랜덤 선택
- 1800~2400자 원고 자동 생성
- 실시간 정보 수집 및 반영

### 4️⃣ 복사 및 붙여넣기

**네이버:**
1. "네이버 블로그 서식 포함 복사" 버튼 클릭
2. 네이버 블로그 에디터에서 Ctrl+V
3. 서식 그대로 적용됨

**티스토리:**
1. "티스토리 HTML 복사" 버튼 클릭
2. 티스토리 글쓰기 → HTML 모드로 전환
3. Ctrl+V로 붙여넣기

---

## 🔧 환경 변수 설정

### .env 파일 생성

프로젝트 루트 디렉토리에 `.env` 파일 생성:

```env
# Google Gemini API Key (필수)
GEMINI_API_KEY=AIzaSyXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

### API 키 발급 방법

1. [Google AI Studio](https://makersuite.google.com/app/apikey) 접속
2. "Get API Key" 클릭
3. 프로젝트 선택 또는 생성
4. API 키 복사
5. `.env` 파일에 붙여넣기

### API 사용량 및 한도

**무료 티어:**
- 분당 15회 요청
- 하루 1,500회 요청
- 분당 100만 토큰

**비용 (유료 사용 시):**
- 1개 글 생성: 약 1원
- 100개: 약 100원
- 1,000개: 약 1,000원

---

## 📦 requirements.txt

```txt
streamlit==1.28.0
google-generativeai==0.3.0
python-dotenv==1.0.0
duckduckgo-search==3.9.0
```

---

## 🛠️ 트러블슈팅

### 문제 1: API 키 오류
```
🚨 GEMINI_API_KEY를 .env 파일에서 찾을 수 없습니다.
```

**해결:**
1. `.env` 파일이 프로젝트 루트에 있는지 확인
2. `GEMINI_API_KEY=your_key` 형식이 맞는지 확인
3. 따옴표 없이 작성했는지 확인

### 문제 2: 모듈을 찾을 수 없음
```
ModuleNotFoundError: No module named 'streamlit'
```

**해결:**
```bash
pip install -r requirements.txt
```

### 문제 3: 포트가 이미 사용 중
```
OSError: [Errno 98] Address already in use
```

**해결:**
```bash
# 다른 포트 사용
streamlit run GHOST_HUB_FINAL.py --server.port 8502
```

### 문제 4: 한글 깨짐
```
UnicodeDecodeError
```

**해결:**
- 파일이 UTF-8로 저장되어 있는지 확인
- 코드 내 인코딩 설정이 되어 있음 (자동 해결)

### 문제 5: Rate Limit 초과
```
429 Error: Too Many Requests
```

**해결:**
- 무료 티어: 분당 15회 제한
- 60초 대기 후 재시도
- 유료 티어로 업그레이드 검토

---

## 📊 프로젝트 구조

```
ghost-hub/
├── GHOST_HUB_FINAL.py    # 메인 통합 파일
├── .env                   # 환경 변수 (직접 생성)
├── requirements.txt       # 패키지 목록
├── README.md             # 이 파일
└── .gitignore            # Git 무시 파일
```

---

## 🎨 기능별 상세 설명

### 페르소나 시스템
매번 다른 캐릭터로 글을 작성:
- 30대 워킹맘: "진짜 좋더라고요 👍"
- 20대 직장인: "가성비 미쳤음 🔥"
- 40대 전문가: "검증된 제품입니다 ✅"

### 구조 랜덤화
5가지 서사 구조 자동 변경:
- 스토리텔링형: 경험담 → 문제 → 해결
- 데이터 분석형: 수치 → 비교 → 평가
- 비교 대결형: A vs B → 승자
- 폭로 고발형: 충격 → 진실 → 대안
- Q&A 해결형: 질문 → 답변 → 정리

### AI 감지 회피
41개 금지어 자동 필터링:
- ❌ "안녕하세요", "오늘은"
- ❌ "저는", "블로거입니다"
- ❌ "결론", "마무리"
- ❌ "쿠팡", 날짜 표기

---

## 🔒 보안 주의사항

### .gitignore에 반드시 추가:
```gitignore
.env
__pycache__/
*.pyc
venv/
.DS_Store
```

### API 키 보호:
- ⚠️ API 키를 절대 GitHub에 업로드하지 마세요
- ⚠️ 공개 저장소에서 .env 파일 공유 금지
- ✅ 각자 로컬에서 .env 파일 생성

---

## 📈 성능 최적화 팁

### 1. 배치 생성
```python
# 여러 개 생성 시
keywords = ["키워드1", "키워드2", "키워드3"]
for kw in keywords:
    # 생성 로직
    time.sleep(5)  # 5초 간격
```

### 2. 에러 핸들링
- Rate Limit 발생 시 60초 대기
- 실패 시 자동 재시도 (최대 3회)

### 3. 로그 저장
- 생성된 콘텐츠를 로컬에 저장
- 히스토리 관리

---

## ❓ FAQ

**Q: 무료로 사용할 수 있나요?**
A: 네, Google Gemini API 무료 티어로 하루 1,500개 글 생성 가능합니다.

**Q: 네이버와 티스토리 차이는?**
A: 네이버는 HTML 제한적 (나눔고딕, 배경색 금지), 티스토리는 완전 자유입니다.

**Q: 상업적 이용 가능한가요?**
A: 네, MIT 라이선스로 자유롭게 사용 가능합니다.

**Q: 글자수가 항상 1800~2400자인가요?**
A: 네, 프롬프트에 엄격히 제한되어 있습니다.

**Q: 다른 AI 모델 사용 가능한가요?**
A: 현재는 Gemini 3.0 Flash만 지원합니다. 다른 모델은 코드 수정 필요합니다.

---

## 🤝 기여 방법

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 라이선스

MIT License - 자유롭게 사용, 수정, 배포 가능

---

## 📞 문의

- Issues: [GitHub Issues](https://github.com/YOUR_USERNAME/ghost-hub/issues)
- Email: your.email@example.com

---

## 🙏 감사의 말

- Google Gemini API
- Streamlit
- DuckDuckGo Search

---

## 📅 업데이트 내역

### v1.0.0 (2025-01-07)
- 🎉 초기 릴리즈
- 🟢 네이버 수익형/정보성 모드
- 🟠 티스토리 정보성 (주제 이탈 방지)
- 💀 페르소나 시스템
- 🔥 FOMO 극대화

---

**⭐ 별표 눌러주시면 개발에 큰 힘이 됩니다!**
