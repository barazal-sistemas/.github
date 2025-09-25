# 📦 Barazal Rastreador

**Barazal Rastreador** é uma plataforma completa para rastreamento de ativos móveis (principalmente veículos), voltada para empresas, autônomos e pessoas físicas. A solução oferece telemetria em tempo real, relatórios analíticos, notificações, controle de contratos e veículos, com gestão centralizada de usuários.

## 🎯 Visão Geral da Arquitetura

O sistema é composto por múltiplos microserviços, cada um com responsabilidades específicas:

### Core Services
- **API Tracker Management**: Gerenciamento central de contratos, veículos e módulos
- **API User Management**: Autenticação e autorização centralizada
- **API Devices Communication**: Comunicação com dispositivos IoT
- **API Notification Sender**: Sistema de notificações

### Business Services
- **API Contract Management**: Gestão de contratos e leads
- **Barazal Tracker (App)**: Frontend mobile e PWA
- **Sistema Administrativo**: Interface de gestão

### Infrastructure
- **Traccar**: Engine GPS
- **Nominatim API**: Geocodificação
- **RabbitMQ**: Mensageria
- **PostgreSQL + TimescaleDB**: Armazenamento principal
- **MongoDB**: Armazenamento de logs e eventos

## 🏗 Stack Tecnológica

### Backend
- Java 21
- Spring Boot 3.x
- Spring Security
- Spring Data JPA
- Spring Cloud
- RabbitMQ
- PostgreSQL + TimescaleDB
- MongoDB (em migração)

### Frontend
- Angular 17
- Ionic 7
- React 18
- TailwindCSS
- TypeScript

### DevOps
- Docker
- Kubernetes
- GitHub Actions
- DigitalOcean
- Prometheus + Grafana

## 🚀 Guia de Desenvolvimento

### Pré-requisitos
- Java 21
- Node.js 20+
- Docker & Docker Compose
- Maven
- Git

### Padrões de Código
- Clean Architecture
- SOLID Principles
- DDD (Domain-Driven Design)
- REST API Best Practices
- Event-Driven Architecture

### Convenções
- Branch naming: `feature/`, `bugfix/`, `hotfix/`, `release/`
- Commit messages: Conventional Commits
- API versioning: URL path versioning
- Documentation: OpenAPI/Swagger

## 📚 Documentação por Módulo

| Módulo                     | Repositório GitHub                                                                 | Descrição                                                                                     | Documentação |
|---------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|--------------|
| **API Tracker Management**| [BZSistemas.TrackerManagement](https://github.com/barazal-sistemas/BZSistemas.TrackerManagement) | CRUD de contratos, veículos, módulos, últimas posições, relatórios e dashboards.              | [tracker_management.md](docs/tracker_management.md) |
| **Barazal Tracker (App)** | [BZSistemas.Tracker](https://github.com/barazal-sistemas/BZSistemas.Tracker)       | Frontend Ionic PWA/Android/iOS com mapa, relatórios e gestão de frotas.                      | [tracker_frontend.md](docs/tracker_frontend.md) |
| **API Notification Sender** | [BZSistemas.NotificationSender](https://github.com/barazal-sistemas/BZSistemas.NotificationSender) | Envio de notificações por push e e-mail. Integra com MongoDB (migração futura planejada).     | [notification_sender.md](docs/notification_sender.md) |
| **API User Management**   | [BZSistemas.UserManagement](https://github.com/barazal-sistemas/BZSistemas.UserManagement) | Central de autenticação e autorização para todos os sistemas.                                | [user_management.md](docs/user_management.md) |
| **API Devices Communication** | [BZSistemas.DevicesCommunication](https://github.com/barazal-sistemas/BZSistemas.DevicesCommunication) | Comunicação com módulos via Traccar, webhooks, RabbitMQ e filas.                             | [devices_communication.md](docs/devices_communication.md) |
| **Lib de Segurança**      | [BZSistemas.bzs-security-lib](https://github.com/barazal-sistemas/BZSistemas.bzs-security-lib) | Biblioteca compartilhada com validações AuthZ/AuthN via filtros e tokenService.              | [security_lib.md](docs/security_lib.md) |
| **API de Contratação**    | [BZSistemas.ContractManagement](https://github.com/barazal-sistemas/BZSistemas.ContractManagement) | API de leads e contratos via landing page. Geração de PDF e fluxo de assinatura.             | [contract_management.md](docs/contract_management.md) |
| **Sistema Administrativo**| *(privado/local)*                                                                  | Interface React SSR com TailwindCSS. Gestão de usuários, módulos, contratos e templates.     | [admin.md](docs/admin.md) |
| **Traccar**               | https://www.traccar.org                                                            | Engine GPS de rastreamento utilizada para comunicação com módulos.                           | [traccar.md](docs/traccar.md) |
| **Nominatim API**         | *(privado/local)*                                                                  | Geocodificação e busca reversa baseada em OSM/Nominatim.                                     | [geolocation.md](docs/geolocation.md) |

## 🔒 Segurança

### Autenticação
- JWT-based authentication
- OAuth2/OpenID Connect
- Role-based access control (RBAC)

### Dados
- Encryption at rest
- TLS/SSL para comunicação
- Rate limiting
- Input validation

## 📊 Monitoramento

### Métricas
- Prometheus para coleta
- Grafana para visualização
- Alertas configurados

### Logs
- Centralized logging
- ELK Stack
- Log correlation

## 🤝 Contribuição

1. Fork o repositório
2. Crie sua feature branch
3. Commit suas mudanças
4. Push para a branch
5. Crie um Pull Request

## 📝 Licença

Este projeto é proprietário e confidencial. Todos os direitos reservados.
