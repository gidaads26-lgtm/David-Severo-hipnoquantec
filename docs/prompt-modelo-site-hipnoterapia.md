# Prompt: modelo de site para profissional de Hipnoterapia Clínica

Baseado no site do David Severo (HipnoQuantec®). Serve para criar o mesmo site, com a mesma ordem de seções, design e comportamento, para outro profissional.

## Como usar

1. Crie uma pasta nova para o projeto e coloque nela:
   - `modelo-base.html`: o `index.html` deste repositório (`github.com/gidaads26-lgtm/david-severo-hipnoquantec`). É a referência visual e de código.
   - `img/`: as fotos do novo profissional (lista na ficha abaixo).
   - Opcional: briefing, textos do cliente, logo, PDF de credenciais.
2. Preencha a **Ficha do profissional** (seção 3 do prompt). Pode deixar campos em branco: o site sai com marcações `[a preencher: ...]` visíveis nesses pontos, para você completar depois.
3. Cole tudo a partir de "PROMPT" no Claude Code, aberto na pasta do projeto.

---

## PROMPT

### 1. Papel e objetivo

Atue como copywriter sênior e desenvolvedor(a) front-end. Crie o site institucional de um(a) profissional de Hipnoterapia Clínica a partir do arquivo `modelo-base.html`, que é o site de outro profissional já publicado.

Mantenha do modelo: a ordem das seções, a estrutura HTML de cada bloco, todo o CSS, todo o JavaScript, as animações, os botões e o comportamento no celular. Troque: todo o conteúdo (textos, nomes, fotos, links, vídeos, endereço, metatags, imagem de compartilhamento) pelos dados da Ficha. Nenhum texto, nome, marca ou link do profissional original pode sobrar no site novo (procure por "David", "Severo", "HipnoQuantec", "Quantec", "Biomagnético", "Praia Grande", "Mário Tamashiro", "5513998072472", "davidseveroh" e "Nasa" antes de entregar).

Se o `modelo-base.html` não estiver na pasta, construa o site do zero seguindo as seções 4, 5, 6 e 7 deste prompt, que descrevem o modelo em detalhe.

### 2. Regras gerais

- Português do Brasil. Linguagem neutra de gênero dirigida ao visitante ("você", "quem chega", "cada pessoa"), sem "bem-vindo/a" nem "o paciente / a paciente". O(a) profissional pode ter gênero definido nos textos sobre ele(a).
- Não use travessão (—) nos textos. Use ponto, vírgula ou dois-pontos.
- Campo da Ficha vazio → escreva `[a preencher: descrição do que falta]` no lugar, visível, e liste no relatório final. Nunca invente nome, formação, registro, número de atendimentos, preço, depoimento ou estudo.
- Textos enviados pelo cliente têm prioridade sobre os textos-padrão abaixo. Ajuste só o necessário para cumprir as regras da seção 8 (e avise o que mudou).

### 3. Ficha do profissional (preencher)

