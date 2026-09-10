# Declaracao-IR

Planilha estruturada em Excel para **coleta e organização dos dados necessários à Declaração de Imposto de Renda Pessoa Física (IRPF)**.

O objetivo é substituir o processo caótico de juntar informes, extratos e dados cadastrais em papéis e e-mails soltos por um único arquivo padronizado, validado e pronto para ser entregue ao contador ou usado no preenchimento do programa da Receita Federal.

---

## 📌 Sobre o projeto

Todo ano o contribuinte precisa reunir a mesma coisa: dados cadastrais, informes de rendimentos de cada banco e o histórico de entradas mês a mês. O `Lion App` organiza esse levantamento em três etapas numeradas, com campos pré-formatados (CPF, CEP, telefone, moeda) e listas suspensas que impedem preenchimento inválido.

**Problema que resolve:** perda de tempo e erro de digitação na fase de coleta de dados do IRPF.

---

## 📂 Estrutura da planilha

| Aba | Função |
|-----|--------|
| **Titular** | 1. Dados cadastrais do contribuinte — nome, CPF, nascimento, título de eleitor, cônjuge, endereço, contatos e três indicadores de situação (alterações desde a última entrega, dependente cônjuge, residente no exterior). |
| **Informes** | 2. Informes de rendimentos bancários — até 3 instituições, com banco, valor atual, referência do arquivo anexo e **total consolidado automaticamente**. |
| **Notas** | 3. Lançamento das entradas mês a mês — data, categoria (Holerite / CNPJ / Freelance) e valor. |
| **Tabelas** | Aba auxiliar (oculta) com a lista oficial de bancos usada pelas listas suspensas. |

---

## ⚙️ Recursos técnicos aplicados

- **Validação de dados (listas suspensas)**
  - `SIM / NÃO` nos indicadores de situação da aba *Titular*
  - `Holerite / CNPJ / Freelance` na coluna Categoria da aba *Notas*
  - Lista de instituições financeiras alimentada pela aba *Tabelas*
- **Formatação numérica personalizada** — máscaras automáticas para CPF (`000.000.000-00`), CEP (`00000-000`), telefone fixo e celular, e moeda em Real (`R$ #.##0,00`)
- **Fórmula de consolidação** — `=SOMA(...)` totalizando os saldos dos bancos informados
- **Aba de apoio oculta** — separa dados de referência da interface de preenchimento
- **Células mescladas e hierarquia visual** — títulos, subtítulos de instrução e blocos numerados para orientar o usuário

---

## ▶️ Como usar

1. Baixe o arquivo `Lion_App.xlsx` (ou clone o repositório).
2. Abra no **Microsoft Excel**, **LibreOffice Calc** ou **Google Sheets**.
3. Preencha as abas na ordem: **Titular → Informes → Notas**.
4. Nos campos com seta ▼, selecione uma das opções da lista.
5. Na aba *Informes*, informe o nome do PDF do informe de rendimentos no campo **ANEXO** e mantenha os arquivos na mesma pasta da planilha.
6. O campo **TOTAL** é calculado automaticamente — não edite.

> ⚠️ Os dados presentes no arquivo são **fictícios**, apenas para demonstração. Substitua-os pelos seus antes de usar.

---

## 🛠️ Requisitos

- Microsoft Excel 2016 ou superior · LibreOffice Calc · Google Sheets
- Nenhuma macro, complemento ou instalação adicional

---

## 🚀 Melhorias futuras

- [ ] Número ilimitado de bancos (hoje são 3 blocos fixos)
- [ ] Aba de **saídas/despesas dedutíveis** (saúde, educação, previdência)
- [ ] Dashboard com gráficos de entradas por categoria e por mês
- [ ] Cálculo estimado do imposto devido com base nas faixas vigentes
- [ ] Exportação/versão em Google Sheets com preenchimento por formulário

---

## 👤 Autor

**Luccas Pessuto Borges Lopes**

---

## 📄 Licença

Distribuído sob a licença MIT. Uso livre para fins educacionais.
