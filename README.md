# 🚀 Apache Kafka Real-Time Data Pipeline

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Kafka](https://img.shields.io/badge/Apache_Kafka-2.8+-black?logo=apachekafka)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)

> **Özet:** Bu proje, yüksek hacimli verileri gerçek zamanlı olarak işlemek, dönüştürmek ve analiz etmek için tasarlanmış ölçeklenebilir bir **Apache Kafka** ekosistemidir.

---

## 📋 İçindekiler

- [Proje Hakkında](#-proje-hakkında)
- [Mimari](#-mimari)
- [Özellikler](#-özellikler)
- [Gereksinimler](#-gereksinimler)
- [Kurulum](#-kurulum)
- [Kullanım](#-kullanım)
- [Yapılandırma](#-yapılandırma)
- [Katkıda Bulunma](#-katkıda-bulunma)
- [Lisans](#-lisans)

---

## 📖 Proje Hakkında

Bu repo, dağıtık sistemlerde veri tutarlılığını sağlamak ve olay tabanlı (event-driven) mimarileri desteklemek amacıyla geliştirilmiştir. **Producer** servisleri veriyi üretir, **Kafka Broker** kümeleri veriyi güvenle saklar ve **Consumer** grupları veriyi işleyerek [Hedef Veritabanı/Servis]'e yazar.

### Kullanılan Teknolojiler
* **Core:** Apache Kafka, Zookeeper
* **Backend:** [Python / Java / Go - Burayı Düzenle]
* **Containerization:** Docker & Docker Compose
* **Veritabanı:** [PostgreSQL / MongoDB / Elasticsearch - Burayı Düzenle]

---

## 🏗 Mimari

Sistemin veri akış diyagramı aşağıdadır:

```mermaid
graph LR
    A[📡 Data Source / API] -->|JSON Logs| B(🚀 Producer Service)
    B -->|Topic: logs-stream| C{🔥 Apache Kafka Cluster}
    C -->|Group: analytics| D(⚙️ Consumer A - Analytics)
    C -->|Group: storage| E(💾 Consumer B - DB Writer)
    D --> F[📊 Dashboard]
    E --> G[(🗄️ Database)]
