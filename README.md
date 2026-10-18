# MicroHub

**Rascunho.** Não há código de produção, release nem versão utilizável. Nada aqui deve ser
lido como compromisso de escopo, prazo, compatibilidade ou API.

O MicroHub é um hub **local**, para Windows, para trabalhar com microcontroladores em
MicroPython — começando pela LOLIN D32 (ESP32 clássico), o hardware visado efetivo do MVP.
O Raspberry Pi Pico original (RP2040) está morto/deferido, fora do MVP. A proposta é reunir
num só lugar o que hoje fica espalhado entre editor,
terminal, gravador de firmware e console serial, preservando o contexto do projeto entre
uma sessão e outra.

A intenção é integrar ferramentas consolidadas — entre as candidatas, `mpremote`,
`esptool`, `picotool` e os fluxos UF2 do RP2040 (deferidos com o Pico — fora do MVP)
— em vez de reimplementar compiladores, protocolos ou simuladores. Projetos, código e
histórico permanecem locais por padrão; serviços externos são opcionais e explícitos.

## Status

- **Sem código.** Nenhuma funcionalidade existe; nada foi executado em hardware.
- **Sem compatibilidade declarada.** Nenhuma placa é oficialmente suportada: isso exige
  teste físico, que ainda não foi feito. A matriz de compatibilidade está inteira em
  *não avaliada*.
- **Sem transporte validado.** O transporte primário é serial USB; Wi-Fi é essencial depois
  (P1, fora do MVP) e um complemento móvel é futuro (pós-MVP).
- **Sem interface.** A UI ainda não foi desenhada: depende de pesquisa de referências
  visuais e de assets de logo, ambos pendentes.

## Roteiro

| Marco | Resultado |
|---|---|
| M0 | Fundação e prova de viabilidade na LOLIN D32 |
| M1 | Fundação do produto: projetos, persistência, operações |
| M2 | Fluxo essencial: editor, REPL, transferência, execução |
| M3 | Firmware e recuperação validados |
| M4 | Continuidade, qualidade de uso e instalação limpa |
| M5 | Observabilidade inicial baseada em evidências |
| M6 | Extensões experimentais, incluindo simulação |

Cada marco termina com demonstração reproduzível, evidências e documentação atualizada.

O escopo do primeiro produto utilizável é **condicional a M0**: se a prova de viabilidade
não passar na LOLIN D32, escopo e stack são reavaliados explicitamente antes de qualquer
compromisso de entrega.

## Fora do escopo

- substituir integralmente todas as IDEs e toolchains existentes;
- suportar placas de todos os fabricantes;
- reimplementar compiladores, gravadores ou protocolos consolidados;
- garantir simulação elétrica precisa;
- deduzir automaticamente todo o estado interno de qualquer programa;
- exigir infraestrutura em nuvem para operações locais.

## Licença

MIT — ver [LICENSE](LICENSE).
