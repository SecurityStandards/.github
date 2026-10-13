# Guia de Contribuição - SecurityStandards

Agradecemos o interesse em contribuir com os projetos da **SecurityStandards**!

## Princípios de Engenharia & Contribuição

1. **Spec-Driven Development (SDD)**:
   * Antes de submeter grandes refatorações ou novas features, crie ou discuta uma especificação formal em `docs/specs/<NNN>-<feature>/`.
   * A especificação deve contemplar `spec.md` (o quê/por quê), `plan.md` (como/arquitetura) e `tasks.md` (passos de entrega incrementais).

2. **Commits e Assinatura**:
   * Todos os commits devem ser assinados criptograficamente com GPG.
   * Mensagens de commit devem seguir o padrão Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`, etc.).

3. **Pull Requests**:
   * Cada PR deve ser atômico e focado em um único propósito.
   * Certifique-se de que testes e linters estejam passando localmente antes de submeter o PR.
