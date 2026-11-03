# ⚔️ 나이트 서바이버 (Night Survivors) 공식 웹사이트 & 게임

모바일 터치 조이스틱과 PC 키보드를 모두 지원하는 웹 기반 로그라이트 서바이벌 게임 및 공식 포털 웹사이트입니다.

## 🚀 게임이 수정/패치될 때마다 자동으로 배포되는 방법 (CI/CD)

이 저장소에는 GitHub Actions 자동 배포 파이프라인(`.github/workflows/deploy.yml`)이 사전 구성되어 있어, **코드를 수정하고 `git push`할 때마다 30초 내로 라이브 웹사이트에 자동 반영**됩니다.

### 1. GitHub Pages로 무료 호스팅하기 (권장)
1. GitHub에서 새로운 저장소(Repository)를 만듭니다 (예: `night-survivors`).
2. 이 폴더의 파일들을 저장소의 `main` 브랜치에 업로드합니다:
   ```bash
   git init
   git add .
   git commit -m "feat: Night Survivors v2.1.2 official release"
   git branch -M main
   git remote add origin https://github.com/당신의아이디/night-survivors.git
   git push -u origin main
   ```
3. GitHub 저장소 상단 **Settings → Pages** 메뉴로 이동합니다.
4. **Build and deployment > Source**를 `Deploy from a branch` 대신 **`GitHub Actions`**로 선택합니다.
5. 이후에는 게임이나 웹사이트 코드를 수정하고 `git push`할 때마다 자동으로 최신 버전이 빌드되어 실시간 웹사이트 주소(`https://당신의아이디.github.io/night-survivors/`)에 자동 배포됩니다!

### 2. Vercel / Netlify로 1초 연동하기
- [Vercel](https://vercel.com) 또는 [Netlify](https://netlify.com)에 로그인 후 해당 GitHub 저장소를 `Import`하기만 하면, 별도의 서버 설정 없이 `git push` 때마다 무중단 자동 배포가 이루어집니다.

---

## 🎮 주요 게임 시스템
- **자동 조준 사격 & 모바일 가상 조이스틱:** 이동만 하면 사거리 내 적을 100% 자동 공격
- **3택 1 레벨업 시스템:** 적을 처치하고 보석을 모아 레벨업할 때마다 세 가지 축복 중 하나를 선택
- **10레벨 초월 진화 조합:**
  - ⚡ 천벌의 낙뢰 Lv.10 + 🔥 화염 파동 Lv.10 = **⚡🔥 뇌화겁화 (지속 불장판)**
  - 🗡️ 회전 성검 Lv.10 + 🛡️ 신성 결계 Lv.10 = **🗡️🛡️ 성스러운 심판의 폭풍 (연쇄 심판 폭발)**
  - 🔹 마법 탄환 Lv.10 + 🔪 암살자 단검 Lv.10 = **🔪🔹 환영 비검술 (초고속 관통 검기)**
- **4가지 영웅 클래스:** 성기사(아서), 아크메이지(루나), 번개술사(카이), 암살자(쉐도우)
- **시간대별 7종 몬스터 & 4단계 엘리트 보스:** 시간이 지날수록 새로운 적 군단과 보스 등장
