<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;Sistema de Presenças&gt;*
</center></font>

>*Observação 1: A estrutura inicial deste documento é só um exemplo. O seu grupo deverá alterar esta estrutura de acordo com o que está sendo solicitado na disciplina.*

>*Observação 2: O índice abaixo não precisa ser editado se você utilizar o Visual Studio Code com a extensão **Markdown All in One**. Essa extensão atualiza o índice automaticamente quando o arquivo é salvo.*

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Enzo Ribeiro - 10418262 
* Gabriel Ken Kazama Geronazzo - 10418247 
* Lucas Pires de Camargo Sarai - 10418013
* Lucas Zanini da Silva - 10417361
  
# Descrição do Projeto

A Escola Infinito necessita de um sistema para controlar as presenças de seus alunos, pois a operação ainda é realizada totalmente em papel. Assim, esse projeto visa montar essa aplicação de forma a atender todos os requisitos e auxiliar a instituição em seu dia a dia.

# Análise de Requisitos Funcionais e Não-Funcionais

_Requisitos não funcionais:_<br>
–	Acessibilidade<br>
–	Segurança<br>
–	Desempenho
<br><br>
_Requisitos funcionais:_<br>
–	Registro de faltas<br>
–	Relatórios de faltas<br>
–	Notificações<br>
–	Acesso a partir de qualquer dispositivo via web (responsivo)


# Diagrama de Atividades

Disponível em [here](./diagramas/diagrama-de-atividades.png)

# Diagrama de Casos de Uso

*&lt;Diagrama para visualizar o comportamento dos atores&gt;*

# Descrição dos Casos de Uso

| **Registrar falta** | **Descrição** |
| :------- | :--- |
| Função | Cadastrar a ausência(falta) de um aluno em uma disciplina. |
| Descrição | Registra no sistema que o aluno estava ausente em uma aula, acrescendo essa falta ao total de faltas do aluno. |
| Entradas | Registro Acadêmico do aluno(RA), disciplina em que esteve ausente e o professor responsável. | 
| Atores | *Ativo*: Professor responsável  *Passivo*: Responsável|
| Saída | Acréscimo no total de faltas do aluno no sistema. |
| Destino | Banco de dados do sistema (e responsável - Efeitos colaterais).|
| Ação | O sistema busca no banco de dados o aluno especificado. Com base nas informações da entrada, cadastra uma falta para esse aluno e calcula o percentual de presença. Se o percentual de presença estiver entre 75% e 80%, uma notificação via e-mail é emitida para os responsáveis. (ver Notificação). |
| Requer | Todas as informações de entrada são obrigatórias para possível contestação da falta no futuro. |
| Pré-condição | O aluno estar matriculado, aluno estar na disciplina e o aluno estar ausente na aula em que pretende-se registrar a falta. |
| Pós-condição | Verificar se a falta foi registrada. |
| Efeitos | Caso a porcentagem de presença do aluno esteja entre 75% e 80%, uma notificação deve ser enviada aos responsáveis. |

| **Revogar falta** | **Descrição** |
| :------- | :--- |
| Função | Remover do banco de dados a ausência(falta) cadastrada para um aluno em uma disciplina. |
| Descrição |Remove uma falta registrada para um aluno caso a falta tenha sido justificada (por exemplo, atestado), recalculando o total de faltas do aluno.|
| Entradas | Registro Acadêmico(RA) do aluno, disciplina em que esteve registrado como ‘ausente’ e o professor responsável. | 
| Ator | Professor responsável. |
| Saída | Decréscimo no total de faltas do aluno no sistema. |
| Destino | Banco de dados do sistema. |
| Ação | O sistema busca no banco de dados o aluno especificado com base no RA. Com base nas informações da entrada, busca a falta armazenada no sistema. Retira essa falta, atualizando no banco de dados o total de faltas. |
| Requer | Todas as informações de entrada são obrigatórias, visando realizar a busca do aluno no banco de dados. |
| Pré-condição | O aluno estar matriculado, aluno estar na disciplina e o aluno estar registrado como ‘ausente’. |
| Pós-condição |Verificar se a falta foi revogada. |
| Efeitos | Nenhum. |

| **Gerar relatório** | **Descrição** |
| :------- | :--- |
| Função | Criar um relatório em formato PDF para que os professores ou responsáveis vejam informações sobre a presença de um aluno (responsáveis e professores), turma, disciplina ou série (apenas professores). |
| Descrição | Gera um arquivo com dados da presença do grupo selecionado, dependendo da requisição e permissão feita pelo responsável ou professor. Caso um responsável tente gerar o relatório, apenas os dados do seu respectivo aluno serão expostos, caso seja um professor, ele deve indicar o que busca no relatório, uma turma, série ou disciplina. |
| Entradas | Aluno, turma, série ou disciplina. | 
| Ator | Professor ou responsável. |
| Saída | Relatório em formato PDF. |
| Destino | Tela de informações gerais do sistema. |
| Ação | O sistema busca as faltas de uma lista de alunos conforme a seleção determinada pelo usuário e suas permissões. Por exemplo, caso o professor busque um relatório de faltas para uma turma específica, o sistema busca todos os alunos da turma, seus respectivos indicadores de presença e sumariza as informações num único relatório para o professor. |
| Requer | 1 aluno cadastrado no sistema de presenças. |
| Pré-condição | No filtro de seleção de alunos, há pelo menos 1 aluno cadastrado. |
| Pós-condição | Nenhuma |
| Efeitos | Nenhum |

| **Enviar notificação** | **Descrição** |
| :------- | :--- |
| Função | Enviar um comunicado via e-mail para o(s) responsável(is) de um aluno. |
| Descrição |Envia uma notificação ao(s) responsável(is) informando que o percentual de presença do aluno está próximo de 75%, o percentual limite para não reprovar. |
| Entradas |Registro Acadêmico(RA) do aluno, e-mail do(s) responsável(is). | 
| Ator |Sistema. |
| Saída | E-mail enviado ao(s) responsável(is).|
| Destino | Caixa de Entrada do E-mail do(s) responsável(is).|
| Ação | O sistema busca no banco de dados o aluno especificado com base no RA. Com base no e-mail relacionado ao(s) responsável(is) desse aluno, envia o comunicado. |
| Requer | Todas as informações de entrada são obrigatórias, visando realizar a busca do busca do e-mail de destino. |
| Pré-condição | O aluno estar matriculado, ter um responsável cadastrado, ter menos de 80% de presença.|
| Pós-condição |O e-mail ser enviado e o(s) responsável(is) receber(em). |
| Efeitos | Nenhum. |

# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
