# 🚀 Desafio Chibas - API de Estatísticas Financeiras

## 🔥 E aí Samuca!
Chegou seu **terceiro** Desafio Chibas! Dessa vez vamos mergulhar no mundo das APIs REST e fazer uma aplicação MUITO MASSA de processamento de transações financeiras! 

## 📅 Data de Entrega
[Data a definir]

## ⚠️ ATENÇÃO! EXTREMAMENTE IMPORTANTE! ⚠️

# DOCUMENTAÇÃO É SEU MELHOR AMIGO
# NÃO CAIA NO TUTORIAL HELL
# USE A DOCUMENTAÇÃO OFICIAL DO SPRING E STACKOVERFLOW

## 🎯 O Desafio

Samuca, sua missão (e você vai aceitar!) é criar uma API que:
1. Recebe transações financeiras
2. Calcula estatísticas em tempo real
3. Permite limpar os dados quando necessário

O mais legal? Você vai fazer tudo em memória, sem banco de dados! 🧠

## 🛠️ Ferramentas que você vai usar

- Java 8+ ou Kotlin (você escolhe!)
- Spring Boot (framework ANIMAL pra criar APIs)
- Maven ou Gradle (gerenciador de dependências)
- Seu editor favorito
- Muito café ☕

## 📝 Como Começar

1. Primeiro, vai no [Spring Initializr](https://start.spring.io/) e cria seu projeto:
   - Escolhe Maven ou Gradle
   - Java ou Kotlin
   - Spring Boot (última versão)
   - Adiciona a dependência "Spring Web"

2. Baixa o projeto e BORA CODAR! 🚀

## 📋 Regras do Projeto

### Regras Técnicas Importantes! 🔧

1. **GitHub/GitLab:**
   - Criar repositório público
   - NÃO fazer fork de outros projetos
   - Mínimo 3 commits (1 por endpoint)
   - Usar sempre o mesmo usuário nos commits

2. **Código:**
   - Usar EXATAMENTE os nomes de endpoints descritos
   - Trabalhar só com JSON
   - NADA de banco de dados (nem H2, MySQL, PostgreSQL...)
   - NADA de cache (nem Redis, Memcached...)
   - Guardar tudo em memória!

## 🎮 Os Endpoints que você precisa criar

### 1. POST /transacao
Recebe transações assim:
```json
{
    "valor": 123.45,
    "dataHora": "2020-08-07T12:34:56.789-03:00"
}
```

#### Regras da Transação! ⚠️
Só aceita transação se:
- Tiver `valor` e `dataHora` preenchidos
- NÃO for no futuro
- Tiver acontecido em qualquer momento do passado
- NÃO tiver valor negativo
- Valor for maior ou igual a 0

#### Respostas possíveis:
- `201 Created`: Transação aceita! 🎉 (sem corpo)
- `422 Unprocessable Entity`: Transação inválida ❌ (sem corpo)
- `400 Bad Request`: JSON mal formatado 🚫 (sem corpo)

### 2. DELETE /transacao
- Limpa TODAS as transações da memória
- Retorna `200 OK` quando der certo (sem corpo)

### 3. GET /estatistica
Retorna estatísticas dos últimos 60 segundos:
```json
{
    "count": 10,    // quantidade de transações
    "sum": 1234.56, // soma total
    "avg": 123.456, // média
    "min": 12.34,   // menor valor
    "max": 123.56   // maior valor
}
```

#### Detalhes Importantes! 🔍
- Só considera transações dos últimos 60 segundos
- Se não tiver transações, TODOS os valores devem ser `0`
- Retorna `200 OK` com o JSON das estatísticas

## 🌟 Bônus (Quer impressionar? Faz esses aqui!)

1. **Testes Automatizados:** 
   - Testes unitários
   - Testes funcionais
   - Testa os casos de erro também!

2. **Containerização:** 
   - Cria um Dockerfile
   - Não precisa publicar o container

3. **Logs:** 
   - Mostra o que tá acontecendo
   - Ajuda a debugar problemas

4. **Observabilidade:** 
   - Endpoint de healthcheck
   - Monitora a saúde da API

5. **Performance:** 
   - Otimiza o cálculo das estatísticas
   - Mede o tempo de processamento

6. **Tratamento de Erros:** 
   - Mensagens de erro claras
   - Usa as ferramentas do Spring Boot

7. **Documentação da API:** 
   - Usa Swagger ou similar
   - Documenta todos os endpoints

8. **Documentação do Sistema:** 
   - Como buildar
   - Como executar
   - Requisitos do sistema

9. **Configurações:** 
   - Deixa o tempo de 60 segundos configurável
   - Outras configurações úteis

## 💡 Super Dicas

1. Use `OffsetDateTime` pra trabalhar com as datas
2. A classe `DoubleSummaryStatistics` é sua amiga!
3. Testa TODOS os casos de erro possíveis
4. Documenta TUDO que puder
5. Código limpo = código feliz 😊

## 📚 Links Úteis

- [Spring Boot - Documentação Oficial](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- [Spring Web MVC](https://docs.spring.io/spring-framework/docs/current/reference/html/web.html)
- [Java Time API](https://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/spring-boot)

## 🤔 Precisa de ajuda?

- Consulte a documentação
- Use o Stack Overflow
- Peça ajuda pro time
- MAS NÃO CAIA NO TUTORIAL HELL!

Bora codar, Samuca! Mostre pra gente do que você é capaz! 💪
