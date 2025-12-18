# 🚀 Desafio de Performance: BlazeDemo (JMeter)

Este repositório contém a solução do desafio técnico de performance, simulando a compra de passagens aéreas no site [BlazeDemo](https://www.blazedemo.com). O objetivo é validar a escalabilidade e o tempo de resposta do sistema sob carga.

---

## 📊 Critérios de Aceitação (SLA)
Para aprovação, o script deve atingir:
* **Vazão (Throughput):** 250 requisições por segundo (RPS).
* **Tempo de Resposta (90th Percentile):** Inferior a 2 segundos.

---

## 🛠️ Tecnologias Utilizadas
* **Ferramenta:** Apache JMeter 5.x
* **Linguagem:** Java 17
* **CI/CD:** GitHub Actions (Execução automatizada em cada Push)

---

## 📂 Estrutura do Projeto
text
├── .github/workflows/    # Automação do teste no GitHub (CI)
├── scripts/              # Arquivo .jmx do JMeter
├── reports/              # Prints dos resultados e dashboard
└── README.md             # Documentação do projeto

## ⚙️ Como Executar os Testes
### 1. Via Interface Gráfica (GUI) - Apenas para validação
Abra o JMeter.
Clique em File > Open e selecione o arquivo scripts/desafioActPerformance.jmx.
Clique no botão de Play (verde) para validar o fluxo.

### 2. Via Linha de Comando (Non-GUI) - Teste Oficial
Para gerar os resultados reais sem interferência da interface, use o comando na raiz do projeto:
bash
jmeter -n -t scripts/desafioActPerformance.jmx -l results.jtl -e -o reports/dashboard/


## 📊 Relatório Online
Veja os resultados detalhados aqui: [Clique para abrir o Dashboard](https://caducondo.github.io/desafioActPerformance/)