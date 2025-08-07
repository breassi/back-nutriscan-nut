# 🍽️ NutriScan – Assistente de Nutrição por Visão Computacional

> 📸 IA que analisa fotos de pratos para fornecer controle nutricional realista e sugestões personalizadas para balanceamento alimentar.

![NutriScan Banner](./docs/assets/banner-nutriscan.png)

---

## 📘 Sumário

- [🧩 Visão Geral](#-visão-geral)
- [✨ Funcionalidades](#-funcionalidades)
- [🔬 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [📱 Arquitetura](#-arquitetura)
- [💡 Diferenciais](#-diferenciais)
- [📈 Roadmap](#-roadmap)
- [🔐 Privacidade e Ética](#-privacidade-e-ética)
- [🛠️ Como Contribuir](#️-como-contribuir)
- [🚀 Como Executar Localmente](#-como-executar-localmente)
- [📄 Licença](#-licença)

---

## 🧩 Visão Geral

Manter o controle nutricional no dia a dia pode ser complicado e demorado.  
O **NutriScan** permite que o usuário simplesmente tire uma foto do prato e receba uma análise detalhada de:

- Tipos de alimentos presentes
- Quantidade de calorias, carboidratos, proteínas e gorduras
- Sugestões para balancear a refeição conforme metas pessoais

Usando **visão computacional** e **deep learning**, o NutriScan automatiza o diário alimentar e torna a nutrição prática e personalizada.

---

## ✨ Funcionalidades

| Funcionalidade                 | Descrição                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------------------|
| 📷 Análise de Imagens          | Classificação e identificação dos alimentos presentes na foto                             |
| 🔢 Cálculo Nutricional         | Estimativa automática de calorias e macro/micronutrientes                                 |
| 📊 Diário Alimentar            | Registro automático das refeições diárias com histórico e evolução                        |
| 🎯 Metas Nutricionais          | Definição de objetivos personalizados (perda de peso, ganho muscular, manutenção)         |
| 💡 Recomendações em Tempo Real | Sugestões para balanceamento nutricional com base no prato analisado                      |
| 🗓️ Histórico e Relatórios      | Visualização gráfica do consumo nutricional ao longo do tempo                             |

---

## 🔬 Tecnologias Utilizadas

| Área             | Tecnologias                                                |
|------------------|------------------------------------------------------------|
| Backend          | Go (Gin Framework), gRPC                                   |
| Visão Computacional | TensorFlow, OpenCV, PyTorch (microserviço Python)         |
| Deep Learning    | Modelos CNN para reconhecimento de alimentos              |
| Banco de Dados   | PostgreSQL (dados do usuário), Redis (cache de imagens)   |
| Frontend         | React Native (mobile), TailwindCSS                         |
| Armazenamento    | AWS S3 (fotos), MinIO (alternativa open-source)            |
| DevOps           | Docker, Kubernetes, GitHub Actions                         |

---

## 📱 Arquitetura

                +-----------------------+
                |     Mobile App        |
                |   (React Native)      |
                +----------+------------+
                           |
                           v
               +-----------+------------+
               |       API Gateway      |
               |        (Go Gin)        |
               +-----------+------------+
                           |
       +-------------------+-------------------+
       |                   |                   |
       v                   v                   v
+----------------+ +--------------------+ +--------------------+
| Image Upload | | Nutrition Engine | | User Profile |
| (AWS S3/MinIO)| | (Python TensorFlow) | | & Data Storage |
+----------------+ +--------------------+ +--------------------+


        +---------------------------------------------+
        |        PostgreSQL / Redis / S3 Storage       |
        +---------------------------------------------+

---

## 💡 Diferenciais

- ✅ **Nutrição por Imagem**: elimina a necessidade de anotações manuais
- ✅ **Feedback Imediato**: recomendações para ajustar cada refeição em tempo real
- ✅ **Diário Alimentar Automatizado**: histórico completo sem esforço extra do usuário
- ✅ **Personalização Total**: metas e preferências individuais incorporadas ao modelo
- ✅ **Privacidade e Segurança**: dados criptografados e controle total pelo usuário

---

## 🔐 Privacidade e Ética

O NutriScan prioriza a proteção dos dados dos usuários:

- Consentimento claro e explícito para uso de imagens e dados
- Armazenamento seguro com criptografia
- Nenhum compartilhamento com terceiros sem autorização
- Transparência nas análises e recomendações

---

## 🛠️ Como Contribuir

1. Fork este repositório  
2. Crie uma branch: `git checkout -b feature/nova-funcionalidade`  
3. Commit suas alterações: `git commit -m 'feat: adiciona nova funcionalidade'`  
4. Push para seu fork: `git push origin feature/nova-funcionalidade`  
5. Abra um Pull Request  

Contribuições são bem-vindas de desenvolvedores, nutricionistas, especialistas em IA e designers UX!

---

## 🚀 Como Executar Localmente

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/nutriscan.git
cd nutriscan

# Backend (Go Gin)
cd backend
go mod download
go run main.go

# Frontend (React Native)
cd ../frontend
npm install
npm run start
```

## ⚠️ Requisitos: 
Go 1.20+, Node.js 18+, Docker (para TensorFlow e serviços Python)

## 📄 Licença
Distribuído sob a licença MIT. Consulte o arquivo LICENSE para mais informações.

## 💙 Agradecimentos
NutriScan nasceu do desejo de facilitar a alimentação saudável, usando tecnologia de ponta para que nutrição e tecnologia caminhem juntas.

"A melhor dieta é aquela que entende você — agora com IA para te ajudar a escolher o caminho." 🍏

Desenvolvido com carinho por **Breno Assis**
