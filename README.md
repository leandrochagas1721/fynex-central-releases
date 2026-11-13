# Central de Integrações Bancárias — MK-AUTH

Addon do MK-AUTH que registra boletos na API do **Sicoob (Cobrança V3)** e dá baixa automática no MK-AUTH quando o cliente paga.

- Registro do boleto no banco pelo painel ou automático, X dias antes do vencimento
- Baixa automática no MK-AUTH (webhook do Sicoob + conferência a cada 15 min)
- Pix no boleto, cancelamento no banco, grade de lançamentos com histórico
- Atualização pelo próprio painel

## Requisitos

- MK-AUTH com acesso root (terminal)
- Conta Sicoob com a **API Cobrança** liberada no portal de desenvolvedores (Client ID + certificado .pfx) Manual: 

## Instalação

Como root no servidor do MK-AUTH:

```bash
cd /tmp
wget -O fynex-central.zip https://github.com/leandrochagas1721/fynex-central-releases/releases/latest/download/fynex-central-instalacao.zip
rm -rf fynex-central-bancaria && unzip -q fynex-central.zip && cd fynex-central-bancaria
bash install.sh SEU_LOGIN_DO_MKAUTH
```

O instalador pede **CPF ou CNPJ** (e, para CPF, nome, CEP e número) e ativa **15 dias grátis**.
Depois, o menu fica em **Financeiro › Integrações Bancárias**.

## Primeiros passos

1. Em **Integrações Bancárias**, cadastre a conta Sicoob: número do cliente, Client ID e certificado.
2. Clique em **Testar**. Deve aparecer **Sucesso**.
3. Na lista de lançamentos, registre o primeiro boleto.

## Licença

A mensalidade é paga por **Pix** dentro do próprio addon: clique na versão no topo da tela e depois em **Pagar via Pix**.
A licença é renovada sozinha depois do pagamento.
Com a licença vencida, a emissão de boletos para, mas **as baixas dos boletos já registrados continuam**.

## Atualização

Clique na versão no topo da tela e depois em **Procurar** e **Atualizar**.
A atualização é aplicada em até 1 minuto, com cópia de segurança automática.

## Suporte

Desenvolvedor — suportesistema@fynexfibra.com.br
Telefone: (91) 2888-0033
