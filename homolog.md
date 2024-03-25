# Homologação - ATC TECH com forma de pagamento via PagSeguro

## URL Sandbox:

Link em ambiente SANDBOX para homologação pela PagSeguro, checkout para pagamento:

https://atctech-checkout-git-feat-billet-daniloras.vercel.app/?pay=TVM4eQ%3D%3D

<img width="376" alt="Captura de Tela 2024-03-25 às 00 49 58" src="https://github.com/daniloras/atctech-homolog/assets/25010021/04327384-545c-46d0-a3ec-dab357a74786">

## Forma de Pagamento: Cartão de Crédito - Visão usuário

<img width="606" alt="Captura de Tela 2024-03-25 às 00 56 45" src="https://github.com/daniloras/atctech-homolog/assets/25010021/eea77b0e-6506-41a6-a803-57511fcbd344">

### Request / Cartão de Crédito

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
        "type": "CREDIT_CARD",
        "installments": 1,
        "capture": true,
        "card": {
          "encrypted": "IwwJxzLOJmqOju+rCfujOehuGz9DN9QQDrun1FaZnf5i2sfzCw7MzMb0+uhoSpfXDG6ocfSHcPo8kRWiT0LMQn7MNjTRtoRCSd5s6oL7RdNWHQSotzeIQ0jPBPRJdNyNuMSD305xwaPziN/3NBlwDJ1VbrKj2ziP/bgGkmyCYurRfN6vEcrc8LBZNhtPaoa2YuddzOeyTLwQB7LYEQSyUMLeFzjyJwX2P4GZSVsNtwdwqjJSyk9yHs0wgUicDt52usCehfeHmi6SsLKB8iaZkV3LV68NKGuwOWD7p8nxou2p3iY4pviHTunJk0Nm43BMUqz7pvZLUE9SWxePRL5kuA==",
          "security_code": "123",
          "holder": {
            "name": "JOAQUIM TAVORA"
          },
          "store": false
        }
      }
    }
  ]
}
```

### Response / Cartão de Crédito

```json
{
    "status": 201,
    "statusCredit": "PAID",
    "pdf": "https://sandbox.api.pagseguro.com/charges/CHAR_EBBB3946-2C0B-4C09-B12B-54A9798C1346"
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
