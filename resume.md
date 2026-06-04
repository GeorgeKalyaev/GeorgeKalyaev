# Georgii Kaliaev

**Senior / Lead Performance Engineer**

Russia, Moscow (open to relocate). [LinkedIn](https://www.linkedin.com/in/georgii-kaliaev-3826b6214/), Telegram [@KGeorgeK](https://t.me/KGeorgeK), [GitHub profile](README.md).

---

## Education

**Plekhanov Russian University of Economics**, Bachelor's Degree in Information Systems (Jul 2014 - Jul 2018)  
**Moscow International Academy of Higher Education**, Business Informatics in Economics (Jul 2015 - Jul 2019)

---

## Professional summary

Senior / Lead Performance Engineer with **7+ years** of experience in performance engineering of **enterprise and high-load distributed systems** across **fintech, banking, retail, insurance, and government**.

Specialized in **workload modelling**, **NFR definition** (p95/p99 latency, throughput, scalability KPIs), **capacity planning**, **JVM and database** bottleneck analysis, and **CI/CD-integrated** performance validation. At **IBS**, **led a load-testing team of ~5 engineers**.

Track record of finding **root causes** of degradation and delivering **measurable** improvements in latency, throughput, and stability for **mission-critical** platforms.

---

## Selected results

Most significant outcomes and **root-cause findings** only — routine issues (pools, indexes, standard JVM/DB tuning, etc.) omitted. Full detail in work experience below.

- **First Asset Management — Kangal / K8s** (asset management, 2025–present): **introduced and standardized Kangal + JMeter on Kubernetes** as the default load-testing platform; **performance-tested 15+ REST microservices** across release cycles — on-demand injectors in an isolated namespace, horizontal worker scaling, automatic teardown after runs; distributed campaigns **without dedicated hardware idle between test windows**; **adopted by the team** for all release-cycle runs.
- **First Asset Management — PostgreSQL / capacity:** 5 growth models (0→100M+ rows, **~19 GB / ~12 GB indexes**); **~90%** forecast accuracy; **INSERT ~2.7 s → 22–77 s** (up to **8.3×**); SLA breach risk **~11 months**. **Partitioning + index tuning** (dev implemented on LT evidence) — **INSERT 20–70 s → ≤1 s** (to **2B** rows); capacity horizon **~11 months → ~30 years** at projected growth.
- **First Asset Management — batch / K8s:** throughput capped by **1 min cron** batch, not pod count (1 vs 3 pods — no gain); **Kafka** lag — not the bottleneck; recommended event-driven / worker pool.
- **First Asset Management — tooling:** built, published, and rolled out [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) for the team — JMeter step-profile validation; **reduced step-profile analysis time from ~5–6 hours to ~30 minutes** per campaign.
- **Sberbank SAP (IBS)** (very similar to **JPMorgan Chase**): ALL IN **~4 000** concurrent users; **~110** LoadRunner scripts; **~50–70** defects/campaign → **~500+** performance defects closed pre go-live across biweekly ERP train.
- **Federal Treasury GIIS (IBS):** Treasury-approved LTM **~45k ops/h** (P1); **15** JMeter scenarios, **7** LT iterations; NGINX **GOST/Lua** — national rollout sign-off.
- **Cooper / SberMarket (IBS)** (very similar to **Instacart**): prod night LT (**23:00–03:00**), **0** incidents: **~900 → 2600+ orders/h** (**+189%**); vs Dec **434k orders/day** business plan (Shopper/RTE separate); **400%** profile **~3900** HTTP req/s, **450k+** catalog req/h, **5000+** users; **30+** Gatling scenarios; RTE **~822** orders/h @ 100%.
- **Rosgosstrakh / Guidewire (IBS):** **~47k ops/h** baseline, **35+** use cases; **~151k** (max) / **~165k** (peak) ops/h at **80%** profile; **15+** stubs; Oracle/PolicyCenter fixes before insurance launch.
- **Leroy Merlin TMS (IBS):** **1200%** sign-off; volume model **~233k shipments** — PostgreSQL query **32 ms → 15.1 min** (~**28 000×**).
- **SPIMEX (IBS)** (very similar to **CME Group**): **~10 000 WebSocket msg/s** (STOMP); soak thread leak found pre go-live; RabbitMQ, ClickHouse.
- **Megapolis / IBS portal (IBS):** Megapolis **~95–99%** @ **~24** threads; IBS **1C-Bitrix** **~3380 ops/h**, auth **~425 → ~850** logins/15 min, **~3×** headroom, **2000-user** spike **~53%** CPU.
- **JVM / VisualVM (IBS):** remote VisualVM on soak — **threads not shutting down**, live count grew; fix applied right after load-test findings.
- **HornetQ / JBoss (Alfa-Bank):** queues unmonitored; custom **bash** → **CSV** → **Excel** summary showed backlog growth; JBoss HornetQ memory config — queues stabilized after rollout.
- **Oracle (Alfa-Bank / ScriptMaster)** (very similar to **Citigroup**): LoadRunner, IBM MQ; **5000** VU; **~25%** latency / **~15%** throughput improvement after SQL tuning.

---

## Work experience

### First Asset Management, *Principal Development Engineer — load testing* (Jan 2025 - Present)

Russian asset management company; very similar to **Vanguard** (mutual funds, ETFs, discretionary portfolios). In-house digital platform on microservices and **Kubernetes**.

- **Proposed PostgreSQL table partitioning and index tuning** based on load-test evidence; dev implemented — **INSERT 20–70 s → ≤1 s** (to **2B** rows); capacity horizon **~11 months → ~30 years** at projected growth (vs **~11 months** breach risk before fix).
- **PostgreSQL capacity planning:** built **5 growth models** (**0 → 100M+ rows**, **~19 GB data, ~12 GB indexes** at peak); **~90%** forecast accuracy; as data volume grew, **INSERT latency increased from ~2.7 s to 22–77 s** (up to **8.3×**), with up to **800 MB disk read** per operation.
- **Introduced and standardized Kangal + JMeter on Kubernetes** as the default load-testing platform: **performance-tested 15+ REST microservices** across release cycles — on-demand load generators in an isolated namespace, horizontal scaling of JMeter workers, automatic teardown after runs; distributed campaigns **without dedicated hardware idle between test windows**; **adopted by the team** for all release-cycle runs.
- **Batch processing in K8s:** throughput limited by **1 min cron** batch, not pod count (1 vs 3 pods — no gain); **Kafka** lag analysis — not the bottleneck; recommended worker pool / event-driven design.
- Built, published, and rolled out **[jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker)** — JMeter step profile validation; **reduced step-profile analysis from ~5–6 h to ~30 min** per campaign.
- **NFR** validation (p95/p99 latency, throughput); correlation with **Grafana**, **Prometheus**, **Zabbix**, **ELK/OpenSearch**, **HAProxy**, **Redis**. Internal automation (**Python**, **GitLab CI**).

### IBS, *Senior Performance Test Engineer* (May 2020 - Jan 2025)

Large IT consulting and system integrator; very similar to **EPAM** or **Accenture** (embedded in client teams). Engagements across banking, insurance, retail and e-commerce, commodity exchange, and government.

- **Led a load-testing team of ~5 engineers:** campaign planning, mentoring, onboarding, technical interviews, hiring. IBS awards: **Team Player** (2023), **Project Driver** (2022).
- **Observability and logs (across engagements):** **Grafana** with **InfluxDB** / **Telegraf**, **Zabbix**, **ELK** (**Elasticsearch**, **Kibana**; **Logstash** / **Filebeat** as deployed); plus **AppDynamics** and **Splunk** for APM-style analysis and incident triage.  
- **Sber** (Russia's largest bank; very similar to **JPMorgan Chase**) — **SAP ERP / SAP BW** on **HANA** (**LoadRunner** / **Performance Center**): ALL IN **~4 000** concurrent users; **~110** scripts (SAP GUI/Web, **Fiori**); **~50–70** defects/campaign → **~500+** closed pre go-live; **~10** biweekly ERP cycles; BW on separate analytical cadence; **Jira** / **Confluence**.  
- **Rosgosstrakh / Guidewire** (very similar to **State Farm**) — customer-approved **LTM**; **PREPROD** → dedicated LT stand; **15+** stubs (**Spring Boot**, **MockServer**); stepping peak **~165k ops/h** at **80%** profile; **47k ops/h** baseline, **35+** use cases (**CASCO**, **OSAGO**, multichannel); Oracle/PolicyCenter fixes before launch; **AppDynamics**, **Splunk**, **Bamboo**.  
- **SPIMEX** (national commodity exchange; very similar to **CME Group**) — exchange / trading workloads: up to **~10,000 WebSocket** messages/s (**STOMP**), **RabbitMQ**; **REST** microservices and **ClickHouse** (time-series, ingest) plus **JDBC** to **PostgreSQL**; **JSR223** in **JMeter** to drive trading-style traffic into **RabbitMQ**; **custom Java** load clients (**Spring**, **STOMP**/**WebSocket**, **order book** / **facade** scenarios) alongside **JMeter**; on injectors — **Telegraf**, **InfluxDB 2.x**, **Grafana** (including **JMeter** and **Java** run metrics), customer **Zabbix** and **RabbitMQ Management** for queue depth.  
- **Leroy Merlin** (very similar to **Home Depot**) — **Gatling**: **1200%** sign-off (1h peak + 5h soak) on **TMS** / **Carrier Portal** (**K8s**, **PostgreSQL**, **Redis**); volume model **~233k shipments** (2–3 years): max query **32 ms → 15.1 min**, UI freeze localized pre go-live.  
- **Cooper / SberMarket** (very similar to **Instacart**) — prod night LT (**23:00–03:00**), **0** incidents: **~900 → 2600+/h** (**+189%**); validated vs **434k orders/day** Dec peak plan (Shopper/RTE separate); **400%** profile **~3900** HTTP req/s, **450k+** catalog req/h, **5000+** users; **30+** Gatling; RTE **~822** orders/h; prod-scale test data (**~45k** B2C/B2B accounts, **~2k** RTE, **1200** Shopper stores); **Kafka**, **PostgreSQL**, ELK.  
- **GIIS “Electronic Budget” / Federal Treasury** (very similar to U.S. **Treasury**): Treasury-approved LTM **~45k ops/h** (P1, **TOFK** statistics); **15** JMeter scenarios, **7** iterations (13h reliability); **NGINX** (**GOST**, **Lua**); **Redis**; **Telegraf**, **InfluxDB**, **Grafana**.  
- **Megapolis (GKM)** — SAP HR portal: **~95–99%** target throughput at sign-off load (**~24** threads), p90 **3–10 s**; peak stress risks documented at **240** threads.  
- **Corporate portal (IBS internal)** — **1C-Bitrix**: profile **~3380 ops/h** from analytics; **2×** CPU → auth **~425 → ~850** logins/15 min; **~3×** headroom (**~400%** vs **~135%**); **2000-user** news spike **~53%** CPU; AD vs local login RCA.  
- **Technical interviews**, mentoring, hiring contributions.  
- **JVM / VisualVM (IBS):** during load and soak runs monitored the application with **remote VisualVM** (thread timeline, live thread count); on one engagement thread-level metrics were **not visible in standard dashboards** — found **threads not shutting down**: live count **grew steadily** under load; localized the pattern, reported root cause to development; **fix applied right after the load-test findings**.  
- **JVM and OS limits (across engagements):** GC, heap, thread contention; extra **scheduler** threads (**RxJava**-style pools, metric export to **InfluxDB**); when hitting **native** memory / OS limits — diagnosis and **temporary** mitigation (**vm.max_map_count**, **ulimit** **nproc**/**nofile**) pending code fixes; dumps, logs, correlation with the run.  
- **NFR** definition and validation across client engagements.  
- **Profiling and distributed tracing** where available: **APM** (**AppDynamics** and similar) for **distributed traces** and slow spans; JVM profiling; correlating traces, spans, and metrics with load-test windows; without full APM — logs, metrics, and time-based correlation.  

### ScriptMaster, *Performance Test Engineer* (Jul 2019 - May 2020)

IT integrator on **Alfa-Bank** projects (major private bank; very similar to **Citigroup**): core banking and legal workflows (**30M+** retail clients).

- Banking systems with **30M+** end users; stability under peak load.  
- **LoadRunner** scenarios, up to **5,000** concurrent users on legal workflows.  
- **IBM MQ** high-volume inbound flows; **HornetQ (JBoss)** internal queues were **not monitored** by the business or platform — built a **bash** script for load-test runs to sample **queue depth and timestamp**, export to **CSV**, and build a summary in **Excel**; the table showed **backlog growth** under load and localized the bottleneck; recommended **JBoss** HornetQ memory limit increase (`address/global-max-size`) — queues stabilized after rollout.  
- **Oracle** tuning with execution plans and **AWR**: example outcome **~25%** DB latency reduction and **~15%** throughput gain.  
- **JBoss** JVM monitoring (GC, thread pools).  

---

## Technical skills

**Load testing**  
![JMeter](https://img.shields.io/badge/JMeter-D22128?style=flat-square&logo=apachejmeter&logoColor=white)
![Gatling Java/Scala, SBT](https://img.shields.io/badge/Gatling%20Java%2FScala%2C%20SBT-FF6600?style=flat-square&logo=gatling&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![LoadRunner](https://img.shields.io/badge/LoadRunner-007ACC?style=flat-square)
![Performance Center](https://img.shields.io/badge/Performance%20Center-0052CC?style=flat-square)
![LoadIT](https://img.shields.io/badge/LoadIT-546E7A?style=flat-square)
![Kangal](https://img.shields.io/badge/Kangal-4CAF50?style=flat-square)

**Observability / APM**  
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=flat-square&logo=influxdb&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Telegraf](https://img.shields.io/badge/Telegraf-000000?style=flat-square)
![ELK](https://img.shields.io/badge/ELK-005571?style=flat-square&logo=elasticsearch&logoColor=white)
![Zabbix](https://img.shields.io/badge/Zabbix-CC0000?style=flat-square)
![AppDynamics](https://img.shields.io/badge/AppDynamics-1488C6?style=flat-square)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white)

**Databases and cache**  
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![MS SQL Server](https://img.shields.io/badge/MS%20SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Messaging**  
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![IBM MQ](https://img.shields.io/badge/IBM%20MQ-054ADA?style=flat-square)

**Protocols**  
![REST](https://img.shields.io/badge/REST-02569B?style=flat-square)
![SOAP](https://img.shields.io/badge/SOAP-6DB33F?style=flat-square)
![WebSocket](https://img.shields.io/badge/WebSocket-STOMP-1976D2?style=flat-square)
![JDBC](https://img.shields.io/badge/JDBC-F29111?style=flat-square)
![gRPC](https://img.shields.io/badge/gRPC-24496A?style=flat-square&logo=grpc&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=flat-square)
![XML](https://img.shields.io/badge/XML-005571?style=flat-square)
![SAP](https://img.shields.io/static/v1?label=SAP&message=ERP%20-%20BW%20-%20FIORI&color=0FAAFF&style=flat-square)

**Languages**  
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Scala](https://img.shields.io/badge/Scala-DC322F?style=flat-square&logo=scala&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square)
![Lua](https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white)

**Cloud / DevOps**  
![CI/CD](https://img.shields.io/badge/CI%2FCD-607D8B?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![Bamboo](https://img.shields.io/badge/Bamboo-0052CC?style=flat-square&logo=bamboo&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Bitbucket](https://img.shields.io/badge/Bitbucket-0052CC?style=flat-square&logo=bitbucket&logoColor=white)

**Middleware**  
![NGINX](https://img.shields.io/badge/NGINX-GOST%20%7C%20Lua-009639?style=flat-square&logo=nginx&logoColor=white)
![HAProxy](https://img.shields.io/badge/HAProxy-21313C?style=flat-square)
![JBoss](https://img.shields.io/badge/JBoss-WildFly-CC0000?style=flat-square)

**Stubs / integration**  
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![MockServer](https://img.shields.io/badge/MockServer-7E57C2?style=flat-square)
![Axis2](https://img.shields.io/badge/Axis2-SOAP-5C6BC0?style=flat-square)
![Active Directory](https://img.shields.io/badge/Active%20Directory-0078D4?style=flat-square&logo=microsoft&logoColor=white)

**JVM and OS analysis**  
![VisualVM](https://img.shields.io/badge/VisualVM-4A4A4A?style=flat-square)
![GC logs](https://img.shields.io/badge/GC%2Fheap%2Fthread%20dumps-607D8B?style=flat-square)
![lab128](https://img.shields.io/badge/lab128-546E7A?style=flat-square)
![nmon](https://img.shields.io/badge/nmon-546E7A?style=flat-square)

**Tooling**  
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-000000?style=flat-square&logo=intellijidea&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=flat-square&logo=androidstudio&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)
![SoapUI](https://img.shields.io/badge/SoapUI-6CB33E?style=flat-square)
![Fiddler](https://img.shields.io/badge/Fiddler-6B69D6?style=flat-square)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white)
![Confluence](https://img.shields.io/badge/Confluence-172B4D?style=flat-square&logo=confluence&logoColor=white)

---

## Honors

- IBS **Team Player** (2023)  
- IBS **Project Driver** (2022)  

---

## Languages

- **English:** professional working proficiency (B2+)  
- **Russian:** native  

---

## Open source and writing

- [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) (open source)
- **PostgreSQL at scale** — [LinkedIn](https://www.linkedin.com/pulse/how-we-found-postgresql-bottleneck-during-load-testing-kaliaev-rbr2e/)
- **NGINX + JMeter** — [LinkedIn](https://www.linkedin.com/pulse/why-we-started-using-nginx-load-testing-jmeter-george-kalyaev-ump7e/)

---

*[GitHub profile / README](README.md)*
