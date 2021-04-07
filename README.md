# Liquidation Templates
Collection of liquidation hint messages

## File format

All submitted liquidation notification must be a json in the following format: 

```json
{
    "variables": [
        "contract_type",
        "value"

    ],
    "var_allowed": {
        "contract_type": ["USDT"]
    },
    "message": [
        "[Huobi][<contract_type>本位永续][<contract_type>全仓账户]",
        "您的帐户的担保资产已低于0，有<contract_type>等一个合约已被强平。"
    ]
}
```

### Properties

| variables | meaning |
|:-------|------|
| variables | Allowed variables in user dictionary |
| var_allowed | Allowed variable values |
| message | Message itself, anything in\<\> will be replace with variable |

### Predefined vars

These vars are defined in templates engine, and can be used with declaration.  
- Time `<time>`
  Current system time

## Pull request

You should place your template in the following format:  
`<repo root>/<codename>/<whatever>.lqtpl.json`  
Where codename should be the trader's English name.
