# Atividade Prática – Git & GitHub

## Objetivo
Cada aluno deverá criar **sua própria branch**, adicionar **uma pasta com seu nome** dentro de `alunos/` e colocar um arquivo `README.md` lá dentro com algumas informações pessoais (curso, interesses, etc.).  
O envio será feito via **Pull Request (PR)**.

---

## Passo a passo

### 1. Fazer o **Fork** do repositório
1. Acesse: [https://github.com/molettta/senacCursoGit](https://github.com/molettta/senacCursoGit)
2. Clique no botão **Fork** (canto superior direito).
3. Isso criará uma cópia do repositório no seu GitHub.

---

### 2. Clonar o repositório (seu fork)
```bash
git clone https://github.com/<SEU_USUARIO_GITHUB>/senacCursoGit.git
cd senacCursoGit
```

---

### 3. Criar uma **branch** com seu nome
Padrão: `aluno/<nome-sobrenome>` (tudo minúsculo, sem acento)
```bash
git checkout -b aluno/seu-nome
```

---

### 4. Criar sua pasta e o arquivo README.md
Padrão de pasta: `alunos/NomeSobrenome`
```bash
mkdir -p alunos/NomeSobrenome
echo "# Nome Sobrenome" > alunos/NomeSobrenome/README.md
echo "- Curso: Seu curso aqui" >> alunos/NomeSobrenome/README.md
echo "- Interesses: Liste aqui" >> alunos/NomeSobrenome/README.md
```

---

### 5. Adicionar, commitar e enviar para o GitHub
```bash
git add .
git commit -m "feat: adiciona pasta e README de Nome Sobrenome"
git push origin aluno/seu-nome
```

---

### 6. Criar o Pull Request
1. No GitHub, vá até **seu fork**.
2. Clique no botão **Compare & pull request**.
3. Confirme que está enviando para:
   - **Base repository**: `molettta/senacCursoGit`
   - **Base branch**: `main`
   - **Head repository**: seu fork
   - **Compare branch**: `aluno/seu-nome`
4. Adicione um título como: `Adiciona Nome Sobrenome em alunos/`
5. Clique em **Create pull request**.

---

## Regras importantes
- Não edite a pasta de outros alunos.
- Sempre trabalhe em uma branch nova, **nunca** direto na `main`.
- Nome da pasta e da branch devem seguir o padrão indicado.
- Apenas um `README.md` dentro da sua pasta.

---

### Exemplo de estrutura final
```
alunos/
 ├── FulanoSilva/
 │    └── README.md
 ├── MariaOliveira/
 │    └── README.md
```

---

✏ **Dica:** Antes de começar, sincronize sempre seu fork com o repositório original para evitar conflitos.
```bash
git remote add upstream https://github.com/molettta/senacCursoGit.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```
