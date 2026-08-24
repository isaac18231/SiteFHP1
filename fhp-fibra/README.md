# FHP Fibra — Site institucional

Site estático (HTML + CSS + JS puro) da FHP Fibra: apresentação da empresa, planos, "quem somos", processo de contratação, contato e modais de login/pagamento.

## Estrutura

```
fhp-fibra/
├── index.html
├── style.css
└── images/
    └── hero.png   <- imagem de destaque do hero (já incluída)
```

## Como colocar no GitHub

1. Crie um repositório novo no GitHub (pode ser público), por exemplo `fhp-fibra`.
2. Envie estes arquivos para a raiz do repositório (mantendo a pasta `images/`):
   - pela interface web do GitHub: "Add file" → "Upload files" → arraste `index.html`, `style.css` e a pasta `images` (com `hero.png` dentro);
   - ou pelo terminal:
     ```bash
     git init
     git add .
     git commit -m "Site FHP Fibra"
     git branch -M main
     git remote add origin https://github.com/SEU-USUARIO/fhp-fibra.git
     git push -u origin main
     ```

## Como publicar (GitHub Pages)

1. No repositório, vá em **Settings → Pages**.
2. Em "Build and deployment", selecione **Deploy from a branch**.
3. Escolha a branch `main` e a pasta `/root`, depois clique em **Save**.
4. Em alguns minutos o site ficará disponível em:
   `https://SEU-USUARIO.github.io/fhp-fibra/`

## Observações

- O botão "Acessar plano" abre um modal de pagamento com links de checkout ainda vazios (`href="#"`). No `index.html`, procure o comentário `Cole aqui os links de checkout do PagSeguro` e substitua os `#` pelos links reais gerados no seu painel do PagSeguro para Pix, débito, crédito e boleto.
- O formulário de contato e o de login/cadastro são apenas visuais (front-end): eles não enviam dados a lugar nenhum ainda. Se quiser que funcionem de verdade (enviar e-mail, salvar cadastro, autenticar usuário), será preciso conectar a um backend ou serviço externo (ex: Formspree, Firebase, PagSeguro API, etc.).
