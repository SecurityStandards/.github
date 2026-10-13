# Contrato Canônico de Agentes de IA - SecurityStandards

Este arquivo define as convenções de ambiente, engenharia e conduta para agentes de inteligência artificial que atuam nos repositórios da organização **SecurityStandards**.

## 1. Identidade & Commits (Regra Inviolável)
* **Autor e Committer**: SEMPRE `Matheus Breguêz <matbrgz@gmail.com>`.
* **Assinatura GPG**: Todos os commits DEVEM ser assinados com a chave configurada no ambiente do usuário (`B6FA8458D5176E83`).
* **Proibições**: NUNCA usar `--no-gpg-sign` ou forçar outro autor.
* **Co-autoria da IA**: Apenas como trailer no rodapé do commit:
  `Co-Authored-By: <Agent Name> <noreply@...>`

## 2. Metodologia: Spec-Driven Development (SDD)
* Nenhuma alteração estrutural deve ser feita sem especificação prévia.
* Estrutura canônica de especificações: `docs/specs/<NNN>-<feature>/` com:
  * `spec.md` (o quê e por quê: escopo, requisitos funcionais e não-funcionais, critérios de aceite)
  * `plan.md` (como: contratos de interface, arquitetura, dependências)
  * `tasks.md` (passos de implementação incrementais e verificáveis)
* Uma spec = um domínio ou feature. Nunca misturar domínios independentes na mesma spec.

## 3. Gestão de Worktrees & Ambiente
* Operações paralelas ou de longa duração devem ocorrer em worktrees isoladas.
* Após conclusão e envio de PRs, as worktrees temporárias devem ser limpas imediatamente (`git worktree remove` e `git worktree prune`).
