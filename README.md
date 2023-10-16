# exchangerate

This library is a pure Go interface for the [ExchangeRate-API](https://www.exchangerate-api.com/).

## Requirements

You will need an API key from [ExchangeRate-API](https://www.exchangerate-api.com/). Place the API key in the environment variable `EXCHANGERATE_API_KEY`.

## Sample Usage

```go
package main

import (
    "fmt"
    "github.com/sorucoder/exchangerate"
)

func main() {
    fmt.Printf("$5.50 USD = £%0.2f GBP\n", exchangerate.Convert(exchangerate.CurrencyFromCode("USD"), exchangerate.CurrencyFromCode("GBP"), 5.5))
}
```