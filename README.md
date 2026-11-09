# Ateliê Nuvem — protótipo funcional

Protótipo navegável de catálogo de moda com carrinho, checkout e painel de pedidos. Foi criado para validar a experiência com a cliente antes da ligação ao Supabase e à Uazapi.

## Abrir

Abra `index.html` diretamente no navegador ou sirva esta pasta com qualquer servidor estático.

## O que já funciona

- Catálogo responsivo com filtros e imagens de demonstração.
- Carrinho persistido no `localStorage`.
- Checkout com nome, telefone e consentimento para receber atualização.
- Criação de protocolo de pedido e painel “Área da loja”.
- Estados de demonstração para substituir depois por Supabase.

## Próxima integração

1. Criar tabelas `products`, `product_variants`, `orders`, `order_items` e `notification_jobs` no Supabase.
2. Trocar o `localStorage` pelas consultas autenticadas do Supabase e aplicar RLS.
3. O checkout deve chamar uma Edge Function ou rota server-side que cria o pedido com preço/estoque validados.
4. O n8n recebe o evento e chama a Uazapi. Token e URL da Uazapi ficam apenas em credenciais do n8n, nunca no navegador.
5. Gravar tentativa, resposta, erro e status de cada mensagem para a cliente e para a dona.

O número do WhatsApp usado nos links é fictício (`5511999999999`) e deve ser trocado antes da publicação.
