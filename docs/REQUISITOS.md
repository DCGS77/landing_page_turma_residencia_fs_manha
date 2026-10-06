# 📑 Documento de Requisitos — Landing Page da Turma de Residência Full Stack (Manhã)

> **Status:** Em validação  
> **Versão:** 1.0.0  
> **Última atualização:** 06 de Outubro de 2026  
> **Repositório:** `landing_page_turma_residencia_fs_manha`

---

## 🎯 1. Visão Geral e Objetivos do Produto

### 1.1 Objetivo Geral
Desenvolver uma landing page moderna, atrativa e de alta performance com o propósito de servir como vitrine profissional da turma de residentes de desenvolvimento Full Stack (turno manhã). A página visa conectar os alunos recém-formados/em formação ao mercado de tecnologia (empresas de software, recrutadores e gestores de engenharia).

### 1.2 Proposta de Valor
* **Para as Empresas/Recrutadores:** Encontrar talentos de forma rápida, filtrando por competências e tecnologias, com acesso direto a perfis do LinkedIn, GitHub e portfólios individuais.
* **Para os Residentes:** Exposição centralizada de seus perfis profissionais, demonstrando competência técnica, projetos reais entregues e capacidade de trabalho em equipe.
* **Para a Coordenação do Programa:** Documentar e divulgar publicamente os resultados, a qualidade formativa da turma e a metodologia hands-on aplicada.

### 1.3 Personas / Público-Alvo
1. **Tech Recruiters & Analistas de RH:** Buscam desenvolvedores júnior/pleno com perfil qualificado e links diretos para contato e triagem rápida.
2. **Tech Leads & CTOs:** Avaliam a qualidade dos projetos, a maturidade técnica da stack e os repositórios de código dos candidatos.
3. **Comunidade Acadêmica & Alunos:** Acompanham o progresso da turma e compartilham a página em redes sociais.

---

## 🧩 2. Requisitos Funcionais (RF)

| ID | Nome | Descrição | Prioridade |
|---|---|---|:---:|
| **RF-01** | **Hero Section de Apresentação** | Cabeçalho de alto impacto visual com identificação clara da turma (*Residência de Software Full Stack - Manhã*), chamada de valor e botões de ação rápida (*CTA* para "Conhecer Residentes" e "Contatar Turma"). | **Alta** |
| **RF-02** | **Apresentação do Programa** | Seção descritiva explicando a metodologia da residência (projetos práticos, resolução de problemas reais, carga horária e dinâmicas ágeis). | **Média** |
| **RF-03** | **Grid / Galeria de Residentes** | Exibição de cards individuais contendo foto de perfil, nome completo, cargo/foco (Frontend, Backend, Full Stack), resumo de apresentação (bio curta), badges das principais competências e links para redes profissionais (GitHub, LinkedIn, Portfólio pessoal e e-mail). | **Alta** |
| **RF-04** | **Modal de Perfil Detalhado** | Ao clicar em um card de residente, abrir um modal com visualização expandida: trajetória, stack completa, projetos em destaque desenvolvidos durante o programa e botão de contato direto. | **Média** |
| **RF-05** | **Showcase de Projetos em Destaque** | Seção dedicada aos principais projetos práticos desenvolvidos pelos residentes (individuais ou em squads), contendo título, descrição do problema resolvido, tecnologias utilizadas e links para repositório e demo online. | **Média** |
| **RF-06** | **Mural de Tecnologias (Stack da Turma)** | Seção visual com ícones/badges organizadas por categorias (Frontend, Backend, Banco de Dados, DevOps/Ferramentas e Metodologias Ágeis). | **Baixa** |
| **RF-07** | **Canal de Contato & Contratação** | Seção final com links diretos e formulário ou botão de contato para empresas interessadas em contratar residentes ou estabelecer parcerias com o programa. | **Alta** |
| **RF-08** | **Depoimentos / Estatísticas Rápidas** | Métricas da turma (ex.: quantidade de residentes formados, horas de código, projetos entregues) para reforçar a credibilidade do programa. | **Baixa** |

---

## ⚡ 3. Requisitos Não-Funcionais (RNF)

| ID | Requisito | Critério de Aceite |
|---|---|---|
| **RNF-01** | **Responsividade Total** | Layout *Mobile-First*, com experiência fluida e sem quebra visual em celulares, tablets e telas widescreen de desktop. |
| **RNF-02** | **Desempenho e Core Web Vitals** | Carregamento rápido inicial (LCP < 2.0s), uso de imagens comprimidas/otimizadas e carregamento sob demanda (*lazy loading* nos avatares e mídias). |
| **RNF-03** | **Design & UI Premium** | Estética visual moderna (dark/light contrast, tipografia legível, micro-interações suaves ao passar o mouse e estados de foco acessíveis). |
| **RNF-04** | **Desacoplamento de Dados** | Todos os dados de alunos e projetos devem ficar isolados em arquivos estruturados (ex.: `data/residents.json` e `data/projects.json`), permitindo atualizações fáceis sem alterar a estrutura de código. |
| **RNF-05** | **SEO & Social Share** | Tags Open Graph (`og:title`, `og:description`, `og:image`) configuradas para gerar prévias atrativas ao compartilhar o link no LinkedIn e WhatsApp. |
| **RNF-06** | **Acessibilidade (A11y)** | Contrastes de cor em conformidade com WCAG AA, uso de tags semânticas (`<header>`, `<main>`, `<section>`, `<article>`, `<nav>`, `<footer>`) e atributos `alt` em todas as imagens. |

---

## 📁 4. Estrutura de Informação & Arquitetura de Pastas Sugerida

```text
landing_page_turma_residencia_fs_manha/
├── docs/
│   └── REQUISITOS.md       # Este documento de especificação
├── README.md               # Instruções de execução e documentação do projeto
├── .gitignore              # Arquivos e diretórios ignorados pelo Git
├── index.html              # Estrutura semântica da página
├── assets/
│   ├── css/
│   │   ├── variables.css   # Variáveis de design (cores, fontes, espaçamentos)
│   │   ├── styles.css      # Estilos globais e componentes
│   │   └── responsive.css  # Media queries e ajustes móveis
│   ├── js/
│   │   ├── app.js          # Lógica principal e interatividade
│   │   └── modal.js        # Controle de modais e drawer
│   ├── images/
│   │   ├── residentes/     # Fotos de perfil dos alunos
│   │   ├── logos/          # Logos e ilustrações
│   │   └── og-banner.png   # Imagem para compartilhamento social
│   └── data/
│       ├── residents.json  # Base de dados estruturada dos residentes
│       └── projects.json   # Base de dados dos projetos desenvolvidos
```


---

## 📋 5. Checklist de Validação com a Turma e Coordenação

- [ ] A lista de informações solicitadas de cada residente (foto, bio, links, skills) está de acordo com a turma?
- [ ] O formato de contato (direto com os alunos ou através da coordenação/banco de talentos) foi definido?
- [ ] As tecnologias da stack principal representam fielmente a ementa do curso?
- [ ] Os projetos em destaque que entrarão na vitrine foram selecionados?
- [ ] O logo ou identificação oficial da instituição parceira deve ser incluído?