```yaml
# IDENTIDADE
nome_profissional:            # ex.: Ana Ribeiro
genero_profissional:          # feminino | masculino | neutro (só para os textos sobre a pessoa)
nome_da_marca:                # nome do método ou consultório; se não houver, use o nome do profissional
marca_registrada:             # sim | não  (se sim, usar ® após o nome da marca)
subtitulo_da_marca:           # aparece abaixo do logo, ex.: "Hipnoterapia clínica para ansiedade"
foco_principal:               # o tema central do site, ex.: ansiedade | autoestima | fobias | luto | sono
publico:                      # quem o site quer atrair, em uma frase
registro_profissional:        # ex.: CRP 06/000000, ou "não possui" (veja seção 8)
formacoes:                    # lista curta e verificável (curso, instituição, ano)

# RECURSOS / ATENDIMENTOS (de 1 a 3; o site se ajusta à quantidade)
recurso_1:                    # o principal, ganha o bloco com painel. ex.: Hipnose Clínica
recurso_1_resumo:             # uma frase simples
recurso_2:                    # ex.: PNL | Terapia Breve | Auto-hipnose guiada | (vazio)
recurso_2_resumo:
recurso_3:                    # ex.: Mindfulness | EFT | Reiki | (vazio)
recurso_3_resumo:
recurso_em_destaque:          # qual dos três recebe o card escuro "Diferencial" no Método
recursos_complementares_restricoes:  # contraindicações ou cuidados que precisam aparecer no texto

# ATENDIMENTO
cidade_uf:                    # ex.: Campinas – SP
endereco_completo:            # rua, número, bairro, cidade – UF, CEP (ou "somente online")
link_google_maps:             # link do perfil no Google Maps
atende_online:                # sim | não
plataforma_online:            # Zoom | Google Meet | WhatsApp vídeo
abrangencia_online:           # ex.: todo o Brasil | Brasil e exterior
primeira_consulta_nome:       # ex.: consulta de avaliação | anamnese | sessão inicial
primeira_consulta_cobrada:    # sim | não
duracao_e_valor_no_site:      # não | sim (se sim, informar abaixo)
duracao_e_valor:

# CONTATO E REDES
whatsapp_numero:              # só dígitos com DDI e DDD, ex.: 5511999998888
whatsapp_mensagem:            # ex.: Olá! Vim pelo site e gostaria de agendar uma consulta.
instagram_url:
youtube_url:                  # opcional
outras_redes:                 # opcional: TikTok, Facebook, LinkedIn
email_contato:                # opcional, aparece no rodapé

# PROFISSIONAIS (1 ou 2)
segundo_profissional:         # não | sim (se sim, repetir nome, papel, bio, foto e registro)
bio_curta:                    # 2 parágrafos, primeira pessoa ("Olá, sou...")
papel_no_metodo:              # aparece em pílula abaixo do nome, ex.: Hipnoterapia Clínica e PNL

# DEPOIMENTOS EM VÍDEO (YouTube), na ordem de exibição
depoimentos:
  - video_id:                 # o código depois de watch?v= ou youtu.be/
    nome_exibido:             # opcional; vazio = só "Depoimento"
    foto_capa:                # arquivo em img/ (opcional; vazio = miniatura do YouTube)
    autorizacao_por_escrito:  # sim | não  (sem autorização, não publicar)

# FOTOS (colocar em img/)
foto_hero:                    # retrato vertical, fundo limpo, mínimo 900×1100
foto_perfil:                  # retrato para a seção "Quem vai atender você"
foto_local:                   # consultório ou sala de atendimento (horizontal)
logo:                         # opcional (SVG ou PNG transparente); sem logo, usar o selo de anéis do modelo

# PUBLICAÇÃO
dominio_final:                # ex.: https://anaribeiro.com.br ou https://nome.vercel.app
paleta:                       # manter azul-marinho e dourado | informar 2 cores da marca
ferramentas_de_medicao:       # nenhuma | Google Analytics | Meta Pixel (exige aviso de cookies)
```

### 4. Ordem fixa das seções

Mantenha exatamente esta ordem, os mesmos ids e as mesmas classes do modelo. Seções com fundo "tint" e fundo claro se alternam; se remover um bloco de recurso, refaça a alternância para nunca ficarem duas seções iguais seguidas.

| # | Seção (comentário no HTML) | id | Fundo |
|---|---|---|---|
| 0 | Barra superior + menu | `topbar` | claro, fixa |
| 1 | HERO | `#inicio` | claro |
| 2 | CREDENCIAIS | `#credenciais` | faixa |
| 3 | ANTES DE TUDO | `#identificacao` | tint |
| 4 | MÉTODO | `#metodo` | claro |
| 5 | ATENDIMENTOS: RECURSO 1 (split + painel) | `#recurso-1` | tint |
| 6 | ATENDIMENTOS: RECURSO 2 (texto solo) | `#recurso-2` | claro |
| 7 | ATENDIMENTOS: RECURSO 3 (split + painel) | `#recurso-3` | tint |
| 8 | COMO FUNCIONA: PRIMEIRO PASSO | `#avaliacao` | claro, bloco escuro |
| 9 | LOCAL DE ATENDIMENTO | `#local` | tint |
| 10 | DEPOIMENTOS | `#depoimentos` | claro |
| 11 | QUEM É | `#profissionais` | tint |
| 12 | DÚVIDAS (FAQ) | `#faq` | claro |
| 13 | FECHAMENTO | `#fechamento` | tint, bloco escuro |
| 14 | Rodapé + botão flutuante (celular) + modal de vídeo | `footer` | escuro |

