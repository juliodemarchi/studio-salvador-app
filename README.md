# 📱 AppStudio - Studio Salvador (Tattoo & Rock Store)

O **Studio Salvador** é um aplicativo mobile completo projetado para gerenciar a experiência de clientes em um estúdio de tatuagem moderno que integra uma loja física/virtual de mercadorias. Desenvolvido em **React Native** com **TypeScript**, o projeto aplica conceitos sólidos de arquitetura de software, componentização, gerenciamento de estado global e tipagem estática.

---

## 🚀 Funcionalidades

### 🔐 Autenticação & Perfil
* **Cadastro e Login:** Fluxo de autenticação seguro gerenciado via Context API (`AuthContext`).
* **Histórico do Usuário:** Painel centralizado onde o cliente acompanha em tempo real o status dos seus agendamentos e compras anteriores.

### 📅 Módulo de Agendamento
* **Agendamento Inteligente:** Formulário dinâmico para escolha de tatuador, data, horário e estilo de arte (Blackwork, Fineline, Oriental, Old School).
* **Validação de Campos:** Bloqueio de agendamentos incompletos para consistência dos dados.

### 🛒 E-commerce & Loja Integrada (Complexidade Completa)
* **Catálogo com Filtros:** Separação de produtos por categorias (Merch, Cuidado Pós-Tattoo, Joias/Piercings).
* **Carrinho Dinâmico:** Gerenciamento global de itens, cálculo automático de subtotal e atualização de quantidades.
* **Checkout Integrado:** Fluxo estruturado para simulação e integração de pagamentos (PIX e Cartão de Crédito).

---

## 📁 Arquitetura e Estrutura de Pastas

O projeto adota uma estrutura modular e escalável, facilitando a manutenção e a integração com serviços de backend:

```text
src/
├── @types/          # Definições e interfaces TypeScript (User, Product, Appointment)
├── assets/          # Arquivos de mídia, logos, imagens e fontes customizadas
├── components/      # Componentes reutilizáveis de UI (Button, Input, Card)
├── context/         # Estados globais compartilhados (AuthContext, CartContext)
├── database/        # Configurações de API (Axios) ou serviços de banco de dados
├── routes/          # Estrutura de navegação (AuthStack, AppTabs)
└── screens/         # Telas de visualização da aplicação
    ├── Auth/        # Telas de Login e Cadastro de novos usuários
    ├── Booking/     # Telas do fluxo de agendamento de sessões
    ├── Store/       # Vitrine da loja, detalhes de itens e Carrinho
    └── Profile/     # Perfil do cliente e histórico completo
