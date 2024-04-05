# Homologação emambiente de Produção - ATC TECH com forma de pagamento via PagSeguro

## URL Produção / Provisória:

Link em ambiente PRODUÇÃO para homologação pela PagSeguro, checkout para pagamento:

LINK: https://atctech-checkout-git-feat-billet-daniloras-projects.vercel.app/?pay=TVRBdk1nPT0=

<img width="324" alt="Captura de Tela 2024-04-05 às 07 46 59" src="https://github.com/daniloras/atctech-homolog/assets/25010021/c0702eb4-6e8c-4571-8165-6bb393cda000">

## Forma de Pagamento: Cartão de Crédito - Visão usuário

<img width="326" alt="Captura de Tela 2024-04-05 às 07 49 41" src="https://github.com/daniloras/atctech-homolog/assets/25010021/d577a5d6-66f8-4b37-b6cc-badac5dde5a6">

### Request / Cartão de Crédito

```json
{
  "reference_id": "atctech-10-2",
  "customer": {
    "name": "Danilo Ramon",
    "email": "contato@d2f.dev",
    "tax_id": "47479020074",
    "phones": []
  },
  "items": [
    {
      "reference_id": "atctech-10-2",
      "name": "Escritório - Romão - Plano Anual",
      "quantity": 1,
      "unit_amount": 9990
    }
  ],
  "shipping": {
    "address": {
      "country": "BRA",
      "region": "safmkl",
      "region_code": "SP",
      "city": "safmkl",
      "postal_code": "13102910",
      "street": "fq090q9q",
      "number": "asmklm",
      "locality": "aslmf"
    }
  },
  "notification_urls": [
    "https://atctech.com.br/pagseguro-notifications"
  ],
  "charges": [
    {
      "reference_id": "atctech-10-2",
      "description": "Produto utilização PicNoLie - Extensão do google",
      "amount": {
        "value": 9990,
        "currency": "BRL"
      },
      "payment_method": {
        "type": "CREDIT_CARD",
        "installments": 4,
        "capture": true,
        "card": {
          "encrypted": "RAcxyKO8R7tjkt2H+vGZKaaIp3GtAeXn/kzGX6h7Zmk1Zf/Ieo3ow+t8Q2kxRBCS1EN/SoAhN/PJpiBA/Xdmuj50RuEeQcl7vEK4Qbg3Z+3OMJFg776QcZhsKg/KHdt7HwZkpcbo+ksTd0FIsYbmhoojGu90nHHH5Cofd6MC7rYxqn+xtnRkJDcxMWMz5jevRJCu6b8ykHTVQm6qidj0tSlo5RK055CN8xphMpQWXZ7Z78FWulotlR9wpCjdYko7XSslOlYoS50Oe5Qp9g+rUSGC4aoIB99UqU8Wixg2zqPiF2d+O7J/pFpLA+oI+5SD5Wc5EWmAmlj/JO+44jov+w==",
          "security_code": "668",
          "holder": {
            "name": "JOÃO SILVA"
          },
          "store": false
        }
      }
    }
  ]
}
```

### Response / Cartão de Crédito

<img width="308" alt="Captura de Tela 2024-04-05 às 07 50 37" src="https://github.com/daniloras/atctech-homolog/assets/25010021/a1599565-cecb-4589-aa9e-acba722249b6">

```json
{
  "status": 201,
  "statusCredit": "DECLINED",
  "pdf": "https://api.pagseguro.com/charges/CHAR_0AD5C94E-BBFC-4FD8-AFC5-695142151A5D"
}
```

## Forma de Pagamento: Boleto bancário - Visualização usuário

<img width="510" alt="Captura de Tela 2024-03-25 às 01 06 00" src="https://github.com/daniloras/atctech-homolog/assets/25010021/d13c1db8-3df0-45e3-beff-ffa45347ce85">

## Forma de Pagamento: Boleto bancário - Visualização PDF

<img width="517" alt="Captura de Tela 2024-03-25 às 01 00 20" src="https://github.com/daniloras/atctech-homolog/assets/25010021/1cf099b3-b252-45ac-87ab-1359df9ee58e">

