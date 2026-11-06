<div align="center">

<!-- ░░░ HEADER ░░░ -->

# Leonardo

**Engenharia de Dados** · **Sistemas Embarcados** · **Engenharia Elétrica**

`do sensor ao dashboard`

<br/>

![Python](https://img.shields.io/badge/Python-0D1117?style=flat-square&logo=python&logoColor=FFD43B)
![FastAPI](https://img.shields.io/badge/FastAPI-0D1117?style=flat-square&logo=fastapi&logoColor=009688)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0D1117?style=flat-square&logo=postgresql&logoColor=4169E1)
![ESP32](https://img.shields.io/badge/ESP32-0D1117?style=flat-square&logo=espressif&logoColor=E7352C)
![C++](https://img.shields.io/badge/C++-0D1117?style=flat-square&logo=cplusplus&logoColor=00599C)
![Docker](https://img.shields.io/badge/Docker-0D1117?style=flat-square&logo=docker&logoColor=2496ED)

</div>

<br/>

> Estudante de **Engenharia Elétrica na UFRN**, técnico em mecatrônica de formação e
> **estagiário de Engenharia de Dados na Hubbi**, onde construo a plataforma interna de
> operações de dados do maior catálogo de autopeças do Brasil.
>
> O fio que costura tudo: eu gosto de projeto que começa num sensor e termina num gráfico.
> Firmware, pipeline, banco, API e interface — a cadeia inteira.

<br/>

## ⟢ Como as frentes se conectam

```mermaid
flowchart LR
    A["Sensores<br/>tensão · corrente · umidade"]
    B["Firmware<br/>ESP32 · C++"]
    C["Transporte<br/>MQTT · HTTP"]
    D["Ingestão<br/>Celery · Airflow"]
    E["Banco<br/>PostgreSQL · Timescale"]
    F["API<br/>FastAPI"]
    G["Interface<br/>React · TypeScript"]

    A --> B --> C --> D --> E --> F --> G

    classDef hw fill:#210008,stroke:#FF003C,stroke-width:1.5px,color:#FFFFFF
    classDef data fill:#0D1117,stroke:#5B1476,stroke-width:1.5px,color:#FFFFFF
    classDef ui fill:#0D1117,stroke:#995200,stroke-width:1.5px,color:#FFFFFF

    class A,B,C hw
    class D,E,F data
    class G ui
```

<br/>

## `01` Engenharia de Dados

Meu dia a dia. Pipelines de ingestão, qualidade de dados em escala de milhões de
registros e as operações de banco que sustentam o resto da plataforma.

- **Pipelines DAG-driven** — pipelines validadas viram DAGs no Airflow, com blocos
  reaproveitáveis como tasks
- **Qualidade de dados em escala** — EDA, validação de código de barras, normalização e
  deduplicação de catálogo com milhões de linhas
- **Classificação com LLM** — pipelines de categorização com pré-filtro fuzzy antes do
  modelo, para custo previsível
- **Infra de dados** — containers Postgres isolados por dev, cache Redis para consultas
  caras, backup automatizado em S3
- **Agentes de dados** — ferramentas de IA human-in-the-loop que geram SQL auditável em
  vez de executar comandos destrutivos

![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-0D1117?style=flat-square&logo=sqlalchemy&logoColor=D71F00)
![Airflow](https://img.shields.io/badge/Airflow-0D1117?style=flat-square&logo=apacheairflow&logoColor=017CEE)
![Celery](https://img.shields.io/badge/Celery-0D1117?style=flat-square&logo=celery&logoColor=37814A)
![Redis](https://img.shields.io/badge/Redis-0D1117?style=flat-square&logo=redis&logoColor=FF4438)
![Pandas](https://img.shields.io/badge/Pandas-0D1117?style=flat-square&logo=pandas&logoColor=150458)
![AWS S3](https://img.shields.io/badge/AWS_S3-0D1117?style=flat-square&logo=amazons3&logoColor=569A31)

<br/>

## `02` Sistemas Embarcados & Automação

Onde comecei, e o que não larguei. Projetos que saem da bancada e ficam rodando em
casa, no quintal e na casa da família.

- **Firmware** — ESP32/ESP8266 em C++, RTC, válvulas solenoides, estágios com
  transistor para compatibilizar relés *active-low* com GPIO de 3,3 V
- **Telemetria** — MQTT como espinha dorsal, broker próprio, histórico em série
  temporal
- **Hardware** — medição de energia com ATM90E32, transformadores de corrente SCT-013,
  sensores de tensão ZMPT101B, esquemático em KiCad
- **Legado útil** — estabilização de drone com MPU6050, telemetria RS-485/Modbus,
  refrigeração industrial

![C++](https://img.shields.io/badge/C++-0D1117?style=flat-square&logo=cplusplus&logoColor=00599C)
![PlatformIO](https://img.shields.io/badge/PlatformIO-0D1117?style=flat-square&logo=platformio&logoColor=F5822A)
![Arduino](https://img.shields.io/badge/Arduino-0D1117?style=flat-square&logo=arduino&logoColor=00878F)
![MQTT](https://img.shields.io/badge/MQTT-0D1117?style=flat-square&logo=mqtt&logoColor=660066)
![KiCad](https://img.shields.io/badge/KiCad-0D1117?style=flat-square&logo=kicad&logoColor=314CB0)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-0D1117?style=flat-square&logo=raspberrypi&logoColor=A22846)

<br/>

## `03` Engenharia Elétrica

A base que dá sentido às outras duas. Sistemas de potência, instrumentação e sistemas
digitais — é o que me deixa confortável em colocar um protótipo direto na rede 220 V e
em raciocinar sobre potência ativa e reativa antes de escrever uma linha de firmware.

![VHDL](https://img.shields.io/badge/VHDL-0D1117?style=flat-square&logo=v&logoColor=FF003C)
![MATLAB](https://img.shields.io/badge/MATLAB-0D1117?style=flat-square&logo=mathworks&logoColor=E16737)
![LaTeX](https://img.shields.io/badge/LaTeX-0D1117?style=flat-square&logo=latex&logoColor=008080)

<br/>

## ⟢ Projetos

| Projeto | O que é | Frente |
| :--- | :--- | :--- |
| **Analisador de Energia** | Medição mono e trifásica de consumo ativo e reativo com ESP32 + ATM90E32, enviando telemetria para dashboard online. Em incubação como produto. | `embarcados` `dados` |
| **Irrigação Automatizada** | Três zonas independentes com ESP32, RTC e válvulas solenoides, migrando a configuração do firmware para um backend multi-proprietário. | `embarcados` |
| **Automação de Ambiente** | Controle e telemetria via ESP8266 e MQTT, com broker próprio como hub central dos projetos. | `embarcados` |
| **Agente de Duplicatas** | Agente de IA que analisa grupos de registros duplicados e devolve SQL auditável, com validação humana fora do loop. | `dados` |

<br/>

<div align="center">

## ⟢ Atividade

<img src="https://github-readme-stats.vercel.app/api?username=leonardolima013&show_icons=true&hide_border=true&bg_color=0D1117&title_color=FF003C&icon_color=FF003C&text_color=8C8C94&include_all_commits=true" height="160" alt="estatísticas" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=leonardolima013&layout=compact&hide_border=true&bg_color=0D1117&title_color=FF003C&text_color=8C8C94&langs_count=8" height="160" alt="linguagens" />

<br/><br/>

---

### Onde me achar

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0D1117?style=flat-square&logo=linkedin&logoColor=0A66C2)](https://linkedin.com/in/SEU-SLUG-AQUI)
[![Instagram](https://img.shields.io/badge/Instagram-0D1117?style=flat-square&logo=instagram&logoColor=E4405F)](https://instagram.com/leonardo.lima__)
[![Email](https://img.shields.io/badge/Email-0D1117?style=flat-square&logo=gmail&logoColor=EA4335)](mailto:SEU-EMAIL-AQUI)

<sub>`220 V` · `3.3 V` · `5432` — todos no mesmo projeto.</sub>

</div>
