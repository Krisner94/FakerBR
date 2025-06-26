# FakerBR – Gerador de Dados Fake Realistas para o Brasil 🇧🇷

Biblioteca Java para geração de dados falsos, válidos e realistas, com foco no padrão brasileiro (CPF, CNPJ, CEP, nomes, etc). Ideal para testes, simulações e populamento de bases de dados.

---

## 📦 Instalação

```xml
<!-- Exemplo Maven -->
<dependency>
  <groupId>br.com.faker</groupId>
  <artifactId>fakerbr</artifactId>
  <version>1.0.0</version>
</dependency>
```

---

## 🧑 Pessoa Física

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.nome().masculino()`                  | Gera nome masculino                              |
| `faker.nome().feminino()`                   | Gera nome feminino                               |
| `faker.nome().sobrenome()`                  | Gera sobrenome aleatório                         |
| `faker.nome().completo()`                   | Nome + sobrenome com sexo atribuído corretamente |
| `faker.cpf().gerar()`                       | Gera CPF válido                                  |
| `faker.rg().gerar()`                        | Gera RG fictício                                 |
| `faker.sexo().gerar()`                      | Retorna 'M' ou 'F'                               |
| `faker.dataNascimento().gerar()`            | Data de nascimento realista                      |
| `faker.email().comNome(String nome)`        | Gera e-mail a partir do nome                     |
| `faker.telefone().celular()`                | Celular com DDD                                  |
| `faker.telefone().fixo()`                   | Telefone fixo com DDD                            |
| `faker.nacionalidade().gerar()`             | Ex: "Brasileiro", "Brasileira"                   |
| `faker.estadoCivil().gerar()`               | Ex: "Solteiro", "Casado", etc.                   |

---

## 🏢 Pessoa Jurídica

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.cnpj().gerar()`                      | Gera CNPJ válido                                 |
| `faker.razaoSocial().gerar()`               | Ex: "Comercial XPTO Ltda."                       |
| `faker.nomeFantasia().gerar()`              | Nome fictício de empresa                         |
| `faker.ie().gerar()`                        | Inscrição estadual                               |
| `faker.setor().gerar()`                     | Ex: "Comércio", "Serviços", etc.                 |

---

## 🏠 Endereço

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.endereco().cep()`                    | Gera CEP realista ou válido                      |
| `faker.endereco().rua()`                    | Nome de rua comum no Brasil                      |
| `faker.endereco().bairro()`                 | Nome de bairro                                   |
| `faker.endereco().numero()`                 | Número de residência (1 a 9999)                  |
| `faker.endereco().cidade()`                 | Cidade real do Brasil                            |
| `faker.endereco().estado()`                 | Estado (sigla ou nome)                           |
| `faker.endereco().completo()`               | Endereço completo realista                       |

---

## 💳 Financeiro e PIX

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.pix().cpf()`                         | Gera chave PIX CPF                               |
| `faker.pix().email()`                       | Gera chave PIX e-mail                            |
| `faker.pix().aleatoria()`                   | Gera chave PIX aleatória                         |
| `faker.banco().nome()`                      | Nome de banco brasileiro                         |
| `faker.banco().codigo()`                    | Código do banco (ex: "001" para Banco do Brasil) |
| `faker.cartaoCredito().numero()`            | Gera número de cartão fictício                   |
| `faker.cartaoCredito().bandeira()`          | Ex: "Visa", "MasterCard"                         |

---

## 📋 Perfil completo

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.perfil().pessoaFisica()`             | Gera objeto com nome, sexo, CPF, e-mail, etc.    |
| `faker.perfil().pessoaJuridica()`           | Gera objeto com CNPJ, razão social, endereço     |
| `faker.perfil().clienteEcommerce()`         | Gera perfil simulado de cliente                  |
| `faker.perfil().funcionarioEmpresa()`       | Perfil fictício de funcionário                   |

---

## 🧠 Dados Demográficos

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.profissao().gerar()`                 | Profissão comum no Brasil                        |
| `faker.religiao().gerar()`                  | Ex: "Católico", "Evangelico", etc.               |
| `faker.escolaridade().gerar()`              | Ex: "Ensino Médio", "Superior Completo", etc.    |

---

## ⚙️ Utilitários

| Método                                      | Descrição                                         |
|---------------------------------------------|--------------------------------------------------|
| `faker.data().aleatoria(min, max)`          | Data entre dois limites                          |
| `faker.numero().entre(min, max)`            | Número inteiro ou decimal aleatório              |
| `faker.uuid().gerar()`                      | UUID v4 aleatório                                |
| `faker.booleano().aleatorio()`              | true ou false                                    |
| `faker.lorem().frase(int palavras)`         | Frase tipo Lorem Ipsum em português              |
| `faker.export().paraJson()`                 | Exporta para JSON                                |
| `faker.export().paraCsv()`                  | Exporta para CSV                                 |

---

## 📦 Extras

- Suporte a geração em massa:
    - `faker.pessoas().gerarLista(int quantidade)`
    - `faker.empresas().gerarLista(int quantidade)`
- Possibilidade de incluir SQLite embutido com base nacional (CEPs, cidades, bancos, etc.)
- Pode ser usado via API