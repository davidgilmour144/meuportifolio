# 🚀 David Gilmour | Portfolio Profissional

Portfolio pessoal desenvolvido com tecnologias modernas, focado em performance, acessibilidade e design responsivo.

![Portfolio Preview](./assets/preview.png)

## 📋 Sumário

- [Tecnologias](#-tecnologias)
- [Estrutura](#-estrutura)
- [Instalação](#-instalação)
- [Configuração](#-configuração)
- [Funcionalidades](#-funcionalidades)
- [Customização](#-customização)
- [Deploy](#-deploy)
- [Créditos](#-créditos)

---

## 🛠 Tecnologias

### Core
| Tecnologia | Versão | Uso |
|------------|--------|-----|
| [Tailwind CSS](https://tailwindcss.com/) | v3.4.x | Framework CSS utilitário |
| [Lucide Icons](https://lucide.dev/) | Latest | Biblioteca de ícones |
| [Google Fonts](https://fonts.google.com/) | - | Inter & Space Grotesk |

### Ferramentas de Desenvolvimento
| Ferramenta | Finalidade |
|------------|-----------|
| Live Server | Servidor de desenvolvimento local |
| VS Code | Editor de código |
| Git | Controle de versão |

---

## 📁 Estrutura

portfolio/
├── index.html          # Estrutura principal (HTML semântico)
├── styles.css          # Estilos customizados + complementos Tailwind
├── script.js           # Interatividade e animações
├── README.md           # Documentação
└── assets/             # Imagens e recursos (opcional)
└── preview.png

---

## ⚡ Instalação

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/portfolio.git
cd portfolio


2. Abra no navegador
# Opção 1: Abrir diretamente
open index.html

# Opção 2: Com Live Server (VS Code)
# Instale a extensão "Live Server" → Clique em "Go Live"
Nota: Não requer npm install! Todas as dependências são via CDN.


⚙️ Configuração
Tailwind Config (inline no HTML)

tailwind.config = {
    theme: {
        extend: {
            colors: {
                primary: '#0f172a',      // Fundo principal
                secondary: '#1e293b',    // Cards e seções
                accent: '#6b2bf5',       // Roxo destaque
                'accent-light': '#69d2e7', // Cyan destaque
                'text-muted': '#94a3b8',   // Texto secundário
            },
            fontFamily: {
                sans: ['Inter', 'system-ui', 'sans-serif'],
                display: ['Space Grotesk', 'sans-serif'],
            },
            animation: {
                'pulse-slow': 'pulse 8s ease-in-out infinite',
                'float': 'float 6s ease-in-out infinite',
                'slide': 'slide 20s linear infinite',
            }
        }
    }
}


Variáveis CSS Customizadas
/* Cores dinâmicas para JavaScript */
:root {
    --color-primary: #0f172a;
    --color-secondary: #1e293b;
    --color-accent: #6b2bf5;
    --color-accent-light: #69d2e7;
    --color-text-muted: #94a3b8;
}


✨ Funcionalidades
Animações

| Animação          | Descrição                  | Gatilho                        |
| ----------------- | -------------------------- | ------------------------------ |
| `fade-in`         | Entrada suave de elementos | Scroll (Intersection Observer) |
| `float`           | Flutuação do avatar        | Loop infinito                  |
| `pulse-slow`      | Pulsação do glow           | Loop infinito                  |
| `slide`           | Movimento diagonal         | Background projetos            |
| `hover:translate` | Elevação de cards          | Mouse hover                    |


Interatividade
✅ Filtro de Projetos - Filtragem por categoria (dados, automação, logística, sistemas)
✅ Menu Mobile - Hamburguer com transição suave
✅ Scroll Suave - Navegação entre seções
✅ Nav Ativa - Destaque automático da seção visível
✅ Navbar Inteligente - Esconde/mostra ao rolar
Seções
Hero - Apresentação com stats e CTAs
Projetos - 6 cases com métricas e filtros
Experiência - Timeline vertical alternada
Habilidades - 6 categorias com tags
Depoimentos - 3 cards com avaliações
Blog - 3 artigos preview
Certificações - 6 certificados com timeline
Contato - 4 canais (email, tel, linkedin, instagram)


🎨 Customização
Alterar Cores
Edite no <script> do Tailwind no index.html:
colors: {
    primary: '#SEU-COR-FUNDO',
    accent: '#SUA-COR-DESTAQUE',
}

Adicionar Projeto
No index.html, duplique um .project-card e altere:
data-category="nova-categoria"  <!-- Para filtro funcionar -->

Alterar Animações
No styles.css, ajuste:
.fade-in {
    transition-duration: 0.7s;  /* Mais rápido/lento */
    transform: translateY(20px); /* Distância menor/maior */
}


🚀 Deploy
GitHub Pages
Vá em Settings → Pages
Source: Deploy from a branch
Branch: main → /(root)
Salve e aguarde o link

Netlify
# Arraste a pasta para https://app.netlify.com/drop
# Ou use CLI:
netlify deploy --prod --dir .

Vercel
npm i -g vercel
vercel --prod

📱 Responsividade
| Breakpoint       | Layout                       |
| ---------------- | ---------------------------- |
| `< 640px`        | 1 coluna, menu hamburguer    |
| `640px - 1024px` | 2 colunas                    |
| `> 1024px`       | 3-4 colunas, menu horizontal |


♿ Acessibilidade
Navegação por teclado (Tab, Enter, Escape)
Contraste WCAG AA
prefers-reduced-motion respeitado
ARIA labels em botões
Foco visível em todos elementos interativos

📊 Resumo das Melhorias
| Técnica                 | Onde | Ganho                       |
| ----------------------- | ---- | --------------------------- |
| `will-change-transform` | CSS  | GPU acceleration            |
| `content-visibility`    | CSS  | ~20% menos render time      |
| `contain`               | CSS  | Isola reflows               |
| Throttle (100ms)        | JS   | Reduz cálculos de scroll    |
| `requestAnimationFrame` | JS   | Sincroniza com refresh rate |
| Passive listeners       | JS   | Melhora scroll touch        |
| Preconnect DNS          | HTML | ~100ms faster load          |
| Font display swap       | CSS  | Evita FOIT                  |
| Service Worker          | JS   | Cache offline               |

🎯 Métricas Esperadas
First Contentful Paint (FCP): < 1.5s
Largest Contentful Paint (LCP): < 2.5s
Cumulative Layout Shift (CLS): < 0.1
Time to Interactive (TTI): < 3.5s


📝 Changelog
v1.0.0 - 18/03/2026
✅ Migração completa para Tailwind CSS v3
✅ Refatoração em 3 arquivos separados (HTML/CSS/JS)
✅ Animações com Intersection Observer
✅ Filtro de projetos funcional
✅ Menu mobile responsivo
✅ 8 seções completas

👨‍💻 Autor
David Gilmour
📧 davidgilmour144@gmail.com
💼 LinkedIn
📷 Instagram
📄 Licença
