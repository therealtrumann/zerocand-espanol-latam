# Identidade Visual — Florah Viva
**Produto:** Protocolo Cero Candidiasis
**Fonte:** zerocand.lovable.app (React/Lovable app)

---

## Paleta de Cores

### Cores Principais

| Token | HSL | Hex aproximado | Uso |
|---|---|---|---|
| `--primary` | `hsl(326, 42%, 55%)` | `#C27098` | Cor principal — Rosa Malva |
| `--background` | `hsl(332, 100%, 99%)` | `#FFF5F8` | Fundo — Branco rosado |
| `--secondary` | `hsl(332, 44%, 92%)` | `#F5E0E8` | Seções alternadas — Rosa claro |
| `--foreground` | `hsl(330, 8%, 40%)` | `#6B5B60` | Texto principal |

### Tons Complementares

| Token | HSL | Hex aproximado | Uso |
|---|---|---|---|
| `--green-natural` | `hsl(145, 40%, 85%)` | `#BFE0CC` | Banner topo — Verde suave |
| `--success-foreground` | `hsl(145, 50%, 30%)` | `#2D7349` | Texto sobre verde |
| `--rose-pale` | `hsl(332, 60%, 94%)` | `#FAE6EE` | Cards, destaques suaves |
| `--rose-medium` | `hsl(332, 44%, 81%)` | `#E8BFCF` | Separadores, bordas |
| `--rose-burnt` | `hsl(15, 45%, 60%)` | `#C47A5A` | Acento quente/terra |
| `--beige-warm` | `hsl(30, 25%, 94%)` | `#F5EDE4` | Fundo neutro aconchegante |
| `--violet-soft` | `hsl(290, 20%, 78%)` | `#C4A8CC` | Acento roxo suave |

### Sistema Completo (Shadcn/Tailwind)

```
--card:              hsl(0, 0%, 100%)       — Branco puro para cards
--card-foreground:   hsl(330, 8%, 40%)      — Texto em cards
--muted:             hsl(332, 44%, 92%)     — Elementos apagados
--muted-foreground:  hsl(330, 8%, 60%)      — Texto secundário
--accent:            hsl(290, 20%, 78%)     — Destaque roxo suave
--border:            hsl(332, 44%, 92%)     — Bordas suaves
--ring:              hsl(326, 42%, 55%)     — Foco/ring (=primary)
--destructive:       hsl(0, 84.2%, 60.2%)  — Vermelho para erros
```

---

## Tipografia

### Fontes Utilizadas

| Papel | Fonte | Pesos | CDN |
|---|---|---|---|
| **Títulos / Headlines** | Playfair Display | 400, 500, 600, 700 | Google Fonts |
| **Corpo / UI / Botões** | Poppins | 300, 400, 500, 600, 700 | Google Fonts |

### Import Google Fonts

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Hierarquia Tipográfica

```
H1 (Hero headline):  Playfair Display 700, ~3xl–5xl
H2 (Seções):         Playfair Display 700, ~2xl–4xl
H3 (Subseções):      Poppins 600, ~xl–2xl
Body:                Poppins 400, base–lg
CTAs/Botões:         Poppins 500–600
Labels/Badges:       Poppins 500, sm
```

---

## Princípios de Design

### Border Radius
```css
--radius: 1rem;  /* 16px — cantos arredondados suaves em todo o sistema */
```
Cards usam `rounded-2xl` (1.5rem) e `rounded-3xl` (2rem) para elementos hero.

### Sombras
- `shadow-sm` — inputs, botões secundários
- `shadow-md` — cards de conteúdo
- `shadow-lg` — cards de preço
- `shadow-2xl` — imagem hero

### Espaçamento
- Seções: `py-8 md:py-20` (mobile-first)
- Container máximo: `max-w-7xl mx-auto px-4`

### Animações
- `animate-fade-in` — entradas suaves em elementos hero

---

## Estilo Visual — Diretrizes

### Identidade
- **Estilo:** Feminino, acolhedor, clínico-natural
- **Tom visual:** Suave e reconfortante, sem agressividade
- **Associações:** Lavanda, saúde natural, pureza, equilíbrio
- **Imagem hero:** `/images/hero-lavender.webp` — lavanda como símbolo de cura e feminilidade

### Logotipo
- Formato: circular
- Borda: `border-2 border-primary/30` (rosa malva 30% opacidade)
- Tamanho: `w-24 h-24 md:w-32 md:h-32`

### Ícones
- Biblioteca: Lucide React
- Check/confirmação: verde (`text-success-foreground`)
- X/rejeição: cinza (`text-muted-foreground`)
- Estrelas: dourado (depoimentos)
- Coração, sparkles, gift: decorativos

### Layout de Seções

```
1. Banner topo (verde natural) — anúncio exclusivo
2. Hero (background branco rosado) — headline + CTA + imagem
3. Dor/Problema (fundo secundário rosa claro) — 3 colunas
4. Etapas (branco) — timeline horizontal
5. Depoimentos (fundo secundário) — carrossel
6. Módulos (branco) — grid de 6
7. Para quem é (fundo card) — 2 colunas
8. Preços (destaque) — 2 cards
9. Custo da inércia (fundo secundário) — comparação
10. Urgência (destaque primário) — lista de consequências
11. Sobre a marca (branco) — 3 pilares
12. FAQ (fundo suave) — acordeão
```

---

## Tokens CSS Completos

```css
/* Copiar para globals.css */
:root {
  --background: 332 100% 99%;
  --foreground: 330 8% 40%;
  --card: 0 0% 100%;
  --card-foreground: 330 8% 40%;
  --popover: 0 0% 100%;
  --popover-foreground: 330 8% 40%;
  --primary: 326 42% 55%;
  --primary-foreground: 0 0% 100%;
  --secondary: 332 44% 92%;
  --secondary-foreground: 330 8% 40%;
  --muted: 332 44% 92%;
  --muted-foreground: 330 8% 60%;
  --accent: 290 20% 78%;
  --accent-foreground: 330 8% 40%;
  --success: 145 40% 85%;
  --success-foreground: 145 50% 30%;
  --destructive: 0 84.2% 60.2%;
  --destructive-foreground: 0 0% 100%;
  --border: 332 44% 92%;
  --input: 332 44% 92%;
  --ring: 326 42% 55%;
  --radius: 1rem;

  /* Tons customizados Florah Viva */
  --rose-pale: 332 60% 94%;
  --rose-medium: 332 44% 81%;
  --rose-burnt: 15 45% 60%;
  --beige-warm: 30 25% 94%;
  --violet-soft: 290 20% 78%;
  --green-natural: 145 40% 85%;
}
```
