<!-- Repositório de portfólio do Vetorque — sem código-fonte. -->

<p align="center">
  <img src="/feature.png" alt="Vetorque — Gestão para oficinas mecânicas" width="100%">
</p>

<h1 align="center">Vetorque</h1>

<p align="center">
  Sistema de gestão para oficinas mecânicas — offline-first, no celular.<br>
  Ordens de serviço, clientes, estoque, agenda e financeiro em um só app.
</p>

<p align="center">
  <img alt="React" src="https://img.shields.io/badge/React-18-149ECA?logo=react&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
  <img alt="Vite" src="https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white">
  <img alt="Tailwind CSS" src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white">
  <img alt="Capacitor" src="https://img.shields.io/badge/Capacitor-119EFF?logo=capacitor&logoColor=white">
  <img alt="Android" src="https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=white">
</p>

> Repositório de portfólio. O código-fonte é fechado (produto comercial). Aqui estão a visão geral, as decisões técnicas e as telas do aplicativo.

---

## O problema

Muitas oficinas mecânicas ainda controlam ordens de serviço, estoque e financeiro no papel — o que gera retrabalho, perda de informação e nenhuma visão do negócio. O Vetorque coloca toda a gestão no celular, de forma simples e funcionando sem internet.

## Recursos

- Ordens de serviço do orçamento à entrega, com veículo, KM, fotos, serviços e status
- Cadastro de clientes e veículos, com histórico e importação de contatos
- Controle de estoque de peças, com alerta de reposição
- Agenda de horários e serviços
- Financeiro e relatórios com painéis personalizáveis (reordenar, ocultar e trocar o tipo de gráfico)
- Local-first: os dados ficam no próprio aparelho — privacidade total e uso offline

## Stack

| Camada | Tecnologias |
|---|---|
| Front-end | React 18, TypeScript, Vite, Tailwind CSS |
| Estado e dados | Zustand com persistência em IndexedDB |
| Mobile | Capacitor (empacotamento Android nativo) |
| Gráficos | SVG próprio, sem biblioteca externa |

## Decisões de arquitetura

- Local-first com camada de dados plugável: o app funciona 100% offline hoje, e a mesma arquitetura está preparada para evoluir para um SaaS (sincronização em nuvem) apenas habilitando o modo remoto.
- Gráficos em SVG próprios, no lugar de uma biblioteca pesada, mantendo o bundle enxuto e o controle total do visual.
- Feature flags de edição (Lite/Full): recursos de servidor ficam atrás de flags, permitindo introduzir planos pagos sem reescrever o app.
- Valores monetários como inteiros (centavos), evitando erros de ponto flutuante no financeiro.

## Telas

| | | |
|:--:|:--:|:--:|
| <img src="/screen-1.png" width="240"> | <img src="/screen-2.png" width="240"> | <img src="/screen-3.png" width="240"> |
| <img src="/screen-4.png" width="240"> | <img src="/screen-5.png" width="240"> | <img src="/screen-6.png" width="240"> |

## Roadmap

- [x] MVP offline publicado na Google Play (teste fechado)
- [ ] Compra vitalícia (desbloqueio do app local)
- [ ] Assinatura SaaS (nuvem, multi-dispositivo, relatórios avançados)
- [ ] Página pública por oficina
- [ ] Multi-idioma (pt / en / es)

## Status

Em teste fechado na Google Play. Link para download público em breve.

---

<p align="center">
  Desenvolvido por Victor Hugo Sampaio — vetorquebr@gmail.com
</p>
