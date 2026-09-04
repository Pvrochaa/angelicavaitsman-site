# Checklist de publicação — Dra. Angelica Vaitsman

Rodar **antes** de tirar a prévia do ar e entregar como site definitivo.

---

## 1. Bloqueios — nada vai ao ar com isso pendente

- [ ] **Remover o `noindex`.** `<meta name="robots" content="noindex, nofollow">` no
  `<head>`. Enquanto estiver lá, o site não existe para o Google — e o objetivo
  inteiro do projeto é ser encontrado. Está marcado no código com
  `REMOVER QUANDO O CONTRATO FECHAR`.
- [ ] **Remover os outros 3 pontos de prévia** (mesmo marcador no código):
  a regra CSS `.previa` / `.rodape__previa`, a `<div class="previa">` no topo do
  body e o `<p class="rodape__previa">` no rodapé.
- [ ] **Domínio próprio.** `angelicavaitsman-site.vercel.app` não compete em busca
  local. Um `.com.br` custa ~R$ 40/ano no Registro.br.
- [ ] **Trocar as URLs absolutas do schema** (`image`, e `url` se for adicionado)
  para o domínio definitivo.

## 2. Confirmar com a Dra. Angelica antes de publicar

- [ ] **Formação:** o mestrado na UFF terminou em julho ou agosto de 2024? O
  LinkedIn diverge entre as duas abas.
- [ ] **São Leopoldo Mandic:** foi Especialização ou Residência? O LinkedIn usa os
  dois termos. A página diz "Especialização em Implantodontia".
- [ ] **Título de instrutora no INERO** — conferir a forma correta de anunciar.
- [ ] **Primeira consulta:** como funciona de fato? (hoje a página diz que o caso é
  avaliado antes de qualquer proposta e que cada etapa é explicada)
- [ ] **Atende convênio ou só particular?** A página não diz — e não deve dizer
  antes dela responder.
- [ ] **Uso da foto do procedimento** na seção Cirurgia: paciente está coberto e não
  identificável, mas a decisão de exibir é dela.

## 3. Conformidade CFO/CRO

- [x] CRO-RJ 48701 e responsável técnica no rodapé
- [x] Sem promessa de resultado, sem antes-e-depois, sem sensacionalismo
- [x] Sem depoimento de paciente como peça de captação — só nota agregada e link
      para o perfil do Google
- [ ] **Não publicar preço, forma de pagamento, parcelamento ou desconto.** O Código
      de Ética Odontológica restringe anunciar isso como forma de atrair paciente.
      Se for entrar algo nessa linha, validar antes com ela ou com o CRO-RJ.

## 4. Rastreamento

- [ ] **Criar propriedade GA4** e colar o snippet no ponto marcado no fim do
  `index.html`. O disparo de eventos já está pronto e roda em silêncio sem o ID.
- [ ] **LGPD antes de ligar:** consultório trata dado de saúde. Publicar aviso de
  privacidade e definir base legal antes de ativar analytics e o mapa do Google.
- [ ] Conferir no GA4 (DebugView) se `clique_whatsapp` e `clique_telefone` chegam,
  com o parâmetro `origem` indicando de qual bloco o clique saiu.

## 5. Google Business Profile

- [ ] Adicionar o site novo na ficha do Google — é o que amarra o perfil (5,0 com
  107 avaliações) à página e move o ponteiro na busca local.
- [ ] Conferir se categoria, horário e serviços da ficha batem com a página.

## 6. Técnico

- [x] Lazy loading (hero em `eager`, as demais em `lazy`)
- [x] Schema `Dentist` com endereço, telefone, horário, serviços e área atendida
- [x] Schema `Person` com formação e credenciais
- [ ] **Converter as 3 fotos para WebP.** Hoje somam 257 KB em JPEG — não é
  gargalo, mas WebP economiza ~40%. Precisa de ferramenta que não existe nesta
  máquina (sem Node, sem ImageMagick). Caminho manual: squoosh.app
- [ ] Rodar PageSpeed Insights depois do domínio definitivo
- [x] `og:url`, `og:image`, `canonical`, `twitter:card` e `theme-color` adicionados
- [ ] **Trocar as 3 URLs absolutas** (`og:url`, `og:image`, `canonical`) pelo domínio final
- [ ] Produzir arte `og:image` 1200×630 — hoje usa o retrato 400×400, que vira
  miniatura quadrada no WhatsApp em vez de card horizontal

## 7. Depois de publicar

- [ ] Solicitar indexação no Google Search Console
- [ ] Enviar sitemap (ou confirmar que a página única foi indexada)
- [ ] Conferir se o link do WhatsApp abre com a mensagem correta no celular
