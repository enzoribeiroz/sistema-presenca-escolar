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
| Entradas | Registro Acadêmico do aluno, disciplina em que esteve ausente e o professor responsável. | 
| Ator | Professor responsável. |
| Saída | Acréscimo no total de faltas do aluno no sistema. |
| Destino | Banco de dados do sistema. |
| Ação | O sistema busca no banco de dados o aluno especificado. Com base nas informações da entrada, cadastra uma falta para esse aluno. Se o percentual de presença estiver entre 75% e 80%, uma notificação via e-mail é emitida para os responsáveis. (ver Notificação). |
| Requer | Todas as informações de entrada são obrigatórias para possível contestação da falta no futuro. |
| Pré-condição | |
| Pós-condição | |
| Efeitos | |

| **Procurar aluno** | **Descrição** |
| :------- | :--- |
| Função |  |
| Descrição | |
| Entradas | | 
| Ator | |
| Saída | |
| Destino | |
| Ação | |
| Requer | |
| Pré-condição | |
| Pós-condição | |
| Efeitos | |

| **Revogar falta** | **Descrição** |
| :------- | :--- |
| Função |  |
| Descrição | |
| Entradas | | 
| Ator | |
| Saída | |
| Destino | |
| Ação | |
| Requer | |
| Pré-condição | |
| Pós-condição | |
| Efeitos | |

| **Gerar relatório** | **Descrição** |
| :------- | :--- |
| Função |  |
| Descrição | |
| Entradas | | 
| Ator | |
| Saída | |
| Destino | |
| Ação | |
| Requer | |
| Pré-condição | |
| Pós-condição | |
| Efeitos | |

| **Enviar notificação** | **Descrição** |
| :------- | :--- |
| Função |  |
| Descrição | |
| Entradas | | 
| Ator | |
| Saída | |
| Destino | |
| Ação | |
| Requer | |
| Pré-condição | |
| Pós-condição | |
| Efeitos | |

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
