# Devops_Ss12ex1 - CI Matrix (Java Spring Boot Gradle)

Dự án Spring Boot (Gradle) minh họa quy trình CI đa phiên bản JDK sử dụng
**Matrix Strategy** của GitHub Actions.

## CI Matrix

Workflow: [`.github/workflows/ci-matrix.yml`](.github/workflows/ci-matrix.yml)

- Trigger: `push` vào nhánh `main`.
- Job `test-matrix` chạy song song trên **JDK 17** và **JDK 21**.
- `actions/checkout@v5` + `actions/setup-java@v5` (distribution `temurin`, `cache: gradle`).
- Thực thi `./gradlew test` trên từng phiên bản JDK.

## Chạy local

```bash
./gradlew test
```