### Request / Boleto bancário

```json
{
  "reference_id": "atctech-1-2",
  "customer": {
    "name": "Cíntia Rodrigues",
    "email": "v09583091644705564494@sandbox.pagseguro.com.br",
    "tax_id": "31701286807",
    "phones": []
  },
  "items": [
    {
      "reference_id": "atctech-1-2",
      "name": "Escritório - Romão - Plano Anual",
      "quantity": 1,
      "unit_amount": 9990
    }
  ],
  "shipping": {
    "address": {
      "country": "BRA",
      "region": "wqomp",
      "region_code": "SP",
      "city": "wqomp",
      "postal_code": "09092223",
      "street": "rqpjreqopji2",
      "number": "awqoiopqm",
      "locality": "mqiom"
    }
  },
  "notification_urls": [
    "https://atctech.com.br/pagseguro-notifications"
  ],
  "charges": [
    {
      "reference_id": "atctech-1-2",
      "description": "Produto utilização PicNoLie - Extensão do google",
      "amount": {
        "value": 9990,
        "currency": "BRL"
      },
      "payment_method": {
        "type": "BOLETO",
        "boleto": {
          "due_date": "2023-12-01",
          "instruction_lines": {
            "line_1": "Pagamento processado Produto utilização PicNoLie - Extensão do google",
            "line_2": "Via PagSeguro"
          },
          "holder": {
            "name": "Cíntia Rodrigues",
            "tax_id": "31701286807",
            "email": "contato@atctech.com.br",
            "address": {
              "country": "BRA",
              "region": "wqomp",
              "region_code": "SP",
              "city": "wqomp",
              "postal_code": "09092223",
              "street": "rqpjreqopji2",
              "number": "awqoiopqm",
              "locality": "mqiom"
            }
          }
        }
      }
    }
  ]
}
```

### Response / Boleto bancário

```json
{
    "status": 201,
    "statusCredit": "WAITING",
    "pdf": "https://boleto.sandbox.pagseguro.com.br/3876e67a-6d0a-45a0-ac71-0271e9de13b0.pdf"
}
```

## Forma de Pagamento: PIX Qr Code

<img width="573" alt="Captura de Tela 2024-03-25 às 01 07 06" src="https://github.com/daniloras/atctech-homolog/assets/25010021/bd0733da-25c6-44e3-b7df-9e8d9eea6357">

### Request / PIX Qr Code

```json
{
  "reference_id": "atctech-1-2",
  "customer": {
    "name": "Cíntia Rodrigues",
    "email": "v09583091644705564494@sandbox.pagseguro.com.br",
    "tax_id": "31701286807",
    "phones": []
  },
  "items": [
    {
      "reference_id": "atctech-1-2",
      "name": "Escritório - Romão - Plano Anual",
      "quantity": 1,
      "unit_amount": 9990
    }
  ],
  "shipping": {
    "address": {
      "country": "BRA",
      "region": "wqomp",
      "region_code": "SP",
      "city": "wqomp",
      "postal_code": "09092223",
      "street": "rqpjreqopji2",
      "number": "awqoiopqm",
      "locality": "mqiom"
    }
  },
  "notification_urls": [
    "https://atctech.com.br/pagseguro-notifications"
  ],
  "qr_codes": [
    {
      "amount": {
        "value": 9990
      }
    }
  ]
}
```
### Response / PIX Qr Code

```json
{
    "status": 201,
    "pdf": null,
    "qrCode": "00020101021226850014br.gov.bcb.pix2563api-h.pagseguro.com/pix/v2/EEEEADAD-173C-4151-8B27-FC4AD321D65327600016BR.COM.PAGSEGURO0136EEEEADAD-173C-4151-8B27-FC4AD321D653520489995303986540599.905802BR5922RSP SERVICOS ADMINISTR6009Sao Paulo62070503***6304F513",
    "qrCodeImg": "https://sandbox.api.pagseguro.com/qrcode/QRCO_EEEEADAD-173C-4151-8B27-FC4AD321D653/png"
}
```
