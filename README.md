# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 09/03/2026  
**Empresa:** Abstergo Industries  
**Responsável:** João Victor Barbosa de Oliveira  

---

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **João Victor Barbosa de Oliveira**. O objetivo do projeto foi elencar 3 serviços AWS com a finalidade de realizar a diminuição de custos imediatos.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

### Etapa 1: 
- **Amazon S3 Intelligent-Tiering**
- **Foco da ferramenta:** Otimização de custos de armazenamento.
- **Descrição de caso de uso:** Movimentação automática de objetos entre camadas de acesso (frequente e infrequente) baseada no padrão de uso, eliminando a necessidade de análise manual e reduzindo custos de storage em até 40% para dados com padrões de acesso desconhecidos.

### Etapa 2: 
- **AWS Lambda**
- **Foco da ferramenta:** Computação Serverless (sem servidor).
- **Descrição de caso de uso:** Migração de microserviços e tarefas de processamento de baixa frequência que antes rodavam em instâncias EC2 ligadas 24/7. Com Lambda, a empresa paga apenas pelo tempo de execução (milissegundos), reduzindo drasticamente o custo de infraestrutura ociosa.

### Etapa 3: 
- **Amazon EC2 Spot Instances**
- **Foco da ferramenta:** Redução de custo em instâncias de computação.
- **Descrição de caso de uso:** Utilização de capacidade ociosa da AWS para ambientes de desenvolvimento, testes e processamento de dados em lote. Esta implementação permite uma economia de até 90% em comparação aos preços de instâncias On-Demand.

---

## Conclusão
A implementação de ferramentas na empresa **Abstergo Industries** tem como esperado **a redução significativa na fatura mensal de nuvem e a otimização do uso de recursos**, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias, como o AWS Cost Explorer, para monitoramento contínuo.

## Anexos
### Anexo 1: Tabela Comparativa de Custos (Estimativa Mensal)

| Recurso (Exemplo: t3.medium) | Custo On-Demand | Custo Spot Instance | Economia (%) | Economia (USD) |
| :--- | ---: | ---: | ---: | ---: |
| 1 Instância (24/7) | \$30,36 | \$9,11 | **70%** | \$21,25 |
| 5 Instâncias (Dev) | \$151,80 | \$45,54 | **70%** | \$106,26 |
| **Total Anual (5 inst.)** | **\$1.821,60** | **\$546,48** | **70%** | **\$1.275,12** |

### Anexo 2: Política de Segurança (IAM JSON)
```json
{
  "Version": "2012-10-17",
  "Statement": [{
      "Effect": "Allow",
      "Action": ["s3:GetObject", "s3:PutObject"],
      "Resource": "arn:aws:s3:::bucket-abstergo/*"
  }]
}
```

**Assinatura do Responsável pelo Projeto:**

_________________________________________________  
**João Victor Barbosa de Oliveira**
