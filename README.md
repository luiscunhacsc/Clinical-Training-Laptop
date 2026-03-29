# Modelo Neurocognitivo Interativo

Aplicação web educativa (sem dependências) para estudo, treino e simulação clínica do modelo neurocognitivo da linguagem.

## Visão Geral

Este projeto foi desenhado para apoiar aprendizagem progressiva em três níveis:

1. **Estudo**: consolidação visual dos componentes do modelo.
2. **Teste**: evocação ativa por arrastar e largar.
3. **Caso Clínico**: raciocínio clínico guiado em 3 passos (lesão, diagnóstico, intervenção).

Tudo funciona num único ficheiro (`index.html`), ideal para uso em sala de aula, tutoria ou autoestudo.

## Principais Funcionalidades

- **3 modos pedagógicos**: Estudo, Teste e Clínico.
- **3 apresentações do modelo**: Geral, Perturbações e Tarefas/Reabilitação.
- **Pontuação gamificada no modo clínico**.
- **Botão "Mostrar resposta certa" no modo clínico**, com fluxo UX seguro:
  - confirmação antes de revelar;
  - continuação sem pontuar na fase atual;
  - destaque visual da solução.
- **Layout adaptativo para portátil** com diagrama prioritário no painel direito.
- **Modo de ecrã inteiro** para máxima legibilidade.
- **Sem backend, sem build, sem framework**.

## Como Executar

### Opção A: abrir diretamente

1. Faça download/clone do projeto.
2. Abra o ficheiro `index.html` no browser.

### Opção B: servidor local (recomendado)

```bash
python -m http.server 8000
```

Depois abra:

```text
http://localhost:8000
```

## Como Usar

1. Escolha o **modo** no painel esquerdo.
2. Selecione a **apresentação** (Geral, Perturbações, Tarefas/Reabilitação).
3. Use os filtros e interações do modo ativo.
4. Ative **Ecrã inteiro** para melhor leitura do diagrama.

### Fluxo do Modo Clínico

1. **Passo 1 - Lesão**: identificar módulo(s) afetado(s) no diagrama.
2. **Passo 2 - Diagnóstico**: escolher a perturbação correta.
3. **Passo 3 - Tratamento**: selecionar tarefas de reabilitação adequadas.

Se necessário, use **"Mostrar resposta certa"** para desbloquear o estudo sem interromper o caso.

## Publicar no GitHub Pages

Como o projeto é estático, pode ser publicado em poucos cliques:

1. Faça push do repositório para o GitHub.
2. Vá a `Settings` -> `Pages`.
3. Em `Build and deployment`, escolha:
   - `Source`: **Deploy from a branch**
   - `Branch`: **main** (root)
4. Guarde e aguarde o URL público ser gerado.

O site ficará disponível num endereço do tipo:

```text
https://<utilizador>.github.io/<repositorio>/
```

## Arquitetura Técnica

- **Stack**: HTML + CSS + JavaScript vanilla.
- **Estado da aplicação**: objeto central `state`.
- **Renderização**: funções `render*` por modo/painel.
- **Layout do modelo**: slots posicionados via `SLOT_DEFS`.
- **Conteúdo pedagógico**:
  - `MODELS` para termos por apresentação;
  - `CASOS_CLINICOS` para sintomas, perturbações e tarefas.

## Estrutura do Projeto

```text
.
├── index.html
└── README.md
```

## Personalização

Para adaptar conteúdos ao seu contexto clínico/educativo:

- Atualize termos e mapas em `MODELS`.
- Edite casos em `CASOS_CLINICOS`.
- Ajuste posicionamento/tamanho das caixas em `SLOT_DEFS`.
- Ajuste estilos e tipografia no bloco `<style>`.

## Compatibilidade

- Chrome, Edge, Firefox e Safari recentes.
- Resoluções de portátil e desktop.
- Funciona offline após carregar o ficheiro.

## Roadmap Sugerido

- Exportar resultados do modo clínico (JSON/CSV).
- Banco de casos por dificuldade.
- Modo docente (sessões, comparação entre tentativas).
- Internacionalização (PT/EN).

## Contribuição

Issues e Pull Requests são bem-vindos para:

- melhorias de UX/UI;
- novos casos clínicos;
- refinamento pedagógico;
- acessibilidade e desempenho.

## Créditos e Contacto

- Autor: **Luís Simões da Cunha**, (C) 2026.
- Membro Efetivo da Ordem dos Psicólogos Portugueses.
- Cédula **#189**.
- Especialista (OPP) em Psicologia Clínica.
- Especialidade Avançada (OPP) em Neuropsicologia.
- Para indicação de bugs ou sugestões de melhoria:
  - `luis.luiscunha.docencia@gmail.com`

## Licença

Este projeto está licenciado sob a **MIT License**.