# FisicApp — Experimento de Desenvolvimento Assistido por IA

Repositório do experimento prático do Trabalho de Conclusão de Curso (TCC) do curso de **Engenharia da Computação** da **Universidade Federal do Vale do São Francisco (UNIVASF)**.

---

## Sobre o experimento

Este repositório documenta o desenvolvimento de um aplicativo mobile de ensino de física (**FisicApp**) utilizando duas ferramentas de desenvolvimento assistido por Inteligência Artificial, com o objetivo de comparar a qualidade, consistência e eficiência do código gerado em cada ambiente.

Ambas as ferramentas utilizaram o **mesmo modelo de linguagem (GPT-5)**, os **mesmos prompts** e o **mesmo scaffold base**, garantindo que a única variável do experimento seja a ferramenta/ambiente utilizado.

---

## Estrutura do repositório

```
tcc-fisicapp/
├── scaffold/          # Base original compartilhada — não modificada
├── fisicapp-cursor/   # Desenvolvimento com Cursor IDE + GPT-5
├── fisicapp-chatgpt/  # Desenvolvimento com ChatGPT Web + GPT-5
└── README.md
```

### scaffold/
Projeto base criado antes do experimento, idêntico para as duas ferramentas. Contém apenas a configuração técnica de stack (Expo + TypeScript + NativeWind + Expo Router), sem nenhuma lógica de aplicativo implementada. Serve como ponto zero do experimento.

### fisicapp-cursor/
Versão do FisicApp desenvolvida com o **Cursor IDE** — ferramenta de desenvolvimento com IA integrada diretamente ao ambiente de código. O modelo utilizado foi GPT-5 via integração nativa do Cursor.

### fisicapp-chatgpt/
Versão do FisicApp desenvolvida com o **ChatGPT Web** — interface conversacional generalista de propósito geral. O modelo utilizado foi GPT-5. O código gerado foi transferido manualmente para o projeto.

---

## Stack tecnológica

| Tecnologia | Versão | Papel |
|---|---|---|
| React Native | 0.82+ | Framework mobile |
| Expo SDK | 54 | Plataforma de desenvolvimento |
| TypeScript | 5.x | Tipagem estrita |
| NativeWind | 4.x | Estilização (Tailwind para RN) |
| Expo Router | 6.x | Navegação por arquivos |
| AsyncStorage | — | Persistência local |
| Expo WebView | — | Simulador PhET |

---

## Metodologia de prompts

Os prompts aplicados em ambas as ferramentas seguem a combinação de três técnicas:

- **Role Prompting** — atribuição de papel profissional ao modelo
- **Especificação Técnica Explícita** — declaração de stack, requisitos e entregáveis
- **Structured Chain-of-Thought** — raciocínio estruturado em etapas antes da geração de código

Os prompts foram divididos em **6 prompts sequenciais**:

| Prompt | Escopo |
|---|---|
| P1 | Setup do projeto e fundação técnica |
| P1.5 | Design system e identidade visual UNIVASF |
| P2 | Conteúdo teórico e simulador PhET |
| P3 | Flashcards e jogo da memória |
| P4 | Quiz, desafio sequencial e completar lacunas |
| P5 | Progresso, IA conversacional e validação final |

Os prompts completos estão documentados em [`scaffold/prompts/`](./scaffold/).

---

## Como executar cada versão

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/tcc-fisicapp.git

# Entre na versão desejada
cd fisicapp-cursor
# ou
cd fisicapp-chatgpt

# Instale as dependências
npm install

# Inicie o projeto
npx expo start
```

---

## Requisitos do aplicativo

### Funcionais (RF)
- RF01 — Flashcards, quiz, memória, desafio sequencial e completar lacunas
- RF02 — Sequência de temas definida pelo sistema
- RF03 — Perguntas de conceito, fórmula e aplicação prática
- RF04 — Entre 3 e 5 temas distintos
- RF05 — Feedback imediato com explicação após cada resposta
- RF06 — Acompanhamento de desempenho (acertos e tempo)
- RF07 — Conteúdo agrupado por nível de dificuldade
- RF08 — Suporte a imagens e fórmulas
- RF09 — Lista de progresso com salvamento local
- RF10 — Seção de conteúdo teórico para consulta rápida
- RF11 — Integração com simulador PhET via WebView
- RF12 — Seção de IA para dúvidas em linguagem natural

### Não Funcionais (RNF)
- RNF01 — Tela inicial com grid de acesso direto
- RNF02 — Botão de reinício em todos os modos de jogo
- RNF03 — Botão de ajuda com instruções de uso
- RNF04 — Dicas extras para respostas incorretas

---

## Autores

Aluno: Antonio dos Santos Filho — Engenharia da Computação — UNIVASF  
Orientador: Prof. Dr. Rosalvo Ferreira de Oliveira Neto 
Ano: 2025/2026

---

## Licença

Este repositório tem fins exclusivamente acadêmicos.