Use ids descritivos com o nome real do recurso (ex.: `#hipnose`, `#pnl`), e atualize todos os links internos (menu, cards, rodapé) para eles.

Abaixo, a estrutura de cada seção com o texto-padrão neutro. Troque `{{campos}}` pelos dados da Ficha. "Rótulo" é a pílula com ponto pulsante que fica acima do título.

**0. Barra superior e menu**
- Logo à esquerda: selo + `{{nome_da_marca}}` com `{{subtitulo_da_marca}}` embaixo.
- Links: O método · `{{recurso_em_destaque}}` · Depoimentos · Profissional (ou "Profissionais") · Dúvidas. Botão "Agendar consulta agora".
- Abaixo de 1260px: botão "Menu" que abre um cartão flutuante no canto superior direito, com os links entrando em sequência, fundo escurecido atrás, fecha ao clicar num link, fora do cartão ou na tecla Esc, e traz o botão de agendar no fim.

**1. Hero**
- H1: "Um cuidado individualizado para você recuperar o equilíbrio e voltar a viver com mais leveza." (adapte ao `{{foco_principal}}`)
- Texto: "Cada história emocional é única, e o cuidado também precisa ser. Com a Hipnoterapia Clínica, trabalhamos os pensamentos, as emoções e os padrões ligados a `{{foco_principal}}`, em um plano construído a partir da sua avaliação."
- Botões: "Quero minha consulta de avaliação" (principal, WhatsApp) e "Ver como o método funciona" (contorno, leva a `#metodo`).
- Três selos curtos (só no computador; escondidos no celular): "Avaliação antes do plano" · "Recursos integrados" (ou "Atendimento individual" se houver só um recurso) · "Acompanhamento contínuo".
- Foto do profissional à direita (no celular, acima ou abaixo do texto, centralizada), com os anéis dourados desenhados atrás.

**2. Credenciais** (faixa com 4 itens, ícones de linha fina)
- Um item por recurso: nome + `{{recurso_n_resumo}}`.
- Último item: `{{nome_da_marca}}` + "Método exclusivo" (ou "Atendimento individualizado").
- Com menos de 3 recursos, complete até 4 itens com: "Presencial e online" · "Avaliação individual" · `{{registro_profissional}}` (se houver).

**3. Antes de tudo** (rótulo "Você se reconhece nesses sinais?")
- H2: "Quando `{{foco_principal}}` drena a sua energia e coloca a sua vida em pausa."
- Texto: "O sofrimento emocional não fica só na mente. Ele também cansa o corpo. Talvez você viva algumas destas situações:"
- 4 cartões (título curto + 1 frase): "A mente não desliga." · "O corpo sente junto." · "A vida fica em pausa." · "O ciclo se repete." (reescreva as frases conforme o foco).
- Frase final em itálico: "Reconhecer esses sinais não é um diagnóstico. É só o ponto em que a nossa conversa começa."

**4. O método** (rótulo "O método")
- H2: "Um acompanhamento pensado para o seu caso, do começo ao fim."
- Texto: "Não aplicamos técnicas padronizadas. O `{{nome_da_marca}}` combina recursos complementares em um plano feito para o seu momento."
- 3 cartões, um por recurso (ícone, título, 1 frase, link "Saiba mais" para o bloco do recurso). O `{{recurso_em_destaque}}` fica no cartão escuro com a etiqueta "Diferencial". Com 1 só recurso, use os 3 cartões para: o recurso, "Avaliação individual" e "Acompanhamento contínuo".
- Linha de 3 passos numerados: **Acolher** ("Ouvimos a sua história sem julgamentos para entender o que pesa e o que você deseja mudar.") · **Planejar** ("Você recebe um plano construído para o seu momento.") · **Transformar** ("Começamos o acompanhamento, com revisões ao longo do caminho.").

