# 📊 Sistema de Gestão de Infraestrutura (SGI) – Aplicação Web (PHP + SQL)

## 👤 Identificação

**Nome do aluno:** Filipe Fernandes Carneiro
**Disciplina:** REDES – M6 – Programação de Sistemas de Informação  
**Curso:** GPSI – 2.º Ano

## 🎯 Objetivo do Projeto

Este projeto consiste no desenvolvimento de uma aplicação web para a gestão e monitorização de uma infraestrutura de rede, incluindo salas, equipamentos, técnicos e intervenções. A aplicação visa fornecer uma plataforma centralizada para:

*   **Gestão de Recursos:** Registo e organização de salas, equipamentos e técnicos.
*   **Controlo de Intervenções:** Registo e acompanhamento de manutenções e reparações.
*   **Monitorização e Relatórios:** Geração de consultas e relatórios sobre o estado da infraestrutura.
*   **Gestão de Utilizadores:** Controlo de acesso e permissões para diferentes tipos de utilizadores.

A aplicação permite não só consultar informações técnicas, mas também gerir o estado dos equipamentos, registar intervenções e ter uma visão geral da infraestrutura de rede escolar.

## 🧱 Estrutura Geral do Projeto

O projeto está organizado numa estrutura de pastas que tenta separar as configurações, estilos e componentes reutilizáveis, embora a maioria dos ficheiros PHP misture lógica e apresentação. A estrutura principal é a seguinte:

```
m6-fp03/
├── config/             # Ficheiros de configuração da aplicação
│   └── db.php          # Configuração da ligação PDO à base de dados MySQL
├── css/                # Ficheiros de estilo CSS
│   └── style.css       # Estilos globais da aplicação
├── includes/           # Componentes PHP reutilizáveis
│   ├── auth.php        # Lógica de autenticação e verificação de sessão
│   ├── footer.php      # Rodapé HTML (uso inconsistente)
│   └── header.php      # Cabeçalho HTML (uso inconsistente)
├── equipamentos.php    # Gestão de equipamentos (listagem, adição)
├── index.php           # Dashboard principal com visão geral e acesso rápido
├── intervencoes.php    # Gestão de intervenções (listagem, adição)
├── login.php           # Página de autenticação (login e registo)
├── logout.php          # Lógica para terminar a sessão
├── queries.php         # Módulo de relatórios e consultas dinâmicas
├── salas.php           # Gestão de salas (listagem, adição)
├── tecnicos.php        # Gestão de técnicos (listagem, adição)
└── utilizadores.php    # Gestão de utilizadores (listagem, adição, eliminação)
```

## ⚙️ Funcionalidades Desenvolvidas

As principais funcionalidades implementadas no projeto incluem:

*   **Autenticação de Utilizadores:** Sistema de login e registo com gestão de sessões.
*   **Gestão de Salas:** Adição e listagem de salas com detalhes de localização.
*   **Gestão de Equipamentos:** Registo de equipamentos por tipo, marca, modelo e endereço IP, associados a salas.
*   **Gestão de Técnicos:** Registo de técnicos com nome, email e contacto.
*   **Gestão de Intervenções:** Registo de intervenções com data, descrição, equipamento associado e técnico responsável.
*   **Módulo de Relatórios:** Consultas dinâmicas para visualizar equipamentos por sala, histórico de intervenções por equipamento, intervenções por técnico e equipamentos sem intervenções.
*   **Gestão de Utilizadores (Admin):** Funcionalidade para adicionar, listar e eliminar utilizadores (com acesso administrativo).
*   **Interface Responsiva:** Design adaptável a diferentes tamanhos de ecrã, com suporte a tema claro/escuro.

## 🤖 Utilização da Inteligência Artificial (IA)

Durante o desenvolvimento deste projeto, a Inteligência Artificial foi utilizada como uma ferramenta de apoio para otimizar o processo e explorar novas abordagens:

*   **Estruturação de Código:** Apoio na organização de ficheiros e na definição de padrões para a lógica da aplicação.
*   **Queries SQL:** Ajuda na formulação de queries complexas, incluindo `JOIN`s e subconsultas para relatórios.
*   **Interface Gráfica:** Sugestões de design e implementação de componentes visuais para uma experiência de utilizador moderna e responsiva.
*   **Resolução de Problemas:** Assistência na depuração e otimização de código, como ajustes de fuso horário e correção de lógica.
*   **Ideias "Fora da Caixa":** Inspiração para funcionalidades adicionais e melhorias na usabilidade da aplicação.

## ✍️ Trabalho Desenvolvido Manualmente

Apesar do apoio da IA, grande parte do desenvolvimento e refinamento foi realizado manualmente para garantir a qualidade e especificidade do projeto:

*   **Personalização Visual:** Ajustes finos de CSS, cores, ícones e alinhamentos para corresponder aos requisitos estéticos e funcionais.
*   **Lógica de Negócio Específica:** Implementação e adaptação da lógica central para a gestão de infraestruturas, incluindo validações e fluxos de dados.
*   **Estruturação da Base de Dados:** Criação e otimização do esquema da base de dados, incluindo a definição de tabelas e relações para suportar todas as funcionalidades.
*   **Refatoração e Otimização:** Melhoria contínua do código para garantir performance, segurança e manutenibilidade.

## 🚧 Dificuldades Encontradas

O desenvolvimento do projeto apresentou alguns desafios, nomeadamente:

*   **Segurança de Autenticação:** A implementação de um sistema de autenticação seguro, especialmente no que diz respeito ao *hashing* de passwords e proteção contra vulnerabilidades comuns.
*   **Separação de Preocupações:** Manter uma clara separação entre a lógica de negócio, acesso a dados e apresentação em ficheiros PHP, que tendem a misturar estes elementos.
*   **Otimização de Queries:** Garantir que as consultas SQL fossem eficientes, especialmente em cenários de múltiplos `JOIN`s ou loops que poderiam levar a problemas de N+1 queries.
*   **Consistência da Interface:** Assegurar um design responsivo e consistente em todas as páginas, apesar da abordagem de CSS e JavaScript inline em vários ficheiros.

## 📚 Aprendizagens Realizadas

Este projeto proporcionou uma valiosa experiência e aprendizagem em diversas áreas:

*   **PHP e PDO:** Aprofundamento no uso de PHP para desenvolvimento web e na utilização segura do PDO para interação com bases de dados MySQL.
*   **Segurança Web:** Compreensão da importância do *hashing* de passwords, *prepared statements* e outras práticas de segurança para proteger aplicações web.
*   **Design de Base de Dados:** Experiência na criação e otimização de esquemas de bases de dados relacionais.
*   **Desenvolvimento Frontend:** Aplicação de princípios de design responsivo e gestão de temas (claro/escuro) para melhorar a experiência do utilizador.
*   **Gestão de Projetos:** A importância da organização do código, refatoração e otimização para a manutenibilidade e escalabilidade de uma aplicação.

