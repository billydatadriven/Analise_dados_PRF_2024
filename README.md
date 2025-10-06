# 🚗 Análise de Dados PRF 2024 - Redução de Acidentes nas Rodovias Federais

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📋 Sobre o Projeto

Este projeto realiza uma análise abrangente dos dados de acidentes de trânsito nas rodovias federais brasileiras, utilizando dados públicos da Polícia Rodoviária Federal (PRF) do ano de 2024. O objetivo principal é identificar padrões e fatores que contribuem para acidentes, fornecendo insights acionáveis para redução de ocorrências e otimização de recursos preventivos.

### 🎯 Objetivos

- **Primário:** Reduzir o número de acidentes nas rodovias federais
- **Secundário:** Diminuir mortalidade e ferimentos graves
- **Terciário:** Otimizar recursos de fiscalização e prevenção

## 🔬 Metodologia

O projeto segue a metodologia **CRISP-DM** (Cross-Industry Standard Process for Data Mining), garantindo uma abordagem estruturada e sistemática:

1. **Business Understanding** - Entendimento do Negócio
2. **Data Understanding** - Entendimento dos Dados  
3. **Data Preparation** - Preparação dos Dados
4. **Modeling** - Modelagem
5. **Evaluation** - Avaliação
6. **Deployment** - Implantação

## 📊 Dataset

### Fonte dos Dados
- **Origem:** Polícia Rodoviária Federal (PRF)
- **Período:** Janeiro a Dezembro de 2024
- **Registros:** 73.156 acidentes
- **Variáveis:** 30 colunas
- **Acesso:** [Dados Abertos da PRF](https://www.gov.br/prf/pt-br/acesso-a-informacao/dados-abertos/dados-abertos-da-prf)

### Principais Variáveis

| Categoria | Variáveis |
|-----------|-----------|
| **Identificação** | id, data_inversa, horario, dia_semana |
| **Localização** | uf, br, km, municipio, latitude, longitude |
| **Características** | causa_acidente, tipo_acidente, classificacao_acidente |
| **Contexto** | fase_dia, condicao_metereologica, tipo_pista, tracado_via |
| **Consequências** | pessoas, mortos, feridos_leves, feridos_graves, ilesos, veiculos |

## 🗂️ Estrutura do Projeto

```
Analise dados PRF/
├── dados/
│   ├── raw/                    # Dados brutos
│   │   ├── Dados_PRF_2023.csv
│   │   └── Dados_PRF_2024.csv
│   └── processed/              # Dados processados
│       └── abt01.csv
├── prf_ven/                    # Ambiente virtual Python
├── C1_Business_understanting_PRF_2024.ipynb    # Entendimento do Negócio
├── C2_Understanding_PRF_2024.ipynb             # Entendimento dos Dados
├── C3_Preparation_modeling.ipynb               # Preparação e Modelagem
├── C4_Evaluation_deployment.ipynb              # Avaliação e Implantação
├── C5_Conclusion.ipynb                         # Conclusões
└── README.md                   # Este arquivo
```

## 🛠️ Tecnologias Utilizadas

### Linguagem e Ambiente
- **Python 3.11+**
- **Jupyter Notebook**
- **Ambiente Virtual** (prf_ven)

### Bibliotecas Principais
```python
pandas          # Manipulação e análise de dados
numpy           # Computação numérica
matplotlib      # Visualização de dados
seaborn         # Visualização estatística
```

## 🚀 Como Executar

### Pré-requisitos
- Python 3.11 ou superior
- Git (para clonar o repositório)

### Instalação

1. **Clone o repositório:**
```bash
git clone https://github.com/seu-usuario/analise-dados-prf.git
cd analise-dados-prf
```

2. **Crie e ative o ambiente virtual:**
```bash
# Windows
python -m venv prf_ven
prf_ven\Scripts\activate

# Linux/Mac
python -m venv prf_ven
source prf_ven/bin/activate
```

3. **Instale as dependências:**
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

4. **Inicie o Jupyter Notebook:**
```bash
jupyter notebook
```

### Ordem de Execução

Execute os notebooks na seguinte sequência:

1. `C1_Business_understanting_PRF_2024.ipynb` - Contexto e objetivos
2. `C2_Understanding_PRF_2024.ipynb` - Exploração inicial dos dados
3. `C3_Preparation_modeling.ipynb` - Preparação e análise
4. `C4_Evaluation_deployment.ipynb` - Avaliação dos resultados
5. `C5_Conclusion.ipynb` - Conclusões e recomendações

## 📈 Principais Descobertas

### Padrões Temporais
- Concentração de acidentes em horários específicos
- Variação por dia da semana
- Sazonalidade ao longo do ano

### Distribuição Geográfica
- Identificação de hotspots críticos
- BRs com maior incidência
- Estados mais afetados

### Fatores de Risco
- Principais causas de acidentes
- Condições meteorológicas mais perigosas
- Tipos de pista com maior risco

### Gravidade dos Acidentes
- Padrões de mortalidade
- Tipos de acidentes mais letais
- Fatores associados à gravidade

## 🎯 Recomendações

### Ações Imediatas
1. **Intensificar fiscalização** nos horários e locais de maior incidência
2. **Campanhas educativas** focadas nas principais causas
3. **Melhorias na infraestrutura** dos trechos críticos

### Estratégias de Longo Prazo
1. **Sistema de monitoramento** em tempo real
2. **Modelos preditivos** para prevenção
3. **Integração de dados** com outras fontes (DETRAN, IBGE)

## 📊 Qualidade dos Dados

### Características do Dataset
- ✅ **Sem duplicatas:** 0 registros duplicados
- ✅ **Período completo:** Dados de janeiro a dezembro 2024
- ✅ **Consistência:** Tipos de dados adequados
- ⚠️ **Valores ausentes:** Análise detalhada nos notebooks

### Limitações
- Dados limitados à PRF (não inclui vias estaduais/municipais)
- Possível subnotificação em algumas regiões
- Dependência da qualidade do registro inicial

## 🤝 Contribuições

Contribuições são bem-vindas! Para contribuir:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📝 Próximos Passos

### Melhorias Técnicas
- [ ] Implementar modelos de machine learning
- [ ] Criar dashboard interativo
- [ ] Automatizar pipeline de dados
- [ ] Integrar APIs de dados externos

### Expansão da Análise
- [ ] Incluir dados históricos (2020-2023)
- [ ] Análise de séries temporais
- [ ] Correlação com dados socioeconômicos
- [ ] Análise geoespacial avançada

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👥 Autor

**Billy Reis**
- GitHub: [@billy-reis](https://github.com/billydatadriven)
- LinkedIn: [Billy Reis](https://www.linkedin.com/in/alanbillyteixeirareis/)

## 🙏 Agradecimentos

- **Polícia Rodoviária Federal** pelos dados públicos disponibilizados
- **PoD Academy** pelo suporte educacional
- **Comunidade Python** pelas ferramentas utilizadas

## 📞 Contato

Para dúvidas, sugestões ou colaborações:
- 💼 LinkedIn: [Billy Reis](https://www.linkedin.com/in/alanbillyteixeirareis/)

---

**⚠️ Importante:** Este projeto tem fins educacionais e de pesquisa. As análises e recomendações devem ser validadas por especialistas antes de implementação em políticas públicas.

**📊 Dados atualizados:** Dezembro 2024  
**🔄 Última atualização do README:** Janeiro 2025