**5. Recurso 1** (layout dividido: texto à esquerda, painel à direita; no celular, painel e depois o botão)
- Rótulo: nome do recurso ou "O diferencial".
- H2 + texto de abertura + bloco "Como funciona na prática?" com 2 parágrafos simples.
- Painel com título (ex.: "Como entra no seu plano") e 4 itens em negrito + explicação: "Definido na avaliação." · "Sessões no seu ritmo." · "Evolução acompanhada." · "Você no controle."
- Botão "Quero agendar minha consulta".
- Se for Hipnose Clínica, inclua: você permanece consciente, ouve tudo e pode interromper quando quiser; nada de hipnose de palco.

**6. Recurso 2** (texto centralizado, sem painel)
- Rótulo, H2, texto de abertura, parágrafo menor (cinza) sobre como a frequência é definida na avaliação, botão "Quero agendar minha consulta".

**7. Recurso 3** (igual ao 5: texto + painel "O seu conforto em primeiro lugar" com 3 itens: "Clareza." · "No seu ritmo." · "O controle é seu.")
- Inclua `{{recursos_complementares_restricoes}}` e a frase "É um recurso complementar e não substitui o cuidado médico."

> Se houver só 1 recurso: mantenha a seção 5 e troque a 6 por "Como é uma sessão" (texto solo) e a 7 por "Para quem é indicado" (texto + painel). Se houver 2: mantenha 5 e 7 e use a 6 para "Como é uma sessão".

**8. Primeiro passo** (bloco escuro com brilho dourado; rótulo "O primeiro passo")
- H2: "Antes de traçar o seu plano, precisamos conhecer você."
- Texto: "A `{{primeira_consulta_nome}}` é um encontro individual, com entrega própria. Nela entendemos o contexto das suas queixas, os padrões que se repetem e o que você deseja alcançar."
- 2º parágrafo: "É a partir dela que o seu plano nasce: quais recursos entram, quantas sessões e com que frequência."
- Botão dourado "Agendar consulta agora".

**9. Local de atendimento** (rótulo "Local de atendimento")
- Cartão com foto do local à esquerda, à direita: "Presencial e online", endereço em 2 linhas, link "Ver no mapa" (abre `{{link_google_maps}}` em nova aba).
- Frase abaixo: "Você escolhe o formato que combina com a sua rotina. O acompanhamento é o mesmo nos dois casos."
- Só online: troque por "Atendimento online" + "Sessões por `{{plataforma_online}}`, para `{{abrangencia_online}}`" e remova o mapa.

