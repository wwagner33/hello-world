# Usando Git e Github

## 1. **Autenticação no GitHub**

Desde agosto de 2021, o GitHub não aceita mais autenticação via usuário e senha diretamente no terminal. Agora, é necessário usar um **Token de Acesso Pessoal (PAT)**. Aqui vai o passo a passo:

### a) **Gerar um Token de Acesso Pessoal (PAT):**

1. Acesse [https://github.com/settings/tokens](https://github.com/settings/tokens)
2. Clique em **"Generate new token"** (ou "Gerar novo token").
3. Dê um nome para o token, selecione as permissões necessárias (por exemplo, `repo` para acesso a repositórios) e defina uma validade.
4. Clique em **"Generate token"** e **copie o token gerado**. Guarde-o em um local seguro!

### b) **Configurar o Git para usar o token:**

No terminal, você pode configurar o Git para lembrar suas credenciais:

```bash
git config --global credential.helper store
```

Isso fará com que o Git armazene suas credenciais em texto plano no arquivo `.git-credentials`. Se preferir mais segurança, pode usar:

```bash
git config --global credential.helper cache
```

Isso armazenará suas credenciais em cache por um tempo (por padrão, 15 minutos).

## 2. **Clonar o Repositório**

Se ainda não clonou o repositório, use:

```bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
```

Substitua `SEU_USUARIO` e `SEU_REPOSITORIO` pelos seus dados.

## 3. **Fazer Pull e Push**

Após configurar o token e clonar o repositório, você pode usar os comandos normalmente:

```bash
git pull origin main
git push origin main
```

Na primeira vez que fizer `pull` ou `push`, o Git pedirá suas credenciais. Use seu **nome de usuário do GitHub** e, no campo de senha, cole o **token de acesso pessoal** que você gerou.
