# ArgoCD Applications

이 디렉토리에는 ArgoCD Application 리소스를 정의합니다.

## 사용법

1. `app-of-apps.yaml`을 ArgoCD에 등록하면 모든 서비스가 자동으로 배포됩니다:
   ```bash
   kubectl apply -f apps/app-of-apps.yaml
   ```

## 파일 구조

- `app-of-apps.yaml` - 모든 서비스를 관리하는 루트 Application
- `frontend.yaml` - Frontend 서비스 Application
- `backend-api.yaml` - Backend API 서비스 Application
- `auth-service.yaml` - Auth 서비스 Application

## 중요

- `repoURL`을 실제 Git 저장소 URL로 변경하세요
- 환경별로 다른 namespace를 사용하려면 각 Application의 destination.namespace를 수정하세요
