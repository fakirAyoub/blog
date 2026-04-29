---
date: "2022-02-02T18:27:58+01:00"
title: "Ayoub Fakir"
hero:
  name: "Ayoub Fakir"
  tagline: "I build data platforms."
  subtitle: "Senior Data Engineer & Architect. Scala · Rust · Go · Python. Distributed systems, functional programming, blockchain."
  certs:
    - "Certified Kubernetes Administrator (CKA-2000-008592-0100)"
  links:
    - { label: "Email", url: "mailto:ayoub@fakir.dev", icon: "mail" }
    - { label: "GitHub", url: "https://github.com/fakirAyoub", icon: "github" }
    - { label: "LinkedIn", url: "https://linkedin.com/in/afakir", icon: "linkedin" }
    - { label: "Medium", url: "https://medium.com/@AyoubFakir/", icon: "medium" }
    - { label: "Twitter", url: "https://twitter.com/the_cryptodata", icon: "twitter" }

experience:
  - company: "Décathlon"
    role: "Senior Data Engineer"
    summary: "Led the migration of Decathlon's data pipelines from Talend/Redshift to Spark/Scala on AWS Databricks."
    bullets:
      - "Lead Data Engineer on the **PerfECO** project, moving Talend/Redshift workloads to a Spark/Scala pipeline."
      - "Data validation at scale (batch + streaming) with Cats / ZIO on POSLog."
      - "Trained team members on Functional Programming and distributed programming."
      - "Migrated Spark/Redshift workloads to **AWS Databricks**."
      - "Built an agent-based distributed streaming system for ingestion."
      - "Member of the architecture committee across multiple Décathlon projects."
    stack: ["Scala", "Spark", "Databricks", "Cats", "ZIO", "AWS"]

  - company: "Glassnode"
    role: "Senior Data Engineer"
    summary: "Led the data platform ingesting and exposing on-chain data from dozens of vendors."
    bullets:
      - "Ingested blockchain data from CoinGecko, CoinMarketCap, Sonar, Dune, ETF feeds and more."
      - "Set up the Medallion architecture in GCP, integrated Snowflake and BigQuery."
      - "Modernized the platform with Airflow (Composer), Spark/Dataproc, dbt."
      - "Introduced Lakehouse formats (Delta / Iceberg)."
    stack: ["GCP", "Snowflake", "BigQuery", "Airflow", "dbt", "Delta", "Iceberg"]

  - company: "Algolia"
    role: "Senior Data Engineer"
    summary: "Petabytes-monthly ingestion and processing on the Data Platform team."
    bullets:
      - "Ingestion via *Kafka* and *Kinesis* from cloud providers and vendors (Salesforce, …)."
      - "Migrated Stitch → Meltano; framework to automate API/DB ingestions (Airflow + deferred ECS Tasks)."
      - "Spark with EMR and AWS Glue. dbt framework for Analytics Engineers."
      - "Led Redshift → Databricks/Snowflake feasibility studies and PoCs."
      - "Lakehouse datalake on Delta Lake + Databricks."
    stack: ["Kafka", "Kinesis", "Spark", "EMR", "Glue", "dbt", "Delta", "Databricks"]

  - company: "Air Liquide"
    role: "Senior DataOps"
    period: "5-month mission"
    summary: "Architected and shipped an in-house Airflow data platform on EKS."
    bullets:
      - "Studied feasibility of an Airflow deployment park on EKS, validated with stakeholders."
      - "Set up DEV/PROD infrastructure via Terraform; deployments via Kubernetes / Helm."
      - "Automated cluster chores via the Airflow API."
      - "Managed cross-team role access; shipped the first dbt / Spark DAGs."
    stack: ["Airflow", "EKS", "Terraform", "Helm", "dbt", "Spark"]

  - company: "Hewlett Packard Enterprise"
    role: "Senior Scala / Data Engineer"
    summary: "Core Team contributor on the Harmony platform."
    bullets:
      - "Maintained and extended the Harmony platform; admin of the team's Kubernetes cluster."
      - "CI/CD with GitHub Actions and Jenkins (legacy)."
      - "Scala features with **ZIO** and **Cats**."
      - "Co-designed the Complex Event Processing engine from scratch."
      - "Messaging via Kafka / Pulsar."
    stack: ["Scala", "ZIO", "Cats", "Kafka", "Pulsar", "Kubernetes"]

  - company: "HydraDX.io"
    role: "DataOps"
    summary: "Infra for Polkadot/Kusama parachains and analytics."
    bullets:
      - "IaC with Terraform, Consul, Rundeck, Ansible, GitHub Actions."
      - "Managed the full project infrastructure (Polkadot + Kusama parachains)."
      - "Analytics infra: Scala/Spark + ZIO on EMR; ad-hoc on Zeppelin / JupyterHub."
      - "Ephemeral testnet deployments for the Runtime team via GitHub Actions + K8s."
    stack: ["Terraform", "Polkadot", "Kusama", "Spark", "ZIO", "Kubernetes"]

  - company: "Alterway Cloud Consulting"
    role: "DataOps & Senior Data Engineer"
    summary: "Lead data engineer for client audits and infra-as-code engagements."
    bullets:
      - "IaC for various clients (Terraform, CDK)."
      - "Data infrastructure and job-performance audits."
      - "Kubernetes ecosystem on AWS."
    stack: ["Terraform", "CDK", "AWS", "Kubernetes"]

  - company: "Andjaro"
    role: "Senior Data Engineer"
    summary: "Industrialized a full data pipeline; built a data catalog for product teams."
    bullets:
      - "Audited the existing data infrastructure."
      - "Pipeline industrialization: Kubernetes, EMR, Airflow, Jenkins, Athena, Glue."
      - "Spark/Scala cleaning + aggregation jobs."
      - "Data Catalog implementation for product teams."
    stack: ["EMR", "Airflow", "Athena", "Glue", "Spark"]

  - company: "Voodoo.io"
    role: "Senior Data Engineer"
    summary: "Daily-TB Spark jobs and a fresh datalake on AWS."
    bullets:
      - "Spark/Scala cleaning and aggregation across terabytes daily."
      - "Built a datalake on AWS; Airflow workflows; Kubernetes."
      - "CI/CD with CircleCI / S3."
    stack: ["Spark", "AWS", "Airflow", "Kubernetes", "CircleCI"]

  - company: "Société Générale"
    role: "Senior Data Engineer"
    period: "via Devoteam"
    summary: "Spark migration and Kafka/NiFi ingestion."
    bullets:
      - "Migrated jobs from Spark 1.x to 2.x."
      - "Ingested data through Kafka and NiFi."
      - "CI/CD with Jenkins / Nexus."
    stack: ["Spark", "Kafka", "NiFi"]

  - company: "AXA Data Innovation Lab"
    role: "Data Engineer"
    period: "via Devoteam"
    summary: "Cloudera platform admin + GDPR compliance project."
    bullets:
      - "Spark/Scala cleaning and normalization of AXA's entities data."
      - "Cloudera cluster admin as part of the Platform Team."
      - "Platform KPIs and YARN resource management."
      - "On-site interventions for internal clients (Hong Kong, Germany, Spain, France)."
      - "**GDPR** compliance project: deletion / update of users' sensitive data on request."
    stack: ["Spark", "Cloudera", "Hadoop", "YARN"]

  - company: "Devoteam Technology"
    role: "Data Consultant"
    summary: "Pre-sales technical lead and internal Big Data trainer."
    bullets:
      - "Tech / architecture lead on business opportunities."
      - "Conducted technical interviews."
      - "Big Data trainer at Devoteam University (Spark, Scala, Python, Hadoop)."
      - "Knowledge Community Leader: internal social-network articles on Big Data."
    stack: ["Spark", "Scala", "Python", "Hadoop"]

  - company: "Crédit Agricole CIB"
    role: "Data Engineer"
    summary: "HortonWorks Hadoop clusters and PoCs."
    bullets:
      - "Built and maintained HortonWorks Hadoop clusters."
      - "Various proofs-of-concept."
    stack: ["Hadoop", "HortonWorks"]

