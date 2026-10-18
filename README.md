# DGM-MAT-Memory — sincronizador de recuperação do cérebro

**Estado:** REPOSITÓRIO A MANTER — FUNÇÃO APROVADA  
**Responsável:** DGM-MAT (cérebro soberano)  
**Objetivo:** cópia de segurança seletiva, versionada e recuperável do conhecimento operacional necessário para reconstruir o DGM-MAT quando um PC falha, é substituído ou reinstalado.

> **Este repositório NÃO deve ser apagado.** O aviso anterior de eliminação estava incorreto e fica substituído por este README.

## Papel e fronteiras

- **DGM-MAT:** fonte de autoridade para decisões, execução, coordenação, políticas e validação.
- **DGM-MAT-Memory:** réplica/arquivo de recuperação de documentos e artefactos selecionados, com proveniência e histórico Git. Não é um segundo cérebro nem decide autonomamente qual é a verdade.
- **andreos-memory:** memória persistente de governação do projeto, decisões arquiteturais e continuidade entre sessões.
- **DGM-MAT-Labs:** laboratório isolado para repositórios externos em estudo. Não é destino de backups de memória nem deve ser clonado automaticamente para o workspace principal.

## Conteúdo permitido

1. Documentação arquitetural aprovada, decisões, ADRs e registos de fases.
2. Inventário de capacidades, departamentos, dependências e versões de ferramentas.
3. Procedimentos de instalação, recuperação, migração e reconstrução do ambiente.
4. Manifestos de backup com origem, data, commit/fingerprint, versão de esquema e estado de validação.
5. Lições de engenharia verificadas, relatórios de testes e instruções para retomar tarefas.
6. Exportações de conversas apenas quando forem necessárias, legalmente permitidas e sanitizadas; preferir metadados, decisões e excertos necessários, mantendo os originais privados no armazenamento local quando possível.
7. Artefactos de código selecionados que sejam necessários à recuperação, com origem, licença, versão e validação documentadas.

## Conteúdo proibido por omissão

- Tokens, passwords, chaves privadas, cookies, credenciais e ficheiros de ambiente.
- Dumps integrais de discos, caches, ambientes virtuais, dependências reconstruíveis, modelos grandes ou artefactos gerados que possam ser reconstruídos.
- Dados pessoais ou conversas integrais de terceiros sem necessidade, autorização e sanitização.
- Cópias indiscriminadas de repositórios satélite, clones privados, conteúdo de clientes ou código externo sem revisão de licença.
- Qualquer material que transforme este repositório num clone integral e automático do workspace.

## Sincronização e recuperação

- Sincronização explícita e seletiva; nunca publicar automaticamente tudo o que aparece no PC.
- Cada pacote de recuperação deve indicar origem, timestamp UTC, commit/versão, lista de ficheiros, checksums quando aplicável e resultado da validação.
- Preservar o histórico Git e não substituir informação anterior sem um commit rastreável.
- Recuperar primeiro para uma pasta/branch isolada; verificar integridade, segredos, compatibilidade e testes antes de restaurar no runtime.
- A falha do GitHub ou da rede não pode parar o cérebro local. A cópia remota é redundância, não runtime obrigatório.
- A mudança de PC deve ser suportada por um manifesto reproduzível de ambiente: capacidades de hardware, ferramentas instaladas, versões, dependências e instruções de reinstalação. Nunca guardar segredos no manifesto.

## Política de hardware adaptativo

O DGM-MAT deteta CPU, RAM, armazenamento, GPU, sistema operativo, conectividade e ferramentas disponíveis. Ajusta paralelismo, modelos locais, limites de memória e carga dos departamentos. Só propõe instalar ferramentas ausentes depois de identificar necessidade, licença, custo, origem e impacto; a instalação requer autorização conforme a política de segurança. Se não houver ferramenta adequada, pode propor construir um componente na Fábrica Virtual, que deve ser isolado, testado e aprovado antes de entrar em produção.

## Departamentos prioritários

- **Programação e Revisão de Código:** alterações pequenas, diff auditável, testes, análise de dependências/segurança, execução de testes em ambiente isolado, regressões e evidência antes de aprovar.
- **Pesquisa e Inovação:** fontes rastreáveis, comparação de alternativas, avaliação de qualidade/licença/manutenção, reprodutibilidade e distinção clara entre factos, hipóteses e recomendações.

Ambos devem poder pedir ajuda, pesquisar documentação e aprender de resultados validados. Nenhum departamento pode declarar sucesso sem evidência, contornar as políticas do cérebro ou autoaprovar alterações de alto risco.

## Relação com o Headquarters

O Headquarters é uma visualização do estado real. Não comanda o cérebro e não é necessário para sincronizar ou recuperar memória. Os agentes e animações apresentados devem corresponder a eventos e estados reais.

## Princípios

- Estabilidade > funcionalidades.
- Evidência > pressupostos.
- Recuperabilidade > cópias indiscriminadas.
- Segredos fora do Git.
- O cérebro continua funcional sem rede, GitHub ou cockpit.
- O conteúdo recuperado é validado antes de ser tratado como verdade atual.
