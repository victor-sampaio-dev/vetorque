<!-- Repositório VITRINE (portfólio) do Vetorque — sem código-fonte. -->

<p align="center">
  <img src="docs/feature.png" alt="Vetorque — Gestão para oficinas mecânicas" width="100%">
</p>

<h1 align="center">Vetorque</h1>

<p align="center">
  <b>Sistema de gestão para oficinas mecânicas — 100% offline, no seu bolso.</b><br>
  Ordens de serviço, clientes, estoque, agenda e financeiro, direto no celular.
</p>

<p align="center">
  <img alt="React" src="https://img.shields.io/badge/React-18-149ECA?logo=react&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
  <img alt="Vite" src="https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white">
  <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white">
  <img alt="Capacitor" src="https://img.shields.io/badge/Capacitor-119EFF?logo=capacitor&logoColor=white">
  <img alt="Plataforma" src="https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=white">
</p>

> ⚠️ **Repositório de portfólio.** O código-fonte é fechado (produto comercial). Aqui você encontra a visão geral, as decisões técnicas e as telas do aplicativo.

---

## 🎯 O problema

Muitas oficinas mecânicas ainda controlam **ordens de serviço, estoque e financeiro no papel** — o que gera retrabalho, perda de informação e nenhuma visão do negócio. O **Vetorque** resolve isso colocando toda a gestão no celular, de forma simples e **funcionando sem internet**.

## ✨ Principais recursos

- 🔧 **Ordens de serviço** do orçamento à entrega — com veículo, KM, fotos, serviços e status
- 👥 **Clientes e veículos** com histórico e importação de contatos
- 📦 **Estoque de peças** com alerta de reposição
- 📅 **Agenda** de horários e serviços
- 💰 **Financeiro e relatórios** com painéis personalizáveis (arrastar, ocultar e trocar o tipo de gráfico)
- 🔒 **Local-first**: os dados ficam no próprio aparelho — privacidade total e uso offline

## 🛠️ Stack

| Camada | Tecnologias |
|---|---|
| **Front-end** | React 18, TypeScript, Vite, Tailwind CSS |
| **Estado / dados** | Zustand (persist em IndexedDB) |
| **Mobile** | Capacitor (empacotamento Android nativo) |
| **Gráficos** | SVG puro (sem biblioteca pesada) |

## 🧩 Decisões de arquitetura

- **Local-first com camada de dados plugável** — o app funciona 100% offline hoje, e a mesma arquitetura está pronta para virar um **SaaS** (sincronização em nuvem) apenas ligando o modo remoto.
- **Gráficos em SVG próprios** — em vez de uma lib pesada, componentes de gráfico feitos à mão (barras, linha, área, rosca) mantêm o bundle enxuto e o controle total do visual.
- **Feature flags de edição (Lite/Full)** — recursos de servidor (IA, envios em massa) ficam atrás de flags, permitindo evoluir para planos pagos sem reescrever o app.
- **Money como inteiro (centavos)** — evita erros de ponto flutuante no financeiro.

## 📸 Telas

| | | |
|:--:|:--:|:--:|
| ![Ordens](docs/screen-1.png) | ![Financeiro](docs/screen-2.png) | ![Detalhe da OS](docs/screen-3.png) |
| ![Controle de peças](docs/screen-4.png) | ![WhatsApp](docs/screen-5.png) | ![Resumo](docs/screen-6.png) |

## 🗺️ Roadmap

- [x] MVP offline publicado na Google Play (teste fechado)
- [ ] Compra vitalícia (desbloqueio do app local)
- [ ] Assinatura SaaS (nuvem, multi-dispositivo, relatórios avançados)
- [ ] Página pública por oficina (mini-site de contato)
- [ ] Multi-idioma (pt / en / es)

## 📱 Status

Em **teste fechado** na Google Play. Link para download público em breve.

---

<p align="center">
  Desenvolvido por <b>Victor Hugo Sampaio</b> · Contato: vetorquebr@gmail.com
</p>
