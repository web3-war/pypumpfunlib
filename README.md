# pypumpfunlib
pump fun trading sdk



### Install 

```
pip install pypumpfunlib-1.1.2-py3-none-any.whl
```



### usage

```python
from pypumpfunlib.api import PumpFunClient

if __name__ == '__main__':
    bs58_private_key = '67rpwLCuS5DGA8KGZXKsVPuheKEb183tzoZ8WFUAFJnqEvsKKrePqksDCCc1qvkkRzHxD5tEhSkUUfjW2aQzMJGE'
    pump_fun_client = PumpFunClient(bs58_private_key)
    
    # Buy Example
    mint_str = "4sESKab2mXSkanR26zoE5RX6qbJF7vCZbFtp7id7MiYx"
    pump_fun_client.buy(mint_str=mint_str, sol_in=.0001, slippage=25)

    # Sell Example
    mint_str = "4sESKab2mXSkanR26zoE5RX6qbJF7vCZbFtp7id7MiYx"
    token_balance = pump_fun_client.get_token_balance(mint_str)

    pump_fun_client.sell(mint_str=mint_str, token_balance=token_balance, slippage=25, close_token_account=True)

```

