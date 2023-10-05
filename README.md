# EngSoftl
Bem vindo ao repositório do componente curricular Engenharia de Software I, do curso de ciência da computação da Unochapecó.

# UNIVERSIDADE COMUNITÁRIA DA REGIÃO DE CHAPECÓ - UNOCHAPECÓ
# ESCOLA POLITÉCNICA 

## Sistema de pronto atendimento para hospital

### Chapecó, 2023

# 1 Introdução
## 1.1 Resumo do projeto 
  O paciente vai à recepcionista, que pede documentos e convênios médicos, se houver. Ela consulta a identidade e o histórico de consultas. Em seguida, o paciente é levado para a triagem, realizada por uma enfermeira. A profissional faz a anamnese: afere os sinais vitais e classifica o risco clínico, que determina o tempo de espera do paciente.
  Conforme o quadro clínico verificado na anamnese, o paciente recebe classificações: vermelha (atendimento emergencial), laranja (atendimento urgencial, até 10 minutos), amarela (risco não imediato, até uma hora), verde (pouco urgente, até duas horas) e azul (sem urgência, até quatro horas).
  Após a triagem, o paciente vai até a sala de espera, onde será chamado por outra enfermeira dentro do horário referente ao seu risco clínico. Posteriormente, o paciente e o prontuário são conduzidos ao consultório médico. Há o atendimento e o enfermo passa para a segunda etapa: ter alta com medicação, ter alta com exames ou ser internado. 
## 1.2 Plataforma de desenvolvimento
## 1.3 Plataforma de operação
## 1.4 Definições e siglas
## 1.5 Perspectiva do produto
### 1.5.1 Modos de operação
### 1.5.2 Requisitos de adaptação ao ambiente
## 1.6 Funções do produto
## 1.7 Características dos usuários
## 1.8 Restrições
## 1.9 Hipótese de trabalho

# 2 Requisitos específicos
## 2.1 Interfaces externas
### 2.1.1 Visão geral
### 2.1.2 Requisitos para interfaces gráficas de usuário
## 2.2 Requisitos funcionais
### 2.2.1 Diagramas de casos de uso
@startuml
actor Paciente #0000FF
actor Recepcionista #FF0000
actor Enfermeira1 #FF0000
actor Enfermeira2 #FF0000
actor Médico #FF0000
rectangle "Sistema de Pronto Atendimento" {
usecase "Entregar documentos" as entregar #00FF00
usecase "Conferir documentos" as conferir #00FF00
usecase "Chamar para triagem e fazer anamnese" as triagem #00FF00
usecase "Classificar risco clínico" as classificar #00FF00
usecase "Chamar para consultório" as consultorio #00FF00
usecase "Examinar paciente" as examinar #00FF00
usecase "Dar alta com medicação" as medicacao #00FF00
usecase "Dar alta com exames" as exames #00FF00
usecase "Internar o paciente" as internar #00FF00
}
Paciente -right- entregar #0000FF
Recepcionista -left- conferir #FF0000
Enfermeira1 -left- triagem #FF0000
Enfermeira1 -left- classificar #FF0000
Enfermeira2 -left- consultorio #FF0000
Médico -left- examinar #FF0000
Médico -left- medicacao #FF0000
Médico -left- exames #FF0000
Médico -left- internar #FF0000
entregar ..> conferir #000000
conferir ..> triagem #000000
triagem ..> classificar #000000
classificar ..> consultorio #000000
consultorio ..> examinar #000000
examinar ..> medicacao #000000
examinar ..> exames #000000
examinar ..> internar #000000
note right of classificar
- Vermelho (atendimento emergencial)
- Laranja (atendimento urgencial, até 10 minutos)
- Amarelo (risco não imediato, até uma hora)
- Verde (pouco urgente, até duas horas)
- Azul (sem urgência, até quatro horas)
end note
@enduml

### 2.2.2 Fluxos dos casos de uso
## 2.3 Requisitos não-funcionais
### 2.3.1 Requisitos de desempenho
### 2.3.2 Requisitos de dados persistentes
### 2.3.3 Restrições ao desenho
### 2.3.4 Atributos de qualidade
## 2.4 Objeto/ Classes
### 2.4.1 Modelo conceitual/ Classes de análise/ Modelo de domínio
### 2.4.2 DSS - Diagramas de sequência do sistema
### 2.4.3 Contratos
### 2.4.4 Classes de implementação

# 3 Análise de UCP




