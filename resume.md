# Georgii Kaliaev

**Senior / Lead Performance Engineer**

Russia, Moscow (open to relocate). [LinkedIn](https://www.linkedin.com/in/georgii-kaliaev-3826b6214/), Telegram [@KGeorgeK](https://t.me/KGeorgeK), [GitHub profile](README.md).

---

## Education

**Plekhanov Russian University of Economics**, Bachelor's Degree in Information Systems (Jul 2014 - Jul 2018)  
**Moscow International Academy of Higher Education**, Business Informatics in Economics (Jul 2015 - Jul 2019)

---

## Professional summary

Senior / Lead Performance Engineer with **7+ years** of experience building and running performance engineering for **enterprise and high-load distributed systems** across **fintech, banking, retail, insurance, and government**.

I design workload models and NFRs (p95/p99 latency, throughput, scalability KPIs), run load / stress / capacity campaigns, find JVM and database bottlenecks, and integrate performance checks into CI/CD. At **IBS** I **led a load-testing team of ~5 engineers**.

I focus on root-cause findings and **measurable** gains in latency, throughput, stability, and infrastructure cost for mission-critical platforms.

---

## Key achievements

- **Cut** total CPU usage by **100+ vCPU** through performance tuning on the current product platform.
- **Built** a Kubernetes load platform (**Kangal + JMeter**) and load-tested **15+** microservices with on-demand generators (no idle load hardware between runs).
- **Developed** [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) and **reduced** campaign analysis from **~5–6 hours to ~1 hour**.
- **Conducted** production night load tests for grocery e-commerce: key flow **~900 → 2600+ orders/h** (**+189%**), **0** customer incidents.
- **Validated** exchange trading load at **~10,000 WebSocket msg/s** and **found** a thread leak that removed OOM risk before go-live.
- **Identified and closed ~500+** SAP performance defects before production (**~4,000** users).
- **Led** a load-testing team of **~5** at IBS (Team Player 2023, Project Driver 2022).

---

## Selected results

Most significant outcomes only — routine issues omitted. Full detail in work experience below.

### First Asset Management *(product · 2025–present)*

Asset management firm (funds / portfolios) — internal product platform (АО УК «Первая» / Sber-related projects), not client consulting.

- **Built** Kangal + JMeter on Kubernetes as the default load platform and **load-tested 15+** REST microservices with on-demand injectors, worker scaling, and teardown — **no idle load hardware** between campaigns.
- **Reduced** total CPU consumption by **100+ vCPU** through performance tuning (service / JVM / infra recommendations from load-test findings).
- **Built 5** PostgreSQL growth models (0→100M+ rows), **forecast** SLA risk with **~90%** accuracy, **identified** INSERT degradation up to **8.3×**, and **proposed** partitioning — after fix **INSERT 20–70 s → ≤1 s** (validated to **2B** rows); capacity horizon **~11 months → ~30 years** — [case write-up](https://www.linkedin.com/pulse/how-we-found-postgresql-bottleneck-during-load-testing-kaliaev-rbr2e/).
- **Showed** that a 1-minute cron/batch path does not scale by adding pods (1→3 pods, no RPS gain) and **recommended** a worker pool / event-driven design instead of polling.
- **Developed and rolled out** [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) — **cut** step-profile analysis from **~5–6 h to ~1 h** per campaign.

### IBS *(consulting / embedded · 2020–2025 · lead ~5 engineers)*

- **Cooper / SberMarket:** **Developed** Gatling scenarios (B2C/B2B + mobile) and **ran** night production load tests with **0** incidents; key flow grew **~900 → 2600+/h** (**+189%**), **5000+** users, **30+** scenarios — [suite](https://github.com/GeorgeKalyaev/gatling-grocery-ecommerce-suite).
- **SPIMEX:** **Conducted** trading-contour load tests (WebSocket/STOMP + REST) at **~10,000 msg/s**, **tested** horizontal scaling of microservices, and **found** a soak thread leak — removed OOM risk before go-live.
- **Federal Treasury / GIIS:** **Agreed** the load model with the customer (**~45k ops/h**), **built** the GOST / CryptoPro contour, and **implemented** NGINX + Lua logging for multi-cert HTTPS load — [article](https://www.linkedin.com/pulse/why-we-started-using-nginx-load-testing-jmeter-george-kalyaev-ump7e/).
- **Rosgosstrakh / Guidewire:** **Developed** end-to-end insurance scenarios and **15+** stubs; **validated** peak **~165k ops/h** at **80%** profile before launch.
- **Leroy Merlin TMS:** **Developed** Gatling scenarios and **ran** tests on a **2–3 year** data volume; **caught** a PostgreSQL query degradation **32 ms → 15.1 min** before go-live — [suite](https://github.com/GeorgeKalyaev/gatling-tms-carrier-portal-suite).
- **Sberbank SAP:** **Maintained** LoadRunner/Performance Center contour for **~4,000** users and **~110** scripts; **identified and closed ~500+** performance defects before production.
- **Megapolis / IBS portal:** **Conducted** capacity sign-off for SAP HR and Bitrix portals; **found** threads not shutting down under soak (VisualVM) and drove the fix.

### ScriptMaster → Alfa-Bank only *(2019–2020)*

At that time ScriptMaster delivered **Alfa-Bank projects only**. Two engagements:

- **FSSP:** **Built** load testing from scratch for bank↔gov legal flows — up to **~5,000** VU (LoadRunner), IBM MQ + file-drop XML over SMB/FTP, **~30** SOAP stubs; **fixed** HornetQ backlog; **improved** Oracle latency **~−25%** and throughput **~+15%**.
- **Citrix / RDP:** **Conducted** remote-desktop load tests and **evaluated** channel/server stability under peak concurrent sessions.

---

## Work experience

### First Asset Management (АО УК «Первая»), *Principal Development Engineer — load testing* (Jan 2025 - Present)

Russian asset management company; very similar to **Vanguard** (mutual funds, ETFs, discretionary portfolios). In-house digital platform on microservices and **Kubernetes** (Sber-related projects).

- **Proposed** PostgreSQL partitioning and index tuning from load-test evidence; after development implemented — **INSERT 20–70 s → ≤1 s** (to **2B** rows); capacity horizon **~11 months → ~30 years** — [case write-up](https://www.linkedin.com/pulse/how-we-found-postgresql-bottleneck-during-load-testing-kaliaev-rbr2e/).
- **Built 5** PostgreSQL growth models (**0 → 100M+ rows**, **~19 GB** data / **~12 GB** indexes); **achieved ~90%** forecast accuracy; **identified** INSERT latency growth from **~2.7 s to 22–77 s** (up to **8.3×**).
- **Introduced** Kangal + JMeter on Kubernetes as the team standard and **performance-tested 15+** REST microservices across release cycles — on-demand injectors, worker scaling, automatic teardown; **no idle load hardware** between campaigns.
- **Reduced** total CPU consumption by **100+ vCPU** through performance tuning from load-test findings.
- **Tested** horizontal vs vertical scaling on K8s; **showed** batch throughput limited by a **1 min cron**, not pod count (1 vs 3 pods — no gain); **analyzed** Kafka lag (not the bottleneck); **recommended** worker pool / event-driven design.
- **Developed, published, and rolled out** **[jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker)** — **reduced** step-profile analysis from **~5–6 h to ~1 h** per campaign.
- **Validated** NFRs (p95/p99, throughput) and **correlated** Grafana / Prometheus / Zabbix / ELK/OpenSearch / HAProxy / Redis with test windows; **automated** prep and runs with **Python** and **GitLab CI**.

### IBS, *Senior Performance Test Engineer* (May 2020 - Jan 2025)

Large IT consulting and system integrator; very similar to **EPAM** or **Accenture** (embedded in client teams). Engagements across banking, insurance, retail and e-commerce, commodity exchange, and government.

- **Led** a load-testing team of **~5 engineers**: campaign planning, mentoring, onboarding, technical interviews, hiring. Awards: **Team Player** (2023), **Project Driver** (2022).
- **Optimized and extended** JMX / VuGen / Gatling scenarios with **Groovy, Bash, Redis and REST API** — shortened test-prep time and made synthetic flow more realistic.
- **Built** observability for campaigns with **Grafana**, **InfluxDB** / **Telegraf**, **Zabbix**, **ELK**, plus **AppDynamics** and **Splunk** for incident triage.
- **Sber** (similar to **JPMorgan Chase**) — **Ran** SAP ERP / SAP BW on HANA load with LoadRunner / Performance Center: **~4,000** concurrent users, **~110** scripts (SAP GUI/Web, **Fiori**); **identified ~50–70** defects per campaign and **closed ~500+** before go-live across biweekly ERP cycles.
- **Rosgosstrakh / Guidewire** (similar to **State Farm**) — **Developed** LTM with customer, **built** PREPROD → dedicated LT stand, **created 15+** stubs (**Spring Boot**, **MockServer**), and **validated** peak **~165k ops/h** at **80%** profile (**47k ops/h** baseline, **35+** use cases: CASCO / OSAGO / multichannel).
- **SPIMEX** (similar to **CME Group**) — **Conducted** exchange load up to **~10,000 WebSocket** msg/s (**STOMP**) with **RabbitMQ**; **drove** REST microservices and **ClickHouse** / PostgreSQL paths; **built** custom Java clients alongside JMeter; **monitored** injectors with Telegraf / InfluxDB / Grafana.
- **Leroy Merlin** (similar to **Home Depot**) — **Developed** Gatling tests and **signed off 1200%** load (1h peak + 5h soak) on TMS / Carrier Portal; **caught** PG query **32 ms → 15.1 min** on **~233k shipments** volume model before go-live — [suite](https://github.com/GeorgeKalyaev/gatling-tms-carrier-portal-suite).
- **Cooper / SberMarket** (similar to **Instacart**) — **Ran** production night LT (**23:00–03:00**) with **0** incidents: **~900 → 2600+/h** (**+189%**); **validated** against **434k orders/day** peak plan; **executed** **400%** profile (**~3900** HTTP req/s, **5000+** users, **30+** Gatling scenarios) — [suite](https://github.com/GeorgeKalyaev/gatling-grocery-ecommerce-suite).
- **GIIS “Electronic Budget” / Federal Treasury** — **Agreed** LTM **~45k ops/h** with the customer; **developed 15** JMeter HTTPS scenarios with **GOST** e-signature; **configured** CryptoPro CSP and **implemented** NGINX (GOST cert per port, Lua logging); **completed 7** LT iterations including 13h reliability — [article](https://www.linkedin.com/pulse/why-we-started-using-nginx-load-testing-jmeter-george-kalyaev-ump7e/).
- **Megapolis (GKM)** — **Conducted** SAP HR portal capacity testing: **~95–99%** target throughput at sign-off (**~24** threads); **documented** peak stress risks at **240** threads.
- **Corporate portal (IBS internal)** — **Tested** 1C-Bitrix capacity (**~3380 ops/h** profile); **showed** auth **~425 → ~850** logins/15 min after **2×** CPU; **analyzed** AD vs local login under a **2000-user** spike (**~53%** CPU).
- **Conducted** technical interviews, mentoring, and hiring.
- **Monitored** JVM with remote VisualVM under load/soak; **found** threads not shutting down (live count grew steadily); **reported** root cause — fix applied right after findings.
- **Diagnosed** JVM/OS limits (GC, heap, thread contention, native memory) and **applied** temporary mitigations (`vm.max_map_count`, `ulimit`) pending code fixes.
- **Defined and validated** NFRs across client engagements; **correlated** APM traces (AppDynamics) and metrics with load-test windows.

### ScriptMaster, *Performance Test Engineer* (Jul 2019 - Apr 2020)

IT integrator on **Alfa-Bank** projects (major private bank; very similar to **Citigroup**): **30M+** retail clients.

**Federal Bailiff Service (FSSP)** — bank ↔ government legal/integration contour. **Built** load testing from scratch: scenarios → stand → runs → RCA → readiness sign-off.

- **Developed** LoadRunner (**Java**) / Performance Center scenarios for up to **~5,000** concurrent users on FSSP legal and transaction flows.
- **Injected** load two ways: **IBM MQ** and **file-based** entry — **generated** FNS XML and **dropped** files to SMB/FTP shares; mixed profile **~75%/25%**; unique keys via **VTS**.
- **Built** in-run custom monitoring in LoadRunner (IBM MQ depth + FTP file counts as user data points) and **caught** backlog during the run.
- **Developed and maintained ~30** SOAP stubs on Java (**Apache Axis2** / Tomcat) to isolate LT from real adjacent bank systems.
- **Identified** HornetQ backlog under JBoss (no stock monitoring); **built** a bash sampler to CSV; **initiated** memory-limit increase — queues stabilized after rollout.
- **Optimized** Oracle SQL via execution plans / AWR: DB latency **~−25%**, throughput **~+15%**; **monitored** JBoss JVM (GC, thread pools).

**Citrix / RDP** (separate engagement): **Conducted** LoadRunner RDP / Citrix load for concurrent remote sessions and **evaluated** channel and server stability under session peaks.

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
![NBomber](https://img.shields.io/badge/NBomber-512BD4?style=flat-square)

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
![RDP / Citrix](https://img.shields.io/badge/RDP%20%2F%20Citrix-0078D4?style=flat-square)
![SMB](https://img.shields.io/badge/SMB%20file%20drop-546E7A?style=flat-square)

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

- [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) (open source) — campaign analysis **~5–6 h → ~1 h**
- **PostgreSQL at scale** — [LinkedIn](https://www.linkedin.com/pulse/how-we-found-postgresql-bottleneck-during-load-testing-kaliaev-rbr2e/)
- **NGINX + JMeter** — [LinkedIn](https://www.linkedin.com/pulse/why-we-started-using-nginx-load-testing-jmeter-george-kalyaev-ump7e/)
- **Load generator OS tuning** (`limits.conf` / `sysctl`) — [LinkedIn](https://www.linkedin.com/pulse/when-bottleneck-load-generator-limitsconf-sysctl-georgii-kaliaev-mnoye/)

---

*[GitHub profile / README](README.md)*
