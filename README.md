# FastAPI DevOps 배포 프로젝트

이 프로젝트는 Terraform, Ansible, Docker, GitHub Actions를 사용하여 FastAPI 애플리케이션을 AWS EC2 인스턴스에 자동으로 배포합니다.

## ⚙️ 기술 스택
- FastAPI - Python 기반 웹 프레임워크
- Docker - FastAPI 컨테이너화
- Terraform - AWS EC2 인프라 구성
- Ansible - EC2 서버 설정 및 배포 자동화
- GitHub Actions - CI/CD 자동화

## 🗂️ 디렉토리 구조
.
├── .github/workflows/deploy.yml
├── terraform/
├── ansible/
├── app/
├── requirements.txt
└── README.md

## 🚀 배포 방법
1. GitHub Secrets에 다음 키 등록:
   - AWS_ACCESS_KEY
   - AWS_SECRET_KEY
   - AWS_PRIVATE_KEY (base64 인코딩)
2. main 브랜치에 push하면 자동으로 배포됩니다.
3. 배포 완료 후 EC2 IP를 통해 접속:
   - http://<EC2-IP>:8000/
   - http://<EC2-IP>:8000/docs

## ✅ 결과 예시
GET http://<EC2 IP>:8000/
→ { "message": "Hello from FastAPI!" }

## 📄 라이선스
MIT License
