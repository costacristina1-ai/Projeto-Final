# Projeto-Final
# Controle de Despesas

Aplicativo desenvolvido em React Native com Expo para cadastrar, consultar, editar e excluir despesas. Os dados são persistidos no Firebase Realtime Database por meio de requisições HTTP.

## Funcionalidades

- Consultar todas as despesas e as despesas dos últimos sete dias.
- Cadastrar despesas com descrição, valor e data.
- Validar os campos antes de salvar.
- Consultar e editar uma despesa existente.
- Excluir despesas.
- Exibir o total das despesas do período.
- Carregar os dados do Firebase ao abrir a tela inicial.
- Exibir estados de carregamento e mensagens de erro.

## Requisitos

- Node.js (versão LTS recomendada).
- npm.
- Expo Go instalado no celular.
- Projeto Firebase com o Realtime Database criado.

## Configuração do Firebase

1. Acesse o [Firebase Console](https://console.firebase.google.com/).
2. Crie ou selecione um projeto.
3. Crie um **Realtime Database**.
4. Copie a URL exibida na página do banco de dados.
5. Abra `util/http.js`.
6. Substitua o endereço de exemplo em `BACKEND_URL` pela URL copiada. Não coloque uma barra `/` no final.

Exemplo de formato (não utilize este endereço como se fosse o seu):

```js
export const BACKEND_URL =
  'https://NOME-DO-SEU-PROJETO-default-rtdb.firebaseio.com';
```

A URL pode variar conforme a região do banco. Use exatamente a URL apresentada pelo Firebase.

Para a atividade, o aplicativo utiliza o caminho `/expenses.json`:
- `POST /expenses.json`: cadastra uma despesa.
- `GET /expenses.json`: carrega as despesas.
- `PUT /expenses/ID.json`: atualiza uma despesa.
- `DELETE /expenses/ID.json`: exclui uma despesa.

**Atenção à segurança:** o professor orientou o uso de dados fictícios porque as regras abertas de teste do Realtime Database não devem receber dados pessoais ou reais. Confira as regras e o prazo de validade no Console do Firebase.

## Como executar

```bash
git clone URL_DO_REPOSITORIO
cd controle-despesas
npm install
npm start
```

Leia o QR Code com o Expo Go. O computador e o celular devem estar em uma rede que permita a comunicação necessária com o servidor Expo.

Para executar no navegador, se necessário:

```bash
npm run web
```

## Estrutura do projeto

```text
App.js
components/
  ExpensesOutput/
  ManageExpense/
  UI/
constants/
screens/
  AllExpenses.js
  ManageExpense.js
  RecentExpenses.js
store/
  expenses-context.js
util/
  date.js
  http.js
```

## Tecnologias e conceitos utilizados

- React Native e Expo.
- React Navigation (Stack e Bottom Tabs).
- `FlatList`.
- Context API e `useReducer`.
- Formulários com `TextInput` e validação.
- `useEffect` para carregar dados.
- Axios e Firebase Realtime Database via HTTP.
- Estados de carregamento e erro.

## O que pode ser melhorado futuramente

- Adicionar categorias para as despesas.
- Implementar filtros por mês e categoria.
- Melhorar a apresentação dos relatórios.
- Adicionar autenticação e regras de segurança adequadas, caso o aplicativo evolua para uso real.

## Aluna

- Nome: **Beatriz Cristina Costa**
- Turma: **4º info 1**

