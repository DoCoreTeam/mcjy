# 🚀 Netlify 배포 가이드

## 배포할 파일 목록

build/ 폴더의 모든 파일을 Netlify에 업로드하세요:

✅ index.html         - 메인 페이지
✅ content.json       - 컨텐츠 데이터
✅ images/            - 이미지 파일들
✅ videos/            - 영상 파일들 (있는 경우)
✅ _redirects         - Netlify 설정

## Netlify 배포 방법

### 방법 1: Netlify 웹사이트에서 드래그 앤 드롭
1. https://app.netlify.com 로그인
2. "Add new site" > "Deploy manually" 클릭
3. build/ 폴더를 드래그 앤 드롭

### 방법 2: Netlify CLI
```bash
npm install -g netlify-cli
netlify login
cd build
netlify deploy --prod
```

## 컨텐츠 수정 시

1. 로컬에서 어드민 페이지 실행:
   ```bash
   npm run dev
   ```

2. http://localhost:3000/admin.html 에서 컨텐츠 수정

3. 수정 완료 후 다시 빌드:
   ```bash
   node build-static.js
   ```

4. build/ 폴더를 다시 Netlify에 배포

## 주의사항

⚠️ 이미지나 영상 파일을 변경한 경우:
   - images/ 또는 videos/ 폴더의 파일이 자동으로 포함됩니다
   - 파일 크기가 클 경우 배포 시간이 길어질 수 있습니다

⚠️ 매번 배포 시 전체 파일을 다시 업로드해야 합니다

---

빌드 완료 시간: 2025. 10. 26. 오후 8:15:52
