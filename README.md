# Como Criar uma Stack no AWS CloudFormation

Este guia rápido explica como criar uma stack no AWS CloudFormation, passo a passo, usando um template simples.

---

## O que é uma Stack no CloudFormation?

Uma **stack** é um conjunto de recursos AWS definidos por um arquivo template (JSON ou YAML). Ao criar uma stack, o CloudFormation cria e gerencia esses recursos para você automaticamente.

---

## Passo a Passo para Criar uma Stack

### 1. Prepare o Template CloudFormation

Crie um arquivo template em YAML ou JSON que descreva os recursos que deseja criar.

### 2. Acesse o Console AWS CloudFormation

- Acesse o [Console da AWS](https://aws.amazon.com/console/).
- Pesquise por **CloudFormation** e abra o serviço.

---

### 3. Crie a Stack

- Clique em **Create stack** > **With new resources (standard)**.
- Na seção **Specify template**, faça upload do seu arquivo YAML/JSON ou cole o código diretamente.

---

### 4. Defina os Detalhes da Stack

- Informe um nome para a stack, ex: `MinhaStackExemplo`.
- Preencha parâmetros, se houver (não obrigatório).

---

### 5. Configure Opções (Opcional)

- Adicione tags, defina permissões, configure notificações, etc.

---

### 6. Revise e Crie

- Revise as configurações e clique em **Create stack**.

---

### 7. Acompanhe a Criação

- Aguarde o status da stack mudar para **CREATE_COMPLETE**.

---

### 8. Verifique os Recursos Criados

- Vá ao console do serviço (ex: S3) para verificar os recursos provisionados.

---

**Exemplo simples (YAML) — cria um bucket S3:**

```yaml
Resources:
  MeuBucketS3:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-bucket-exemplo-123456

