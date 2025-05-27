# In-Memory Cache

Простой потокобезопасный in-memory кэш на Go с методами `Set`, `Get` и `Delete`.

## 📦 Установка

```bash
go get github.com/<your-github-username>/inmemory-cache


🚀 Использование
package main

import (
	"fmt"
	"github.com/PhoenixJustCode/inmemory-cache-golang"
)

func main() {
	c := cache.New()

	c.Set("userId", 42)
	userId := c.Get("userId")
	fmt.Println(userId) // 42

	c.Delete("userId")
	userId = c.Get("userId")
	fmt.Println(userId) // <nil>
}


🧠 Методы
Метод	 - Описание
Set(key, value)	- Устанавливает значение по ключу
Get(key)	- Получает значение по ключу (или nil)
Delete(key)	- Удаляет значение по ключу

