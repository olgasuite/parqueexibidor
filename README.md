# Parque de Servidores OLGA Flux

<!-- aviso-ia -->
> **Feito com IA.** O código deste repositório foi escrito pelo **Claude Code** (inteligência artificial da Anthropic), a partir das especificações, dos testes e da revisão do autor. Leia antes de usar, como faria com qualquer código.

Levantamento dos **servidores de cinema digital** das salas cadastradas no OLGA Flux: fabricante, modelo, número de série e ano de lançamento do equipamento de cada sala, com o certificado do servidor quando disponível.

Página publicada em: https://olgasuite.github.io/parqueexibidor/

## A página

- **Resumo** por modelo: fabricante, modelo, ano de lançamento, quantas salas e em quais UFs.
- **Salas**: complexo, sala, lugares, fabricante, modelo, serial, lançamento e certificado.
- Filtros por UF e por modelo. Servidores montados só para um evento aparecem como "provisório".

## De onde vêm os dados

- O servidor de cada sala foi identificado pelos **KDMs** que a sala recebe (o destinatário do KDM traz o modelo e o serial do servidor) e conferido com o cadastro de salas do Flux e os dados abertos da ANCINE.
- `certs/`: certificados dos servidores. Os da Dolby vêm do portal público da Dolby, pelo número de série; os demais, dos fabricantes ou das próprias salas, e só entram quando o thumbprint confere.
- A página é regenerada a partir do Flux por um script (`parque_atualizar.py`, no repositório de levantamento de servidores). Fabricante, modelo, ano e certificado são curados à mão e mantidos a cada atualização.
