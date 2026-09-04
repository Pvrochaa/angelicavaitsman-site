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
- [ ] **Uso da foto do procedimento** na seção Cirurgia: paciente está coberto e não
  identificável, mas a decisão de exibir é dela.

### As 5 perguntas do FAQ que faltam

O bloco já está escrito e comentado no `index.html`, na seção **Perguntas**.
É só descomentar e preencher. Nenhuma envolve afirmação clínica nem preço:

1. **Quanto tempo dura a primeira consulta?**
2. **Atende convênio ou só particular?** — dizer *se* atende é informação de
   atendimento e pode entrar. **Não listar nomes de planos:** aí vira propaganda e
   o CFO restringe. Plano específico, a secretária responde no WhatsApp.
3. **Precisa levar radiografia ou exames anteriores?**
4. **Tem estacionamento por perto?** (Conde de Bonfim, altura do 422)
5. **Em quanto tempo respondem no WhatsApp?**

## 3. Conformidade CFO/CRO

- [x] CRO-RJ 48701 e responsável técnica no rodapé
- [x] Sem promessa de resultado, sem antes-e-depois, sem sensacionalismo
- [x] Sem depoimento de paciente como peça de captação — só nota agregada e link
      para o perfil do Google
- [ ] **Não publicar preço, forma de pagamento, parcelamento ou desconto.** O Código
      de Ética Odontológica restringe anunciar isso como forma de atrair paciente.
      Se for entrar algo nessa linha, validar antes com ela ou com o CRO-RJ.

## 4. Rastreamento

- [ ] **Contratar Plausible ou Umami** e colar a linha única no ponto marcado no fim
  do `index.html`. São cookieless, não coletam dado pessoal e **dispensam banner de
  consentimento** — num consultório, que trata dado de saúde, isso é bem mais
  defensável que GA4. O disparo de eventos já está pronto e funciona nos dois.
- [x] **Mapa sem pendência de LGPD:** carrega só no clique. A página não faz nenhuma
  requisição ao Google antes disso, então não há cookie de terceiro a consentir.
  Mesmo padrão serve para qualquer embed futuro.
- [ ] **Se optar por GA4 ou pixel da Meta** (para anúncio), aí voltam a ser
  obrigatórios: banner de consentimento, aviso de privacidade e base legal.
- [ ] Conferir se os eventos chegam: `clique_whatsapp`, `clique_telefone` e
  `abriu_mapa`, todos com o parâmetro `origem` indicando de qual bloco saiu.

## 5. Google Business Profile

- [ ] Adicionar o site novo na ficha do Google — é o que amarra o perfil (5,0 com
  107 avaliações) à página e move o ponteiro na busca local.
- [ ] Conferir se categoria, horário e serviços da ficha batem com a página.

## 6. Técnico

- [x] Lazy loading (hero em `eager`, as demais em `lazy`)
- [x] Schema `Dentist` com endereço, telefone, horário, serviços e área atendida
- [x] Schema `Person` com formação e credenciais
- [x] **WebP feito.** As 3 fotos passaram de 257 KB para 99 KB (-61%), servidas via
  `<picture>` com o JPEG como reserva
- [ ] Rodar PageSpeed Insights depois do domínio definitivo
- [x] `og:url`, `og:image`, `canonical`, `twitter:card` e `theme-color` adicionados
- [ ] **Trocar as 3 URLs absolutas** (`og:url`, `og:image`, `canonical`) pelo domínio final
- [x] **Arte `og:image` 1200×630 pronta** (`img/og-angelica-vaitsman.jpg`, 39 KB):
  lockup negativo sobre teal, com CRO e o selo 5,0. `twitter:card` em
  `summary_large_image`

## 7. Depois de publicar

- [ ] Solicitar indexação no Google Search Console
- [ ] Enviar sitemap (ou confirmar que a página única foi indexada)
- [ ] Conferir se o link do WhatsApp abre com a mensagem correta no celular
