# Hopf Metais — Landing Page de Captura

Página de captura de alta conversão para a **Hopf** (marca premium de metais sanitários da Hope Metais).
Vende **banheiros completos** (ambientes de metais que já combinam) em vez de peças isoladas, com CTA para **projeto consultivo** via WhatsApp.

🔗 **Produção:** https://hopf-landing.vercel.app

---

## Como funciona (stack)

- **1 arquivo:** [`index.html`](index.html) — HTML + CSS + JS, tudo self-contained (sem build, sem dependências).
- Fontes via Google Fonts (Cormorant Garamond + Jost).
- Imagens de **exemplo** via Unsplash (trocar por fotos reais da Hopf — ver abaixo).
- Deploy estático na **Vercel** ([`vercel.json`](vercel.json)).

Para editar: abra o `index.html` em qualquer editor. Para ver localmente, é só abrir o arquivo no navegador.

---

## ⚠️ O que precisa ser trocado antes de rodar tráfego

1. **WhatsApp** — no final do `index.html`, na tag `<script>`:
   ```js
   const WHATSAPP = "5511999999999"; // <- trocar por: 55 + DDD + número do cliente
   ```
   Todos os formulários (e o popup) enviam o lead pré-formatado para esse número.

2. **Imagens** — hoje são fotos genéricas do Unsplash. Substituir pelas **fotos reais dos metais/ambientes Hopf**.
   Os endereços das imagens aparecem no HTML como `background-image:url('https://images.unsplash.com/...')`
   e no objeto `IMGS = {...}` dentro do `<script>` (usado no popup).

3. **Depoimentos** — os 3 depoimentos (seção "Por que exigentes escolhem a Hopf") são **ilustrativos**.
   Trocar por depoimentos reais de clientes.

4. **Preços e itens dos kits** — valores de referência (Lavabo R$ 2.200 / Social R$ 3.500 / Suíte R$ 4.900).
   Ajustar conforme o mix e a tabela real da Hopf.

---

## Estrutura da página (ordem das seções)

1. **Hero** — PUV: "O banheiro completo que já nasce em perfeita harmonia"
2. **Vitrine / Ambientes** — Lavabo · Banheiro Social · Suíte Master (cards + popup)
3. **Big Idea** — a grande oportunidade
4. **Problema** — "montar um banheiro é um campo minado"
5. **Virada** — imagine receber o banheiro inteiro
6. **Autoridade** — Hope Metais + estatísticas
7. **Como funciona** — 3 passos
8. **Comparação** — compra tradicional × Hopf
9. **Programa Arquitetos** — cashback/comissões
10. **Prova social** — selos + depoimentos
11. **FAQ / quebra de objeções**
12. **Oferta + escassez**
13. **Formulário** (âncora `#form`) + **Popup** (modal reutilizável)

Captura de leads: todos os CTAs abrem um **popup** com formulário; ao enviar, abre o WhatsApp com os dados preenchidos.

---

## Deploy (Vercel)

Já está conectado à conta Vercel `v4-persona-s-projects`. Para publicar uma nova versão:

```bash
vercel deploy --prod --yes
```

O domínio `hopf-landing.vercel.app` aponta sempre para a última versão em produção.

---

_Handover: página criada como material de partida. Prioridades para o próximo gestor: (1) WhatsApp real, (2) fotos reais, (3) depoimentos reais, (4) revisar preços/itens dos kits._