**10. Depoimentos** (rótulo "O que meus pacientes dizem" ou "O que dizem as pessoas atendidas")
- H2: "O que muda quando você cuida da mente com acompanhamento."
- Texto curto: "Relatos de pessoas que passaram pelo acompanhamento. As experiências são individuais e podem variar."
- Grade de capas verticais (9:16): foto, botão de play, texto "Depoimento" ou "Depoimento de `{{nome_exibido}}`", faixa e marca vertical `{{nome_da_marca}}` na lateral. Legenda igual em todos: "Paciente do `{{nome_da_marca}}`".
- Clique abre o vídeo em uma janela (modal `<dialog>` com embed `youtube-nocookie.com`, autoplay). Abrindo o arquivo localmente (file://), abre o YouTube em nova aba.
- Sem foto de capa: usar `https://i.ytimg.com/vi/{{video_id}}/hqdefault.jpg`, salvo em `img/depoimento-{{video_id}}.jpg`.
- Botão "Quero agendar minha consulta" abaixo.
- Sem nenhum depoimento autorizado: esconda a seção inteira e o link do menu (não deixe grade vazia).

**11. Quem é** (rótulo "Quem vai atender você")
- H2 para 1 profissional: "Quem acompanha você em cada passo." Para 2: "Dois especialistas presentes em cada passo da sua jornada."
- Cartão: foto grande, nome, pílula com `{{papel_no_metodo}}`, `{{registro_profissional}}` em texto pequeno, bio justificada no computador (última linha alinhada à esquerda) e centralizada no celular, botão "Agendar consulta agora".
- 2º profissional: mesmo cartão. Se não houver, remova o cartão e centralize o primeiro.

**12. Dúvidas** (rótulo "Dúvidas sobre o processo"; H2 "Informação clara também constrói segurança."; texto "Entenda como o acompanhamento funciona na prática.")
Acordeão animado, uma resposta aberta por vez. Perguntas-padrão:
1. Como sei se a hipnoterapia é adequada para mim? → "É para isso que existe a primeira avaliação. Se não for o caminho mais indicado para o seu caso, dizemos com clareza."
2. A avaliação é cobrada? → conforme `{{primeira_consulta_cobrada}}` e `{{duracao_e_valor}}` ("Valor, duração e formato são informados no primeiro contato." se não quiser publicar).
3. O plano é igual para todos? → "Não. Recursos, número de sessões e frequência são definidos para o seu caso e revistos ao longo do acompanhamento."
4. Quantas sessões vou precisar? → "Isso é definido na avaliação, a partir dos seus objetivos, e pode mudar nas revisões."
5. Vou perder o controle durante a hipnose? → "Não. Você permanece consciente, ouve tudo e pode interromper a sessão quando quiser."
6. A hipnose funciona com todo mundo? → "As pessoas respondem de formas diferentes. Na avaliação conversamos sobre o seu caso e sobre o que é realista esperar."
7. O atendimento pode ser online? → "Sim. Atendemos presencialmente em `{{cidade_uf}}` e online via `{{plataforma_online}}`, `{{abrangencia_online}}`."
8. O que é preciso para a sessão online? → "Um lugar tranquilo, fone de ouvido e conexão estável. Enviamos as orientações antes do primeiro encontro."
9. O acompanhamento garante resultado? → "Não. Nenhum acompanhamento sério pode garantir resultado. As respostas variam de pessoa para pessoa, e os objetivos são revistos com transparência."
10. Substitui tratamento médico ou psicológico? → "Não. Não interrompa tratamentos nem altere medicações sem falar com o profissional de saúde responsável."
Acrescente 1 pergunta por recurso complementar ("O que é `{{recurso_n}}`?").

**13. Fechamento** (bloco escuro)
- H2: "Dê o primeiro passo para cuidar de `{{foco_principal}}` com acompanhamento de verdade."
- Texto: "Quebrar um ciclo começa quando entendemos de onde ele vem. Agende a sua consulta de avaliação e vamos conversar sobre o seu caso."
- Botão dourado "Quero agendar minha consulta".

**14. Rodapé** (escuro, tudo centralizado)
- Logo + subtítulo, frase curta ("Um acompanhamento que começa pela compreensão da sua história."), link grande em serifa "Agendar consulta agora", endereço clicável (Google Maps), ícones redondos (Instagram, WhatsApp, YouTube, outras), links internos (O método, recursos, Primeira avaliação, Onde atendemos, Depoimentos, Dúvidas), aviso de saúde (seção 9), `{{registro_profissional}}`, "© ano atual `{{nome_da_marca}}`. Todos os direitos reservados." (ano gerado por JS).
- Botão flutuante "Agendar consulta agora" no celular, aparece depois do hero e some no fechamento, com pulso dourado discreto.

### 5. Design (manter do modelo)

- **Fontes** (Google Fonts): Source Serif 4 nos títulos, Plus Jakarta Sans no corpo. `preconnect` para fonts.googleapis.com e fonts.gstatic.com.
- **Paleta** (variáveis em `:root`; os nomes vêm de uma versão antiga e podem ficar como estão):
  - `--green:#1B2F5C` azul-marinho principal · `--green-deep:#0B1D41` · `--forest:#07142F` fundos escuros
  - `--mint:#E6BB55` dourado de destaque · `--mint-soft:#F4E1AE`
  - `--paper:#F6F5F2` fundo tint · `--surface:#FDFCFA` fundo claro · `--line:#E2E1DC`
  - `--ink:#121A2E` títulos · `--text:#3A4256` corpo · `--slate:#5D6475` texto secundário
  - Se `{{paleta}}` trouxer outras cores: troque só os valores das variáveis, mantendo contraste mínimo 4.5:1 no texto (teste) e o dourado só como acento.
- **Raios**: 28 / 22 / 16 / 12 px. **Curva de animação**: `cubic-bezier(.22,1,.36,1)`.
- **Tipografia fluida** com `clamp()`; títulos com `text-wrap: balance`, parágrafos com `text-wrap: pretty`; H2 com largura máxima ~30ch e espaçamento generoso.
- **Tudo centralizado** no computador e no celular (rótulos, títulos, textos, botões), exceto o conteúdo interno dos painéis e a bio justificada.
- **Botões**:
  - Principal (`.btn.cta`): gradiente azul (#203A72 → #0B1D41), texto branco, ícone do WhatsApp em círculo dourado. No hover, um preenchimento dourado desliza da esquerda para a direita, o texto fica azul e o ícone gira e inverte as cores. Nos blocos escuros, o botão é dourado e o preenchimento do hover é branco.
  - Secundário (`.btn.ghost`): contorno azul que se preenche de azul no hover.
  - No toque (celular): leve encolhida (scale .97), preenchimento e efeito de onda (ripple) no ponto tocado.
  - Um brilho atravessa cada botão uma única vez quando ele entra na tela.
- **Rótulos de seção**: pílula com ponto dourado e anel pulsante.
- **Cartões**: elevam no hover; no celular, o cartão que está no centro da tela fica destacado.

### 6. Animações e interações (manter do modelo)

- Entrada do hero em sequência ao carregar (`data-load`) e anéis SVG se desenhando atrás da foto.
- Elementos surgem ao rolar (`data-reveal`, IntersectionObserver), com o atributo removido no fim da transição.
- Barra superior ganha sombra ao rolar; link do menu da seção visível fica ativo.
- FAQ abre e fecha com animação de altura.
- Modal de vídeo fecha com Esc, clique fora e botão ×, e para o vídeo ao fechar.
- `prefers-reduced-motion`: desliga todas as animações e mostra tudo direto.

### 7. Requisitos técnicos

- Um único `index.html` (CSS e JS inline) + pasta `img/` + imagem de compartilhamento na raiz. **Nenhuma imagem em base64** dentro do HTML (pesa e quebra a prévia nas redes).
- Fotos otimizadas em JPG ou WebP: hero e perfil até ~200 KB, capas de depoimento até ~80 KB. `width`/`height` definidos, `loading="lazy"` em tudo abaixo do hero, `alt` descritivo.
- WhatsApp: todos os botões apontam para `https://wa.me/{{whatsapp_numero}}?text={{whatsapp_mensagem codificada}}` com `target="_blank" rel="noopener"` e atributo `data-wa`. Uma constante `WHATSAPP` no JS com o número.
- **Metatags logo depois do `<title>`** (a ordem importa para o WhatsApp): description, og:title, og:description, og:image (URL absoluta em `{{dominio_final}}`), og:image:secure_url, og:image:type, og:image:width 1200, og:image:height 630, og:image:alt, og:url, og:type website, og:site_name, og:locale pt_BR, twitter:card summary_large_image, twitter:title, twitter:description, twitter:image, theme-color `#0B1D41`, canonical.
- **Imagem de compartilhamento** `og-{{marca-sem-espaços}}.jpg`, 1200×630, menos de 300 KB: fundo azul-marinho, foto do profissional à direita, marca + frase curta + cidade em branco e dourado. Gere com Playwright a partir de um HTML auxiliar.
- **Favicon** SVG inline com o selo de anéis dourados (ou as iniciais do profissional) nas cores da paleta.
- Pontos de quebra do modelo: 1260px (vira menu), 960px (colunas viram uma), 640px (celular). Sem rolagem horizontal em nenhuma largura.
- Acessibilidade: foco visível no teclado, `aria-expanded` no menu, `aria-label` nos ícones das redes, contraste AA, botões com área de toque mínima de 44px, `lang="pt-BR"`.

### 8. Regras de redação e cuidados legais

- **Não usar**: "cura", "curar", "resultado garantido", "cientificamente comprovado", "100%", "o único método", "elimina", "definitivo", promessas de prazo ou tempo ("em 30 dias", "em 3 meses", "em poucas sessões"), números de clientes ou taxas de sucesso sem fonte.
- **Não falar em diagnóstico**: o site não diagnostica o visitante. Use "sinais", "situações", "queixas".
- **"Psicoterapia" e "tratamento psicológico"**: só se o profissional tiver CRP ativo. Hipnoterapeuta sem registro usa "hipnoterapia", "acompanhamento", "sessões".
- **Profissional com registro em conselho** (CRP, CRM, COFFITO, CRO etc.): antes de publicar, confira as regras de publicidade do conselho sobre depoimentos, preços, fotos de pacientes e títulos. Alguns conselhos restringem depoimentos; nesse caso, esconda a seção 10.
- **Recursos complementares** (Reiki, biomagnetismo, aparelhos de biofeedback ou de "frequência" etc.): descrever como complementares, "segundo o fabricante/a abordagem" quando o mecanismo não tiver consenso científico, e sempre com a frase de que não substituem o cuidado médico.
- **Depoimentos**: só publicar com autorização por escrito de uso de imagem e voz; guardar o documento.
- **Termos técnicos** sempre seguidos de explicação simples.
- Tom: profissional, calmo, acolhedor e direto. Frases curtas. Sem exagero de vendas.

### 9. Itens que completam o site (incluir)

- **Aviso de saúde no rodapé**: "As informações deste site não substituem avaliação ou tratamento médico ou psicológico. Em situação de crise, procure um serviço de emergência ou ligue para o CVV, 188 (24 horas, gratuito)."
- **Privacidade (LGPD)**: link "Política de privacidade" no rodapé abrindo um `<dialog>` com texto curto: que dados são coletados (só os que a pessoa envia pelo WhatsApp), para que são usados, como pedir exclusão, e contato. Se `{{ferramentas_de_medicao}}` não for "nenhuma", incluir aviso de cookies com botão "Aceitar" e só carregar o script de medição depois do aceite.
- **Dados estruturados** (JSON-LD `ProfessionalService` ou `LocalBusiness`): nome, descrição, endereço, telefone, URL, sameAs com as redes, área atendida. Ajuda no Google.
- **`robots.txt` e `sitemap.xml`** na raiz, com o `{{dominio_final}}`.
- **`README.md`** com como editar textos, trocar fotos e publicar.
- **Link para o Google Meu Negócio** no "Ver no mapa", se o perfil existir.

### 10. Verificação antes de entregar

1. Abra o site com Playwright em 1440px, 1280px, 1024px, 768px, 390px e 360px. Tire capturas de cada seção e corrija: rolagem horizontal, textos cortados, botões quebrando linha, títulos sobrepondo as capas de depoimento, menu mobile.
2. Teste: menu abre e fecha (link, fora, Esc); FAQ; modal de vídeo; botão flutuante aparece e some; todos os links do WhatsApp abrem com a mensagem certa; links internos levam à seção certa.
3. Busque no HTML os nomes e dados do profissional original (lista na seção 1) e as palavras proibidas (seção 8). Resultado esperado: zero.
4. Liste todos os `[a preencher: ...]` restantes.
5. Confira o peso: `index.html` abaixo de 120 KB, imagens dentro dos limites.

### 11. Entregas

1. `index.html`, `img/`, `og-....jpg`, `robots.txt`, `sitemap.xml`, `README.md`.
2. Relatório curto com: o que foi adaptado em relação ao modelo, textos do cliente que foram ajustados e por quê, e a lista de pendências (campos `[a preencher]`, autorizações de depoimento, conferência do conselho, foto que falta).
3. Se houver repositório Git conectado à Vercel: commit, push e confirmação de que a publicação terminou. Depois, peça para testar a prévia de compartilhamento em `https://developers.facebook.com/tools/debug/` (botão "Extrair novamente") e enviar o link no WhatsApp com `?v=1` no fim, para escapar do cache.
