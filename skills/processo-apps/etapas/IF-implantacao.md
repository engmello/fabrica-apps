# Implantação da fábrica — uma vez só

## IF.1 · Acordo da equipe
- **Objetivo:** definir propriedade, papéis, custos e receitas antes do primeiro app.
- **Gatilho:** início da fábrica, ou entrada/saída de um membro.
- **Entradas:** lista de membros e disponibilidade.
- **Passos:** 1. Papéis e dedicação semanal. 2. A quem pertencem código, marcas e contas (recomendado: uma empresa). 3. Divisão de custos e receitas. 4. Regras de entrada e saída. 5. Forma jurídica e CNPJ (contas de empresa nas lojas). 6. Assinar.
- **Saída:** T14 assinado.
- **Responsável:** todos executam e aprovam.
- **IA:** agente `produto` redige o rascunho a partir das decisões; recomendar revisão por advogado.
- **Pronto quando:** assinado por todos.
- **Duração:** 1 semana.

## IF.2 · Contas e ferramentas
- **Objetivo:** todas as ferramentas da stack em nome da equipe, com acesso seguro.
- **Gatilho:** IF.1 concluída.
- **Entradas:** stack padrão; orçamento.
- **Passos:** 1. E-mail da equipe para as contas. 2. GitHub (organização), Supabase, Expo, Vercel, Sentry, PostHog, quadro de tarefas, Claude. 3. Verificação em duas etapas em todas. 4. Dois administradores por conta. 5. Senhas em gerenciador compartilhado.
- **Saída:** lista de contas, administradores e planos (sem senhas).
- **Responsável:** Construtor executa; Produto aprova.
- **IA:** —
- **Pronto quando:** todas as contas com duas etapas e dois administradores.
- **Duração:** 1 a 2 dias.

## IF.3 · Instalar o kit técnico
- **Objetivo:** ferramenta instalada e testada.
- **Gatilho:** IF.2 concluída.
- **Entradas:** este plugin.
- **Passos:** 1. Publicar o plugin no repositório da equipe e instalar em cada máquina. 2. Criar um app de exemplo com `/novo-app` e rodar o E3.1 até staging. 3. Testar `/etapa`, `/status`, `/portao`, `/nova-feature`, `/revisar`.
- **Saída:** plugin instalado e app de exemplo publicando em staging.
- **Responsável:** Construtor.
- **IA:** agente `desenvolvedor` configura; agente `revisor` confere.
- **Pronto quando:** app de exemplo passa no CI e publica sozinho em staging.
- **Duração:** 2 a 3 dias.

## IF.4 · Rituais e canais
- **Objetivo:** operação da equipe pronta antes do primeiro app.
- **Gatilho:** IF.1 concluída.
- **Entradas:** Plano de Gestão da Equipe.
- **Passos:** 1. Canal da equipe. 2. Quadro com colunas de status e etiquetas de etapa (IF.1…E5.6) e `processo`. 3. Coluna "Ideias" (portfólio). 4. Agendar rituais. 5. Pasta compartilhada `Apps/`.
- **Saída:** canal, quadro, agenda e pastas prontos.
- **Responsável:** Produto executa; equipe aprova.
- **IA:** —
- **Pronto quando:** primeira demo e primeiro status assíncrono realizados.
- **Duração:** 1 dia.
