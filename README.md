<p align="center"><img alt="pix-utils" src="./assets/logo-pix.png" width="128px" /></p>

# <p align="center">Go-Pix-Utils<p>

<p align="center">
  <a
    href="https://github.com/thalesog/go-pix-utils/blob/master/LICENSE"
    target="blank"
  >
    <img
      src="https://img.shields.io/github/license/thalesog/go-pix-utils?style=for-the-badge&color=blueviolet"
      alt="License"
    />
  </a>
  <a href="https://github.com/thalesog/go-pix-utils/stargazers" target="blank">
    <img
      src="https://img.shields.io/github/stars/thalesog/go-pix-utils?style=for-the-badge&color=blueviolet"
      alt="Stars"
    />
  </a>
</p>

> ### ⚠️ This package is under development and is not ready for production

> Pix-Utils is a set of tools to parse, generate and validate payments of Brazil Instant Payment System (Pix), making fast and simple to handle charges and proccess then in your project. Originally developed using [TypeScript](https://github.com/thalesog/pix-utils), this is the Go version of the library.

# 🚀 Usage

### Install the package in your project

```sh
go get github.com/thalesog/go-pix-utils
```

### Create Static Pix

```go
package main

import (
	"github.com/thalesog/go-pix-utils/pixUtils"
)

func main() {
	pixUtils.CreateStaticPix(pixUtils.CreateStaticPixParams{
    MerchantName:      "Thales Ogliari",
    MerchantCity:      "São Miguel do Oeste",
    PixKey:            "thalesog@me.com",
    TransactionAmount: 10.00,
    AditionalData:     "Pedido 123",
  })
}
```

### Create Dynamic Pix

```go
package main

import (
	"github.com/thalesog/go-pix-utils/pixUtils"
)

func main() {
	pixUtils.CreateDynamicPix(pixUtils.CreateDynamicPixParams{
    MerchantName:      "Thales Ogliari",
    MerchantCity:      "São Miguel do Oeste",
    Url:               "https://pix.thalesogliari.com.br",
  })
}
```


## 📍 To Do

- [x] Parse Static Pix EMV
- [x] Parse Dynamic Pix EMV
- [x] Parse Pix without specifying the type
- [x] Validate CRC16
- [x] Generate Static Pix EMV
- [x] Generate Dynamic Pix EMV
- [ ] Generate QRCode from EMV or Pix
- [ ] Refactor EMV parsing and remove DRY code

# 🍰 Contributing

Please contribute using [GitHub Flow](https://guides.github.com/introduction/flow). Create a branch, add commits, and [open a pull request](https://github.com/thalesog/go-pix-utils/compare).

# 📝 License

This project is under [MIT](https://github.com/thalesog/go-pix-utils/blob/master/LICENSE) license.

#

<p align="center">
 Developed with 💚 by <a href="https://github.com/thalesog">@thalesog</a> 🇧🇷
</p>
