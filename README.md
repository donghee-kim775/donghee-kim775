# DongHee Kim

**Wanna B.E Data Engineer** · `#Infra` `#DataEngineering`

> 흐르는 배움과 깨달음이 끊기지 않도록,<br/>
> 데이터처럼 계속 흐르는 엔지니어

온프레미스 Kubernetes 위에서 데이터 플랫폼을 설치하고 운영해 왔습니다.
파이프라인 코드뿐 아니라 그 아래의 스토리지, 네트워크, CI/CD, 모니터링까지 직접 다룹니다.

**[Portfolio](https://dongheedecv.samteo.org)** · [velog](https://velog.io/@ehdgml775595) · [Notion](https://youthful-yew-08d.notion.site/1965c4826975808bb481c4d60ef19aec) · [ehdgml775595@gmail.com](mailto:ehdgml775595@gmail.com)

---

## <img src="https://api.iconify.design/lucide/user.svg?color=%234a6cc7" width="22" height="22" /> About

- **?에서 !로 나아가는 엔지니어** — '왜?'라는 물음표를 직접 부딪혀 보며 '!'라는 느낌표로 바꿔 가는 과정을 좋아합니다. 장애를 트러블슈팅할 때도, AI가 만든 코드를 적용할 때도 왜 그렇게 동작하는지 이해한 뒤에 넘어갑니다.
- **성장으로 기여하는 엔지니어** — 회사가 풀어야 할 문제를 제 문제로 여기고, 그 과정에서 성장한 역량으로 회사의 가치에 기여하고 싶습니다.

| | |
|:--|:--|
| **Now** | 대구가톨릭대학교 대학원 AI 빅데이터공학과 · T3Q SW Engineer (주임) 겸직 |
| **Side** | Binance 실시간 스트리밍 플랫폼 (진행 중) |
| **Next** | AWS DEA · SAA |


## <img src="https://api.iconify.design/lucide/layers.svg?color=%237465b8" width="22" height="22" /> Tech Stack

| | |
|:--|:--|
| **Streaming** | ![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white) ![Flink](https://img.shields.io/badge/Apache%20Flink-E6526F?style=flat-square&logo=apacheflink&logoColor=white) |
| **Batch · Lakehouse** | ![Spark](https://img.shields.io/badge/Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white) ![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD4?style=flat-square) ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white) |
| **Infra** | ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white) ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white) |
| **CI/CD** | ![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white) ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white) |
| **Monitoring** | ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) |
| **Language** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white) |


## <img src="https://api.iconify.design/lucide/briefcase.svg?color=%234a6cc7" width="22" height="22" /> Career

**T3Q** · SW Engineer (주임) · 대학원 겸직 · `2025.03 – 현재`

| 1차년도 | 2차년도 |
|:--|:--|
| 플랫폼 이관 · 기능 정상화 (회사 서버 → 학교 서버) | HTTPS 적용 (Cert-manager · Cloudflare) |
| Local Disk 의존성 제거 → Kubernetes 위 MinIO | 레거시 쿼리 · 프로시저 최적화 (ERD 분석 · 트랜잭션 · 인덱스) |
| GitLab · Jenkins CI/CD 인프라 구축 및 파이프라인 수립 | 제약 메타데이터 및 실험 데이터 리니지 정립 |
| 레거시 코드 제거 및 유지보수 | IVIVC · 연속 공정 기능 개발 |
| | KOLAS 성적서 인증 준비 및 명세서 작성 |


## <img src="https://api.iconify.design/lucide/rocket.svg?color=%23cf6a61" width="22" height="22" /> Data Engineering Projects

### <img src="https://api.iconify.design/lucide/radio.svg?color=%23cf6a61" width="18" height="18" /> Streaming

**[Binance Real-Time Market Insight Platform](https://github.com/donghee-kim775/binance-project)** `개인 프로젝트` `진행 중` · [Notion](https://youthful-yew-08d.notion.site/Binance-project-3c55c4826975807994bded2381a86c0b)
> Spot과 선물 시장의 가격 괴리(basis)를 실시간으로 잡아내는 스트리밍 플랫폼

- 트래픽 성격에 따라 Active-Active(×2) / Active-Standby 수집 Pod 분리 — WebSocket 재연결 중 데이터 유실 방지
- Active-Active 중복 이벤트를 Flink에서 거래소 고유 ID로 제거 (raw : clean ≈ 2 : 1 확인)
- 토픽 이름 규칙(raw · clean · analytics)과 심볼 키 기반 co-partitioning 설계
- On-Prem Kubernetes에 Strimzi Kafka(KRaft, 브로커 3) · Flink Operator · 분산 MinIO 체크포인트 구성
- Exactly-Once와 실시간 지연 사이에서 at-least-once sink + 체크포인트 · HA · savepoint 선택

`Spring Boot` `Kafka (Strimzi)` `Flink` `MinIO` `ClickHouse` `Redis` `Kubernetes`

### <img src="https://api.iconify.design/lucide/database.svg?color=%23cf6a61" width="18" height="18" /> Batch

| Project | 내용 | Stack |
|:--|:--|:--|
| **[Riot TFT 데이터 파이프라인](https://github.com/donghee-kim775/tft-victory-planner)**<br/>`Team Project 1` | 상위 티어 경기 데이터를 매일 수집해 Bronze · Silver · Gold 메달리온 구조로 정제, Lambda로 EC2를 켜고 꺼서 비용 절감 | Airflow · dbt · Snowflake · S3 · Lambda |
| **[의류 구매 결정 지원 플랫폼](https://github.com/PonyoAndFriends/Fashion-Insights)**<br/>`Team Project 2` · 팀장 | 3개 패션 플랫폼 랭킹 · 리뷰와 YouTube · 네이버 데이터랩 · 기상청 데이터를 통합해 날씨 · 트렌드 분석 (DevCourse 최종 프로젝트 1등) | Spark · EKS · Airflow · S3 · Redshift · Power BI |


## <img src="https://api.iconify.design/lucide/file-text.svg?color=%237465b8" width="22" height="22" /> Research

| | |
|:--|:--|
| **졸업 논문** | 쿠버네티스 환경에서 DoE 기반 DeltaLake Vacuum 파라미터 최적화 연구 |
| **학부 논문** | Strategies for Data Cleanup and Optimization in Delta Lake: A Compaction-Vacuum Study · 한국정보기술학회 (1저자) |


## <img src="https://api.iconify.design/lucide/graduation-cap.svg?color=%232f9a8c" width="22" height="22" /> Education & Etc

| 기간 | 내용 |
|:--|:--|
| 2019.03 – 2025.02 | 대구가톨릭대학교 AI 빅데이터공학과 학사 · 인턴 3회 (코딩아이 · Adot · ETRI) |
| 2024.10 – 2025.01 | Programmers Data Engineering DevCourse · 팀 프로젝트 4회 (팀장 2회) |
| 2025.03 – 현재 | 대구가톨릭대학교 대학원 AI 빅데이터공학과 석사 |
| 자격 | SQLD (제51회 SQL 개발자) |


## <img src="https://api.iconify.design/lucide/pen-line.svg?color=%23bf9530" width="22" height="22" /> Writing

배운 것은 글로 남깁니다 — velog 시리즈 [문득문득](https://velog.io/@ehdgml775595/series/문득문득) · [Kubernetes](https://velog.io/@ehdgml775595/series/Kubernetes) · Notion [AWS DEA](https://youthful-yew-08d.notion.site/AWS-DEA-3215c482697580fda09de3902df0a769)
