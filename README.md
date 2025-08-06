# 📱 Nearby Mobile

> **Aplicativo mobile Nearby** desenvolvido durante a **NLW Pocket Mobile** da [Rocketseat](https://www.rocketseat.com.br) 🚀

## 📖 Sobre o Projeto

O **Nearby** é um aplicativo mobile que conecta usuários a estabelecimentos próximos, permitindo descobrir locais interessantes e resgatar cupons de desconto exclusivos. Desenvolvido com **React Native** e **Expo**, o app oferece uma experiência fluida e intuitiva para encontrar e interagir com comércios locais.

Este projeto foi criado como parte do evento **Next Level Week (NLW) Pocket Mobile**, uma semana intensiva de aprendizado promovida pela Rocketseat.

## ✨ Funcionalidades

### 🎯 **Principais Features**
- ✅ **Localização em tempo real** - Visualize sua posição atual no mapa
- ✅ **Mapa interativo** - Navegue pelo mapa e descubra estabelecimentos próximos  
- ✅ **Categorias de estabelecimentos** - Filtre locais por categoria (Alimentação, Compras, Hospedagem, etc.)
- ✅ **Lista de estabelecimentos** - Visualize todos os locais disponíveis em formato de lista
- ✅ **Detalhes do estabelecimento** - Veja informações completas, fotos e contato
- ✅ **Sistema de cupons** - Resgate cupons de desconto escaneando QR codes
- ✅ **Interface responsiva** - Design adaptado para diferentes tamanhos de tela
- ✅ **Navegação fluida** - Transições suaves entre telas

### 📸 **Funcionalidades de câmera**
- 📷 **QR Code Scanner** - Escaneie QR codes para resgatar cupons
- 🎫 **Resgate de cupons** - Sistema completo de validação de cupons

## 🛠️ Tecnologias Utilizadas

### **Frontend Mobile**
- **React Native** - Framework para desenvolvimento mobile multiplataforma
- **Expo** - Plataforma para desenvolvimento React Native
- **TypeScript** - Superset tipado do JavaScript
- **Expo Router** - Sistema de roteamento file-based para Expo

### **UI/UX & Estilização**
- **React Native Maps** - Mapas nativos integrados
- **Expo Google Fonts (Rubik)** - Tipografia customizada
- **Tabler Icons** - Biblioteca de ícones moderna
- **Bottom Sheet** - Componente de painel deslizante

### **Funcionalidades Nativas**
- **Expo Camera** - Acesso à câmera do dispositivo
- **Expo Location** - Geolocalização e GPS
- **React Native Reanimated** - Animações performáticas
- **React Native Gesture Handler** - Gestos nativos

### **Networking & Estado**
- **Axios** - Cliente HTTP para comunicação com API
- **React Hooks** - Gerenciamento de estado local

### **Desenvolvimento**
- **Jest** - Framework de testes
- **Babel** - Transpilador JavaScript

## 🚀 Como Executar

### **Pré-requisitos**
- Node.js (versão 18+)
- npm ou yarn
- Expo CLI: `npm install -g @expo/cli`
- **Aplicativo Expo Go** instalado no seu celular
  - [Android](https://play.google.com/store/apps/details?id=host.exp.exponent)
  - [iOS](https://apps.apple.com/app/expo-go/id982107779)

### **Instalação**

1. **Clone o repositório**
   ```bash
   git clone [url-do-repositorio]
   cd nlw.mobile
   ```

2. **Instale as dependências**
   ```bash
   npm install
   ```

3. **Configure a API**
   
   Edite o arquivo `src/services/api.ts` e altere a baseURL para o IP da sua API:
   ```typescript
   export const api = axios.create({
     baseURL: "http://SEU_IP_LOCAL:3333", // Substitua pelo seu IP
     timeout: 700,
   })
   ```

4. **Inicie o projeto**
   ```bash
   npm start
   ```

5. **Execute no dispositivo**
   - Escaneie o QR code com o **Expo Go**
   - Ou pressione `a` para Android / `i` para iOS (se tiver emuladores configurados)

## 📁 Estrutura do Projeto

```
src/
├── app/                     # Telas da aplicação (Expo Router)
│   ├── _layout.tsx         # Layout principal
│   ├── index.tsx           # Tela de boas-vindas
│   ├── home.tsx            # Tela principal com mapa
│   └── market/
│       └── [id].tsx        # Detalhes do estabelecimento
├── components/             # Componentes reutilizáveis
│   ├── button/             # Botão personalizado
│   ├── categories/         # Lista de categorias
│   ├── loading/            # Indicador de carregamento
│   ├── market/             # Componentes do estabelecimento
│   │   ├── coupon/         # Cupom de desconto
│   │   ├── cover/          # Imagem de capa
│   │   ├── details/        # Detalhes do local
│   │   └── info/           # Informações básicas
│   ├── places/             # Lista de estabelecimentos
│   ├── steps/              # Passos do tutorial
│   └── welcome/            # Componente de boas-vindas
├── services/               # Comunicação com APIs
│   └── api.ts             # Configuração do Axios
├── styles/                 # Temas e estilos
│   ├── colors.ts          # Paleta de cores
│   ├── font-family.ts     # Fontes tipográficas
│   └── theme.ts           # Tema global
├── utils/                  # Utilitários
│   └── categories-icons.ts # Ícones das categorias
└── assets/                 # Recursos estáticos
    ├── logo.png           # Logotipo
    ├── location.png       # Ícone de localização
    └── pin.png            # Pin do mapa
```

## 📱 Telas do Aplicativo

### 🎨 **1. Tela de Boas-vindas**
- Apresentação do app e suas funcionalidades
- Tutorial com passos de uso
- Botão para começar a usar

### 🗺️ **2. Tela Principal (Home)**
- Mapa interativo com localização atual
- Filtros por categoria de estabelecimento
- Marcadores dos estabelecimentos no mapa
- Lista de locais próximos na parte inferior

### 🏪 **3. Detalhes do Estabelecimento**
- Informações completas do local
- Foto de capa, endereço, telefone
- Cupons de desconto disponíveis
- Scanner de QR code para resgate

## 🎯 Fluxo de Uso

1. **Início**: Usuário abre o app e vê a tela de boas-vindas
2. **Permissões**: App solicita permissão de localização e câmera
3. **Exploração**: Usuário navega pelo mapa e filtra por categorias
4. **Seleção**: Usuário toca em um estabelecimento no mapa ou na lista
5. **Detalhes**: Visualiza informações completas do local
6. **Cupom**: Escaneia QR code para resgatar desconto
7. **Confirmação**: Recebe confirmação do cupom resgatado

## 🔧 Scripts Disponíveis

```bash
# Iniciar o servidor de desenvolvimento
npm start

# Executar no Android
npm run android

# Executar no iOS  
npm run ios

# Executar no navegador
npm run web

# Executar testes
npm test
```

## 🌐 Integração com API

O aplicativo consome uma API REST para:
- Buscar categorias de estabelecimentos
- Listar estabelecimentos por categoria
- Obter detalhes de um estabelecimento específico  
- Resgatar cupons de desconto

**Endpoints utilizados:**
- `GET /categories` - Lista todas as categorias
- `GET /markets/category/:categoryId` - Estabelecimentos por categoria
- `GET /markets/:id` - Detalhes de um estabelecimento
- `PATCH /coupons/:couponId` - Resgatar cupom

## 👨‍💻 Desenvolvido por

Este projeto foi desenvolvido seguindo as aulas da **Rocketseat** durante a **NLW Pocket Mobile**.

### **Instrutor**
- **Rodrigo Gonçalves** ([@orodrigogo](https://github.com/orodrigogo))

---

## 🚀 Sobre a Rocketseat

A [Rocketseat](https://www.rocketseat.com.br) é uma plataforma de educação em tecnologia que tem como missão levar você até os seus objetivos de forma acelerada. Especializada em Node.js, ReactJS, React Native e outras tecnologias modernas.

### 📚 Next Level Week (NLW)

O NLW é um evento online e gratuito da Rocketseat que acontece várias vezes ao ano, onde em uma semana você desenvolve uma aplicação completa, do backend ao mobile, utilizando tecnologias modernas e as melhores práticas do mercado.

---

## 🔄 Atualizações Recentes

### **SDK 53 Compatibility**
- ✅ Projeto atualizado para Expo SDK 53
- ✅ Compatibilidade com a versão mais recente do Expo Go
- ✅ Todas as dependências atualizadas

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais durante a NLW da Rocketseat.

---

💜 **Feito com muito aprendizado durante a NLW da Rocketseat**

🚀 **#NextLevelWeek #ReactNative #Expo #Rocketseat**
