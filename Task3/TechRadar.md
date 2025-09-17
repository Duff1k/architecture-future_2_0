## Технический радар

| Кольцо (Adopt / Trial / Assess / Hold) | Технологии и практики                            | Статус / комментарий                                             |
| -------------------------------------- | ------------------------------------------------ | ---------------------------------------------------------------- |
| **Adopt (используем)**                 | Microsoft SQL Server 2008 (Legacy DWH)           | Временно, только как источник через CDC до миграции              |
|                                        | Power BI                                         | Основной инструмент BI; будет интегрирован с семантическим слоем |
|                                        | Apache Camel (ESB)                               | Сохраняется до миграции на event-driven архитектуру              |
|                                        | Python (AI-сервисы)                              | Базовый стек ML/AI                                               |
| **Trial (пилотируем)**                 | Lakehouse (Delta Lake / Apache Iceberg)          | Запуск пилотных пайплайнов в Raw/Refined                         |
|                                        | Airflow/Dagster                                  | Оркестрация ELT; сравнение для выбора целевого стандарта         |
|                                        | Kafka/Redpanda                                   | Пилот CDC и стриминга из финтеха и фармы                         |
|                                        | Data Catalog + Lineage (OpenMetadata, DataHub)   | Пилот внедрения для топ-датасетов                                |
|                                        | ABAC/RBAC + DLP                                  | Пилот политики доступа и маскирования                            |
|                                        | Semantic Layer (dbt metrics / Cube / AtScale)    | Пилот для топ-30 KPI                                             |
| **Assess (оцениваем)**                 | Feature Store (Feast/Tecton)                     | Для AI-фичей и переиспользования моделей                         |
|                                        | MDM/Customer 360 (Reltio / Semarchy)             | Анализ целевых решений для мастера данных                        |
|                                        | EDA/API-first (AsyncAPI + schema registry)       | Оценка для долгосрочной замены Camel                             |
|                                        | Observability (Monte Carlo / Soda / OpenLineage) | Выбор DQ/Observability платформы                                 |
| **Hold (выводим из эксплуатации)**     | Power Builder                                    | Планируется деактивация интерфейсов, замена на веб-порталы       |
|                                        | Monolithic ETL в SQL 2008                        | Будет демонтирован после миграции логики в оркестрацию           |
