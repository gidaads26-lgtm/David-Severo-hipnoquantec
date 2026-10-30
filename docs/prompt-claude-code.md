# Prompt para Claude Code — Site HipnoQuantec®

> Coloque na pasta do projeto: `briefing.pdf` (briefing do cliente), `modelo.html` (estrutura visual) e, se tiver, `fontes/` (material técnico do fabricante do Quantec, transcrição do documentário, PDFs dos estudos). Depois cole o texto abaixo.

---

Atue como copywriter sênior e desenvolvedor front-end. Sua tarefa é escrever a copy de um site institucional e entregá-la já aplicada em um `index.html` responsivo, em português do Brasil.

## Fontes, em ordem de autoridade

1. `briefing.pdf` — é a regra final. Tom de voz, posicionamento, arquitetura e, principalmente, a lista de afirmações proibidas (seção 11.3) e as restrições sobre Quantec Pro e Par Biomagnético (seção 4). Se qualquer outra fonte contradizer o briefing, siga o briefing e registre o conflito.
2. `modelo.html` — estrutura visual e blocos a preencher. Mantenha a intenção de cada bloco; acrescente seções que o briefing exige e o modelo não tem (identificação com o problema, jornada T0–30–60–90, transparência sobre evidências).
3. `fontes/` — use apenas o que for verificável. Para cada estudo citado, informe instituição, desenho, número de participantes, duração e o que foi de fato medido. Não estenda o resultado para desfechos que o estudo não mediu (ex.: um estudo sobre glicemia em idosos não comprova efeito sobre ansiedade).

## Contexto do negócio

- Método HipnoQuantec®: Hipnose Clínica (com PNL), Par Biomagnético e Quantec® Pro, integrados em um acompanhamento individualizado para ansiedade.
- Porta de entrada: anamnese paga, com entrega própria. Ela define sessões de hipnose, indicação do Par Biomagnético, configuração do Quantec Pro e indicadores.
- Quantec Pro: diferencial tecnológico central, tratamento de 3 meses para todos que iniciam essa etapa; intervalos e duração das emissões definidos pelo sistema; registros comparados em ~30, 60 e 90 dias a partir de T0. Relatórios documentam o processo e não comprovam, sozinhos, melhora clínica.
- Atendimento presencial na Baixada Santista e online para o Brasil (marcar como "a confirmar").
- Público: pessoas com ansiedade, preocupação excessiva, evitação, insegurança. Não diagnosticar o visitante.

## Regras de redação

- Tom profissional, calmo, direto. Termos técnicos sempre seguidos de explicação em linguagem comum.
- Proibido: "cura", "resultado garantido", "cientificamente comprovado", "elimina o placebo", "reprograma o DNA", "atua em nível atômico/quântico", "age na causa raiz", "o único método", "campo morfogenético" como fato.
- Descreva o funcionamento do Quantec como "segundo o fabricante" e deixe claro que os mecanismos não fazem parte do consenso científico.
- Não use o laboratório PEAR (Princeton) como prova: não estudou o Quantec e seus resultados não foram replicados.
- Não invente nomes, credenciais, números de clientes, depoimentos ou preços. Use colchetes `[a confirmar]` visíveis.
- Inclua aviso de segurança no contato (CVV 188) e aviso legal no rodapé.
- Um CTA principal em todo o site: "Agendar minha anamnese". CTA secundário: "Ver como o método funciona".

## Entregas

1. `copy.md` — copy organizada por seção, com o seletor HTML exato de cada texto (id ou classe), 3 opções de H1 com justificativa, title e meta description, e uma tabela de "afirmações ajustadas" (o que foi pedido × o que as fontes sustentam × como entrou).
2. `index.html` — página única, autocontida (CSS e JS inline, fontes do Google Fonts), paleta verde/branco/cinza do briefing, mobile primeiro, foco visível no teclado, `prefers-reduced-motion` respeitado, formulário com validação e mensagem de protótipo (sem envio real).
3. `pendencias.md` — checklist do que o cliente precisa validar antes de publicar.

## Processo

1. Leia o briefing inteiro e liste as restrições antes de escrever.
2. Mapeie os blocos do `modelo.html` e proponha a ordem final das seções.
3. Escreva a copy, revise contra a lista de proibições e só então gere o HTML.
4. Abra o `index.html` em 1280px e 390px (Playwright, se disponível), corrija quebras de layout e confirme que não há rolagem horizontal.
5. Termine com um resumo curto: o que mudou em relação ao pedido original e o que falta o cliente enviar.
