# Pedido de serviços · SOS Limpeza

Página de pedido de higienização para clientes Residencial, HORECA e Transporte.
É um único ficheiro (`index.html`), sem servidor e sem base de dados. O logotipo já está dentro do ficheiro; `logo.png` é só uma cópia para outros usos.

## Como alterar (abrir `index.html` num editor de texto)

Procure o bloco que começa com `<script>` perto do fim do ficheiro.

- **Contactos:** linha `var CONTACT = { whatsapp: "...", email: "..." }`. O WhatsApp leva só dígitos, com o 244.
- **Preços do residencial e do HORECA:** lista `MOBILIARIO`. Cada linha tem `name`, `unit` e `price` (em Kwanzas, sem pontos). Para acrescentar um item, copie uma linha; para retirar, apague-a.
- **Preços do Transporte:** lista `services` dentro de `transporte`.
- **Campos do formulário:** lista `fields` de cada sector.
- **Texto da autorização de dados:** procure `Lei n.º 22/11` (aparece em dois sítios: no balão e na mensagem de WhatsApp).
- **Cores:** bloco `:root` no início, em `--navy`, `--brand` e `--gold`.

Depois de alterar, abra o `index.html` no navegador e faça um pedido de teste antes de publicar.

## Como publicar (resumo)

1. Criar o repositório no GitHub (conta da empresa, com verificação em dois passos) e carregar estes ficheiros.
2. Ligar o repositório a Cloudflare Pages ou Netlify (gratuito). Cada alteração guardada no repositório publica-se sozinha.
3. Ligar o domínio da empresa (HTTPS automático).
4. Links por sector: `https://SEU-ENDERECO/#residencial`, `#horeca` e `#transporte`.

## Limites

A página não guarda pedidos nem avisa por email. O pedido segue por WhatsApp, só depois de o cliente carregar em "Enviar por WhatsApp".
