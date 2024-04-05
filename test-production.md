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

<img width="317" alt="Captura de Tela 2024-04-05 às 07 54 55" src="https://github.com/daniloras/atctech-homolog/assets/25010021/d7a5d8b4-a8af-4c7c-90a9-45ea0423063d">


## Forma de Pagamento: Boleto bancário - Visualização PDF

<img width="419" alt="Captura de Tela 2024-04-05 às 07 57 44" src="https://github.com/daniloras/atctech-homolog/assets/25010021/d9c0a34b-b9a4-4d35-90ae-7307f2ac1832">


### Request / Boleto bancário

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
        "type": "BOLETO",
        "boleto": {
          "due_date": "2024-04-12",
          "instruction_lines": {
            "line_1": "Pagamento processado Produto utilização PicNoLie - Extensão do google",
            "line_2": "Via PagSeguro"
          },
          "holder": {
            "name": "Danilo Ramon",
            "tax_id": "47479020074",
            "email": "contato@d2f.dev",
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
  "pdf": "https://boleto.pagseguro.com.br/46b85ed3-f3a3-4160-8ea1-4f72d5184b6e.pdf"
}
```

## Forma de Pagamento: PIX Qr Code

<img width="335" alt="Captura de Tela 2024-04-05 às 07 59 45" src="https://github.com/daniloras/atctech-homolog/assets/25010021/cff4005a-66db-46a6-9810-2a92a96e2904">

## Forma de Pagamento: PIX Qr Code - Visualizando QR Code

<img width="320" alt="Captura de Tela 2024-04-05 às 08 02 20" src="https://github.com/daniloras/atctech-homolog/assets/25010021/97ebb22d-8c09-4570-8721-7e857f045d11">

### Request / PIX Qr Code

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
  "qrCode": "00020101021226600016BR.COM.PAGSEGURO0136A33B0FE0-A1F6-4EE4-83C0-640E2DA4FAF1520473925303986540599.905802BR5925RSP SERVICOS ADMINISTRATI6009Sao Paulo63044870",
  "qrCodeImg": "https://api.pagseguro.com/qrcode/QRCO_A33B0FE0-A1F6-4EE4-83C0-640E2DA4FAF1/png"
}
```
