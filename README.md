# gorm-sqlcipher


## Installation

go get github.com/BoredTape/gorm-sqlcipher

## How to use

```go
import (
	sqliteEncrypt "github.com/BoredTape/gorm-sqlcipher"
	"gorm.io/gorm"
)

key := "2DD29CA851E7B56E4697B0E1F08507293D761A05CE4D1B628663F411A8086D99"
dbname := fmt.Sprintf("db?_pragma_key=x'%s'&_pragma_cipher_page_size=4096", key)
db, err := gorm.Open(sqliteEncrypt.Open(dbname), &gorm.Config{})
```

## More
- https://github.com/mutecomm/go-sqlcipher
- https://github.com/go-gorm/gorm
