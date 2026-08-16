# 👨‍💻 Georgii Kaliaev

**Senior / Lead Performance Engineer | Load testing | Capacity planning and NFR**

🌐 English: B2 — professional working proficiency  
📄 Resume: [CV (full)](resume.md)  🔗 LinkedIn: [https://www.linkedin.com/in/georgii-kaliaev-3826b6214/](https://www.linkedin.com/in/georgii-kaliaev-3826b6214/)  
📨 Telegram: [@KGeorgeK](https://t.me/KGeorgeK)  
📦 Open source: [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker)

<!-- GitHub → Settings → Public profile:
  LinkedIn: https://www.linkedin.com/in/georgii-kaliaev-3826b6214/
  Bio (suggested): Senior / Lead Performance Engineer · 7+ years · load, capacity, RCA · JMeter, Gatling, LoadRunner, K8s/Kangal · FSSP file+MQ, Citrix/RDP · First Asset Management · ex-IBS lead ~5
  Pinned (suggested): jmeter-load-profile-checker, gatling-webtours-demo, k6-webtours-demo, nbomber-webtours-demo, LoadRunner-WebTours
-->

---

## 🚀 About Me

I am a **Senior / Lead Performance Engineer** with **7+ years** of hands-on experience building and running load, stress, capacity, and scalability testing for **high-load distributed systems** — fintech, banking, e-commerce, insurance, government, and trading.

I design workload models and **NFRs** (p95/p99, throughput), **conduct** test campaigns, **build** observability around them, **find** bottlenecks, and **deliver** actionable recommendations to development and architecture.

At **IBS** I **led** a load-testing team of **~5 engineers** (Team Player 2023, Project Driver 2022) — e.g. **identified and closed ~500+** SAP defects before prod (**~4 000** users), **agreed** Treasury LTM **~45k ops/h**, **ran** grocery night LT **+189%** with **0** incidents, **validated** exchange **~10k WebSocket msg/s**, **validated** Guidewire **~165k ops/h**.

Currently at **First Asset Management** (АО УК «Первая»; similar to **Vanguard**) as **Principal Development Engineer (load testing)**: **introduced** Kangal + JMeter on Kubernetes, **load-tested 15+** REST microservices (on-demand injectors, scaling, teardown — **no idle load hardware**), **built** PostgreSQL capacity models (100M+ rows), **reduced** total CPU by **100+ vCPU**, and **developed** internal **Python** tooling in **GitLab CI**.

---

## 📊 Key achievements

- **Cut** total CPU usage by **100+ vCPU** through performance tuning.
- **Built** Kangal + JMeter on Kubernetes and **load-tested 15+** microservices with on-demand generators.
- **Developed** [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) — campaign analysis **~5–6 h → ~1 h**.
- **Conducted** grocery prod night LT: **~900 → 2600+ orders/h** (**+189%**), **0** incidents.
- **Validated** exchange load at **~10,000 WebSocket msg/s** and **found** a thread leak (OOM risk removed pre go-live).
- **Identified and closed ~500+** SAP performance defects before production.
- **Led** load-testing team of **~5** at IBS.

---

## 📊 Selected results

Outcomes from load campaigns — **most significant cases only**. Full detail: [resume.md](resume.md).

### First Asset Management *(product · 2025–present)*

Asset management firm (funds / portfolios) — internal product platform (АО УК «Первая» / Sber-related projects), not client consulting.

| Area | Outcome |
|------|---------|
| **PostgreSQL / capacity** | **Built 5** growth models (0→100M+ rows). **Forecast** SLA risk (**~90%** accuracy). **Identified** INSERT degradation up to **8.3×** (**~2.7 s → 22–77 s**). **Proposed** partitioning — after fix **INSERT 20–70 s → ≤1 s** (to **2B** rows); horizon **~11 months → ~30 years** — [write-up](https://www.linkedin.com/pulse/how-we-found-postgresql-bottleneck-during-load-testing-kaliaev-rbr2e/) |
| **K8s / Kangal** | **Introduced** Kangal + JMeter as the default LT platform. **Load-tested 15+** REST services with on-demand injectors, worker scaling, teardown. **No idle LT hardware** between campaigns |
| **CPU / tuning** | **Reduced** total CPU by **100+ vCPU** through performance tuning from LT findings |
| **Tooling** | **Developed and rolled out** [jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker) — analysis **~5–6 h → ~1 h** per campaign |
| **Batch / scaling** | **Showed** throughput capped by **1 min cron**, not pod count (1→3 pods — no gain). **Recommended** event-driven / worker pool |

### IBS *(consulting / embedded · 2020–2025 · lead ~5 engineers)*

| Client / project | Outcome |
|------------------|---------|
| **Cooper / SberMarket**<br>*grocery e-commerce / retail delivery* | **Developed** Gatling scenarios (B2C/B2B + mobile) and **ran** prod night LT (**23:00–03:00**) with **0** incidents: **~900 → 2600+/h** (**+189%**). **400%** profile **~3900** HTTP req/s, **5000+** users, **30+** scenarios — [suite](https://github.com/GeorgeKalyaev/gatling-grocery-ecommerce-suite) |
| **SPIMEX**<br>*commodity exchange, St. Petersburg* | **Conducted** trading load (WebSocket/STOMP + REST) at **~10 000 msg/s**. **Found** soak thread leak (VisualVM) — OOM risk removed pre go-live |
| **Federal Treasury / GIIS**<br>*gov. public finance / e-budget* | **Agreed** LTM **~45k ops/h**. **Built** GOST / CryptoPro contour and **implemented** NGINX (GOST certs per port, **Lua** logging) — [article](https://www.linkedin.com/pulse/why-we-started-using-nginx-load-testing-jmeter-george-kalyaev-ump7e/) |
| **Rosgosstrakh / Guidewire**<br>*insurance (PolicyCenter)* | **Developed** end-to-end scenarios and **15+** stubs. **Validated** peak **~165k ops/h** at **80%** profile before launch |
| **Leroy Merlin TMS**<br>*DIY retail - transport / carrier portal* | **Developed** Gatling tests and **signed off 1200%** load. **Caught** PG query **32 ms → 15.1 min** on **~233k shipments** volume before go-live — [suite](https://github.com/GeorgeKalyaev/gatling-tms-carrier-portal-suite) |
| **Sberbank SAP**<br>*largest Russian bank - ERP / BW* | **Ran** LoadRunner / Performance Center for **~4 000** users and **~110** scripts. **Identified and closed ~500+** performance defects before go-live |
| **Megapolis / IBS portal**<br>*SAP HR portal + corporate Bitrix* | **Conducted** capacity sign-off. Bitrix auth **~425 → ~850** logins/15 min. **Found** threads not shutting down under soak |
| **JVM / VisualVM**<br>*cross-engagement finding* | **Monitored** soak with remote VisualVM; **found** threads not shutting down; fix applied right after LT findings |

### ScriptMaster → Alfa-Bank only *(2019–2020)*

At that time ScriptMaster delivered **Alfa-Bank projects only**. Two engagements:

| Project | Outcome |
|---------|---------|
| **FSSP** (Federal Bailiff Service) | **Built** LT from scratch. **Conducted** LoadRunner campaigns up to **~5000** VU (IBM MQ + file-drop XML over SMB/FTP). **Developed ~30** SOAP stubs. **Fixed** HornetQ backlog. **Improved** Oracle latency **~−25%**, throughput **~+15%** |
| **Citrix / RDP** | **Conducted** remote-desktop load tests and **evaluated** channel/server stability under peak concurrent sessions |

---

### 🔧 What I Do

- **Design** realistic load models and **NFR / methodology** from business traffic and production signals
- **Build** performance frameworks (**JMeter**, **Gatling**, **LoadRunner**, **k6**); **run** **Kangal** on **Kubernetes** (on-demand injectors, scaling, teardown); **tune** load-generator hosts (`limits.conf` / `sysctl`)
- **Optimize and extend** **JMX / VuGen / Gatling** scenarios with **Groovy, Bash, Redis and REST API** — shorter prep, more realistic synthetic flow
- **Conduct** load, stress, soak, and **capacity** tests; **integrate** regression performance into release cycles
- **Correlate** **Grafana / Prometheus / ELK / APM** with test windows; **perform RCA** across app, JVM, DB, **Kafka**, K8s
- **Perform** capacity planning and SLA forecasting (PostgreSQL at scale); **drive** tuning that cut **100+ vCPU** on the current platform
- **Lead and mentor** performance engineers (**team of ~5** at IBS); **conduct** technical interviews and hiring
- **Deliver** clear recommendations to engineering, DevOps, and stakeholders

---

## 🧪 Tools - Technologies

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

## 📌 Domains

- Banking and FinTech
- Insurance
- E-commerce and Logistics
- Commodity Trading Platforms
- Government Financial Systems

---

## 🧠 Professional Focus

- **Conduct** load, stress, and **capacity** testing for **cloud-native / microservices** systems
- **Validate** NFRs (p95/p99, throughput, error rate, scalability KPIs)
- **Perform** bottleneck analysis (application, JVM, database, **Kafka/RabbitMQ**, K8s, LB)
- **Build** performance monitoring / observability and **correlate** distributed traces with test windows
- **Integrate** performance pipelines into **CI/CD** (GitLab CI, Jenkins, Bamboo)
- **Lead** performance engineers (**team of ~5** at IBS): mentoring, interviews, campaign standards
- **Improve** stability, scalability, and reliability of high-load platforms

---

## 📚 Open source and writing

- **[jmeter-load-profile-checker](https://github.com/GeorgeKalyaev/jmeter-load-profile-checker)** (open source) — validate JMeter load profile by step; campaign analysis **~5–6 h → ~1 h**
- **PostgreSQL bottleneck at scale** — capacity, INSERT degradation, data model and indexing — [LinkedIn](https://www.linkedin.com/pulse/how-we-found-postgresql-bottleneck-during-load-testing-kaliaev-rbr2e/)
- **NGINX + JMeter** — multiple client certs, GOST, proxy instead of Fiddler — [LinkedIn](https://www.linkedin.com/pulse/why-we-started-using-nginx-load-testing-jmeter-george-kalyaev-ump7e/)
- **Load generator OS tuning** — `limits.conf` / `sysctl` when the bottleneck is the injector, not the SUT — [LinkedIn](https://www.linkedin.com/pulse/when-bottleneck-load-generator-limitsconf-sysctl-georgii-kaliaev-mnoye/)

---

## 🎓 Certifications and Learning

![Team Player](https://img.shields.io/badge/Team%20Player-IBS%202023-2ea44f?style=flat-square)
![Project Driver](https://img.shields.io/badge/Project%20Driver-IBS%202022-2ea44f?style=flat-square)
![Apache JMeter](https://img.shields.io/badge/Apache%20JMeter-Certified-D22128?style=flat-square&logo=apachejmeter&logoColor=white)
![LoadRunner](https://img.shields.io/badge/LoadRunner-Certified-007ACC?style=flat-square)
![Load Testing](https://img.shields.io/badge/Load%20Testing-Core%20Methods-4CAF50?style=flat-square)
![Test Automation](https://img.shields.io/badge/Test%20Automation-Fundamentals-blue?style=flat-square)
![Mentoring](https://img.shields.io/badge/Mentoring-QA%20Teams-orange?style=flat-square)
![Java](https://img.shields.io/badge/Java-OOP%20Basics-ED8B00?style=flat-square&logo=java&logoColor=white)
![SQL Advanced](https://img.shields.io/badge/SQL-Advanced-4479A1?style=flat-square)
![Git](https://img.shields.io/badge/Git-Version%20Control-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Essentials-FCC624?style=flat-square&logo=linux&logoColor=black)
![XML and XSD](https://img.shields.io/badge/XML%20and%20XSD-Data%20Formats-005571?style=flat-square)
![Banking Systems](https://img.shields.io/badge/Banking%20Systems-FinTech-6f42c1?style=flat-square)
![Web Development](https://img.shields.io/badge/Web-HTML%20%7C%20CSS%20%7C%20JS-E34F26?style=flat-square&logo=html5&logoColor=white)

---

## 🌍 Career Goals

I am interested in **international projects** where performance, scalability, and system reliability are critical.  
Open to roles focused on **Performance Engineering**, **Non-Functional Testing**, or **System Optimization**.

### 📈 Example: Step Load Test Behavior

```text
Users
500 ┤                         ╭──────────╮
400 ┤                    ╭────╯          │
300 ┤               ╭────╯               │
200 ┤          ╭────╯                    │
100 ┼──────────╯                         ╰──────────
      0s     5m     10m    15m    20m

Response Time increases after saturation point
```

---

> *“Performance problems are rarely about one slow component. They are about how systems behave under pressure.”*
