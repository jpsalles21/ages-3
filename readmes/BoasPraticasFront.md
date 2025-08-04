# Arquitetura do Frontend e padrões

Documento para definir os padrões e boas práticas a serem seguidos no desenvolvimento frontend deste projeto (React + TypeScript).

---

## Estrutura de Pastas

- 📁 `src/`
  - 📁 `components/`       - Componentes reutilizáveis
    - 📁 `Button/`
      - `Button.tsx`
      - `Button.module.scss`
    - `index.ts`
  - 📁 `pages/`            - Páginas (rotas)
  - 📁 `hooks/`            - Custom hooks (useSomething)
  - 📁 `contexts/`         - React Context API
  - 📁 `services/`         - Comunicação com API
  - 📁 `types/`            - Tipagens globais
  - 📁 `utils/`            - Funções auxiliares




## Nomenclatura

### ✅ Geral
- **Tudo em inglês**
- **camelCase** para variáveis, funções e props
- **PascalCase** para nomes de componentes e arquivos `.tsx`
- **kebab-case** para pastas.

### ✅ Componentes React
- Nome: `UserCard.tsx`
- Componente com arrow function:
- Props com Interface no componente
  ```tsx
  // components/UserCard.tsx

  interface UserCardProps { 
    title: string;
    description?: string; // opcional
  }

  const UserCard = ({ title, description }: UserCardProps) => {
    return (
      <div>
        <h2>{title}</h2>
        <p>{description}</p>
      </div>
    );
  };

  export default UserCard;
  ```
- Exportação:
  ```tsx
  // components/index.ts
  export { default as UserCard} from './UserCard';
  ```

---

## 🎨 Estilização com SCSS

Este projeto utiliza **SCSS modules** com organização modularizada e padrões consistentes para facilitar manutenção e escalabilidade.

---

### 📛 Nomeação das Classes CSS

- Use **camelCase** para nomes de classes (ex: `primaryButton.module.scss`, `mainContainer.module.scss`).
- Escolha nomes semânticos que reflitam a função ou o papel do elemento, não sua aparência.
---

## 💡 Boas Práticas

- Componentes  reutilizáveis;
- Evitar o uso de `any`: usar tipagens com TypeScript;
- Separar lógica de negócio em hooks ou services;
- Importações configuradas via `tsconfig.paths`.

---

## 🪝 Hooks

- Arquivos nomeados como `useSomething.ts`
- Colocados na pasta `src/hooks`
- Seguir padrão de nomenclatura do React

---

## 🧪 Testes (placeholder)

- `Component.test.tsx` ao lado do componente
- Testar componentes reutilizáveis e lógica de hooks
- Testes E2E com Cypress ou Playwright (opcional)

---

## ✅ Commits e Pull Requests

- Para facilitar a semântica, manteremos os commits e PRs em português
- Commits: usar [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
  - Exemplo: `feat: add login button`
- Pull Requests:
  - Título claro e objetivo
  - Descrição com contexto, mudanças e screenshots (se aplicável)

---

## 📄 Documentação Interna

- Comentários só quando **realmente necessários** (código limpo deve se explicar)

---

> Siga esse guia para garantir consistência, organização e qualidade no desenvolvimento frontend. Em caso de dúvidas, chame algum dos AGES III para esclarecer melhor o processo. 
