<div align="center">

<img src="https://img.shields.io/badge/versão-1.0.0-1565C0?style=for-the-badge" />
<img src="https://img.shields.io/badge/status-Em%20Desenvolvimento-00838F?style=for-the-badge" />
<img src="https://img.shields.io/badge/plataforma-Android%20%7C%20iOS-2E7D32?style=for-the-badge" />
<img src="https://img.shields.io/badge/licença-MIT-6A1B9A?style=for-the-badge" />

<br /><br />

# <img src="./saquaremago-logo.png" width='240' />

### Guia turístico interativo da Capital do Surf

_Projeto de TCC — Universidade de Vassouras · Curso de Engenharia de Software_

<br />

[📱 Sobre o Projeto](#-sobre-o-projeto) •
[🚀 Funcionalidades](#-funcionalidades) •
[🛠️ Tecnologias](#️-tecnologias) •
[👥 Time](#-time)

</div>

---

## 📱 Sobre o Projeto

O **SaquaremaGO** é um aplicativo mobile desenvolvido para turistas e moradores explorarem a cidade de Saquarema RJ de forma prática e interativa. Com um mapa em tempo real, o usuário descobre pontos turísticos, eventos, restaurantes, trilhas e pontos de emergência próximos, com suporte a três idiomas.

> Saquarema é conhecida mundialmente como a **Capital do Surf**, sede de etapas do **WSL Championship Tour**. O app nasce para conectar visitantes à riqueza cultural, natural e gastronômica da cidade.

<br />

```
🗺️  Abre o app  →  Vê o mapa  →  Encontra o que precisa  →  Vai até lá
```

<br />

Este projeto é desenvolvido como **Trabalho de Conclusão de Curso (TCC)** na [Universidade de Vassouras](https://univassouras.edu.br), curso de **Engenharia de Software**, com foco em arquitetura de sistemas mobile, APIs REST geoespaciais e boas práticas de desenvolvimento.

---

## 🚀 Funcionalidades

### Para o Turista / Morador

- **🗺️ Mapa interativo** com pontos turísticos, eventos e estabelecimentos ao redor
- **🔍 Busca e filtros** por nome, categoria e distância
- **📍 Detalhe completo** de cada ponto — fotos, descrição, avaliações e "Como Chegar"
- **⭐ Favoritos** sincronizados com a conta do usuário
- **📅 Agenda de eventos** com filtro por data e localização
- **🚨 Pontos de emergência** — hospitais, delegacias e postos salva-vidas mais próximos
- **🗣️ Avaliações e comentários** sobre pontos turísticos
- **🎫 Cupons promocionais** de estabelecimentos parceiros
- **🛤️ Roteiros temáticos** — família, aventura, gastronomia
- **🌐 Multilíngue** — Português, Inglês e Espanhol

### Para o Administrador

- Cadastro e edição de pontos turísticos e eventos
- Moderação de avaliações e denúncias
- Envio de notificações push segmentadas
- Gerenciamento de planos premium para comerciantes
- Dashboard com métricas de uso e relatórios exportáveis

---

## 🛠️ Tecnologias

### Mobile

| Tecnologia                                          | Uso                                    |
| --------------------------------------------------- | -------------------------------------- |
| [React Native](https://reactnative.dev/)            | Framework do aplicativo mobile         |
| [Expo](https://expo.dev/)                           | Toolchain de build e desenvolvimento   |
| [React Navigation](https://reactnavigation.org/)    | Navegação entre telas                  |
| [Mapbox SDK](https://docs.mapbox.com/react-native/) | Mapa interativo e geolocalização       |
| [Firebase SDK](https://firebase.google.com/)        | Autenticação social (Google, Facebook) |

### Backend

| Tecnologia                                                    | Uso                                         |
| ------------------------------------------------------------- | ------------------------------------------- |
| [Node.js](https://nodejs.org/)                                | Ambiente de execução JavaScript server-side |
| [Express](https://expressjs.com/)                             | Framework HTTP para a API REST              |
| [Prisma](https://www.prisma.io/)                              | ORM para comunicação com o banco            |
| [PostgreSQL](https://www.postgresql.org/)                     | Banco de dados relacional                   |
| [PostGIS](https://postgis.net/)                               | Extensão para consultas geoespaciais        |
| [Redis](https://redis.io/)                                    | Cache e filas de notificações (Bull)        |
| [Firebase Admin SDK](https://firebase.google.com/docs/admin/) | Verificação de tokens e push notifications  |

### Infraestrutura

| Tecnologia                                               | Uso                                |
| -------------------------------------------------------- | ---------------------------------- |
| [Docker](https://www.docker.com/)                        | Ambiente local de desenvolvimento  |
| [GitHub Actions](https://github.com/features/actions)    | CI/CD automatizado                 |
| [Cloudflare R2](https://www.cloudflare.com/products/r2/) | Armazenamento de imagens           |
| [Sentry](https://sentry.io/)                             | Monitoramento de erros em produção |

---

## ⚙️ Como Rodar Localmente

### Pré-requisitos

- [Node.js](https://nodejs.org/) v18+
- [Docker](https://www.docker.com/) e Docker Compose
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- Emulador Android / iOS **ou** o app [Expo Go](https://expo.dev/client) no celular

<!-- ### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/saquaremago.git
cd saquaremago
```

### 2. Configure as variáveis de ambiente

```bash
cp .env.example .env
# Edite o .env com suas chaves (Mapbox, Firebase, etc.)
```

### 3. Suba o banco de dados

```bash
docker-compose up -d
# PostgreSQL + PostGIS + Redis estarão rodando localmente
```

### 4. Instale as dependências e rode as migrations

```bash
npm install
cd packages/database
npx prisma migrate dev
npm run seed         # Popula o banco com POIs reais de Saquarema
```

### 5. Inicie o backend

```bash
cd packages/api
npm run dev
# API rodando em http://localhost:3000
# Documentação em http://localhost:3000/api-docs
```

### 6. Inicie o app mobile

```bash
cd apps/mobile
npx expo start
# Escaneie o QR code com o Expo Go no celular
# ou pressione 'a' para abrir no emulador Android
```

---

## 🗺️ Roadmap

```
✅ Fase 0 · Setup  →  📱 Fase 1 · MVP  →  💬 Fase 2 · Comunidade  →  💰 Fase 3 · Premium
```

| Fase              | Período                   | Status          | Destaques                           |
| ----------------- | ------------------------- | --------------- | ----------------------------------- |
| **MVP**           | Sprints 0–6 · 14 semanas  | 🔵 Em andamento | Mapa, auth, busca, admin, lojas     |
| **Intermediária** | Sprints 7–10 · 8 semanas  | ⬜ Planejado    | Avaliações, roteiros, push, offline |
| **Monetização**   | Sprints 11–14 · 8 semanas | ⬜ Planejado    | Plano premium, cupons, IA, escala   |

--- -->

## 👥 Time

Desenvolvido com 🌊 por estudantes de Engenharia de Software da **Universidade de Vassouras**:

<br />

|     | Nome               | Papel           |
| --- | ------------------ | --------------- |
| 👨‍💻  | **Bruno Pires**    | Desenvolvimento |
| 👨‍💻  | **Josias Andrade** | Desenvolvimento |
| 👨‍💻  | **Lucas Borba**    | Desenvolvimento |
| 👨‍💻  | **Gabriel Rosa**   | Desenvolvimento |

<br />

> 🎓 Trabalho de Conclusão de Curso — Universidade de Vassouras  
> 📚 Curso de Engenharia de Software  
> 📅 2028

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

<div align="center">

Feito com ❤️ para Saquarema 🌊

</div>