skills:
  - { group: "Programming", items: ["Scala", "Python", "Go", "Rust", "Clojure"] }
  - { group: "Cloud", items: ["AWS", "GCP", "Azure"] }
  - { group: "Data Platforms", items: ["Databricks", "Snowflake"] }
  - { group: "Data", items: ["Hadoop", "Spark", "Hudi", "Delta", "Iceberg"] }
  - { group: "FP / Frameworks", items: ["ZIO", "Cats", "Cats Effect"] }
  - { group: "NoSQL", items: ["Cassandra", "HBase", "DynamoDB", "MongoDB"] }
  - { group: "CI/CD", items: ["GitHub Actions", "CircleCI", "Jenkins", "GitLab CI"] }
  - { group: "Blockchain", items: ["Polkadot", "Hyperledger", "Ethereum"] }

education:
  - { school: "Paris 12 University", degree: "Master's Degree", field: "Engineering of Distributed Systems", year: "2015" }

awards:
  - { title: "Odyssey Hackathon Winner", url: "https://www.youtube.com/watch?v=ZfQoCk4kq3Y", linkLabel: "Watch the demo" }
  - { title: "Morocco Web Awards Winner", url: "https://kezakoo.com", linkLabel: "kezakoo.com" }

teaching:
  - { place: "Paris-Est Créteil University", role: "Lecturer in Data Engineering" }
---
